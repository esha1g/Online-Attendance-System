package dbo;
import java.sql*;
import javax.swing*;

public class dblayer
{
    static String driver="oracle.jdbc.driver.OracleDriver";
    static String constr="jdbc:oracle:thin:@localhost:1521:xe";
    static String un="hr";
    static String pwd="hr";

     public static boolean executeq(string sql)
    {
     Connection con;
      Statement s;
      ResultSet rs;
                       try{
                                    class.forName(driver);
                                    con=DriverManager.getConnection(constr,un,pwd);
                                    s=con.createStatement();
	                 rs=s.executeQuery(sql);
		
			return rs;	
		}
		catch(Exception ex)
		{
			JOptionPane.showMessageDialog(null,"Error executing : \n"+sql+"\n"+ex);
			return null;
		}
	}

   public static ResultSet getResult(String sql)
	{
	Connection con;
	Statement s;
	ResultSet rs;
	
		try{
			Class.forName(driver);
			con=DriverManager.getConnection(constr,un,pwd);
			s=con.createStatement();
			rs=s.executeQuery(sql);
		
			return rs;	
		}
		catch(Exception ex)
		{
			JOptionPane.showMessageDialog(null,"Error executing : \n"+sql+"\n"+ex);
			return null;
		}
	}
	
	
	public static String getScalar(String sql)
	{
ResultSet rs;
		try
		{
			rs=getResult(sql);
			if(rs==null)
				return null;
			else if(rs.next()==false)
				return "";
			String p=rs.getString(1);
		
			return p;
		}
		catch(Exception ex)
		{
			JOptionPane.showMessageDialog(null,"Error executing : \n"+sql+"\n"+ex);
			return null;
		}
	}
}
