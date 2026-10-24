# 9.3
import java.sql.*; class JDBCDelete {public static void main(String[] args) throws Exception {Connection c=DriverManager.getConnection("jdbc:mysql://localhost:3306/college","root","password"); PreparedStatement p=c.prepareStatement("DELETE FROM student WHERE id=?");p.setInt(1,101); p.executeUpdate();System.out.println("Record deleted");c.close();}}
