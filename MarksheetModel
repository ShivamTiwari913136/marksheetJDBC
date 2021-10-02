package com.jdbcproject.www;

import java.sql.*;
import java.util.ArrayList;
import java.util.ResourceBundle;

public class MarksheetModel {
	
	public static void add(MarksheetBean bean) throws Exception{
		ResourceBundle rb=ResourceBundle.getBundle("com.javaResourceBundle.www.app");
    	Class.forName(rb.getString("driver"));
		Connection conn =DriverManager.getConnection(rb.getString("url"), rb.getString("user"), rb.getString("passwd"));
			 conn.setAutoCommit(false);
			try {
			PreparedStatement ps = conn.prepareStatement("insert into marksheet values(?,?,?,?,?,?,?)");
			ps.setInt(1, bean.getId());
			ps.setString(2, bean.getRoll_no());
			ps.setString(3, bean.getFname());
			ps.setString(4, bean.getLname());
			ps.setInt(5, bean.getPhysics());
			ps.setInt(6, bean.getChemistry());
			ps.setInt(7, bean.getMaths());
		
			ps.executeUpdate();
			System.out.println("Inserted");
			
			conn.commit();
			ps.close();
			}
			catch(SQLException e)
			{
				conn.rollback();
			}
			
			conn.close();
		
	  }
	  
	public static void update(MarksheetBean bean) throws Exception{
		ResourceBundle rb=ResourceBundle.getBundle("com.javaResourceBundle.www.app");
    	Class.forName(rb.getString("driver"));
		Connection conn =DriverManager.getConnection(rb.getString("url"), rb.getString("user"), rb.getString("passwd"));		conn.setAutoCommit(false);
		PreparedStatement ps = conn.prepareStatement("update marksheet set Roll_no=?, fname=?,lname=?,physics=?,chemistry=?,maths=? where id =?");
		try
		{
		ps.setString(1, bean.getRoll_no());
		ps.setString(2, bean.getFname());
		ps.setString(3, bean.getLname());
		ps.setInt(4, bean.getPhysics());
		ps.setInt(5, bean.getChemistry());
		ps.setInt(6, bean.getMaths());
		ps.setInt(7, bean.getId());
		
		ps.execute();
		System.out.println("updated");
		conn.commit();
		conn.close();
		ps.close();
		
		}
		catch(SQLException e)
		{
			conn.rollback();
		}
	  }
	  
    public static void delete(MarksheetBean bean) throws Exception{
    	ResourceBundle rb=ResourceBundle.getBundle("com.javaResourceBundle.www.app");
    	Class.forName(rb.getString("driver"));
		Connection conn =DriverManager.getConnection(rb.getString("url"), rb.getString("user"), rb.getString("passwd"));		conn.setAutoCommit(false);
		PreparedStatement ps = conn.prepareStatement("delete from marksheet where id=?");
		try {
		ps.setInt(1, bean.getId());
		
		ps.execute();
		System.out.println("Deleted");
		conn.commit();
		conn.close();
		ps.close();
		
		}
		
		catch(SQLException e)
		{
			conn.rollback();
		}
	  }

    public static void get(MarksheetBean bean) throws Exception {
    	ResourceBundle rb=ResourceBundle.getBundle("com.javaResourceBundle.www.app");
    	Class.forName(rb.getString("driver"));
		Connection conn =DriverManager.getConnection(rb.getString("url"), rb.getString("user"), rb.getString("passwd"));
		conn.setAutoCommit(false);
		PreparedStatement ps=conn.prepareStatement("Select * from Marksheet where Roll_No=?");
		try {
		ps.setString(1, bean.getRoll_no());
		ResultSet rs=ps.executeQuery();
		while(rs.next()) {
			System.out.print(rs.getInt(1));
			System.out.print("\t"+rs.getString(2));
			System.out.print("\t"+rs.getString(3));
			System.out.print("\t"+rs.getString(4));
			System.out.print("\t"+rs.getInt(5));
			System.out.print("\t"+rs.getInt(6));
			System.out.print("\t"+rs.getInt(7));
        }
		conn.commit();
		conn.close();
		ps.close();
		}catch(SQLException e) {
			conn.rollback();
		}
		
    }
   
    public  ArrayList<MarksheetBean> getmeritlist() throws Exception{
    	ResourceBundle rb=ResourceBundle.getBundle("com.javaResourceBundle.www.app");
    	Class.forName(rb.getString("driver"));
		Connection conn =DriverManager.getConnection(rb.getString("url"), rb.getString("user"), rb.getString("passwd"));
		PreparedStatement ps = conn.prepareStatement("select *,(Physics+Chemistry+Maths) as Total , (Physics+Chemistry+Maths)/3 as Percentage from marksheet where (Physics>30 And Chemistry>30 And Maths>30) order by Percentage desc limit 0,5");
		ResultSet rs =ps.executeQuery();
		
		ArrayList<MarksheetBean> list= new ArrayList<MarksheetBean>();
		while(rs.next())
		{
		MarksheetBean bean=new MarksheetBean();
		 bean.setId(rs.getInt("id"));
		bean.setRoll_no(rs.getString("roll_no"));
		bean.setFname(rs.getString("fname"));
		bean.setLname(rs.getString("lname"));
		bean.setPhysics(rs.getInt("physics"));
		bean.setChemistry(rs.getInt("chemistry"));
		bean.setMaths(rs.getInt("maths"));
		list.add(bean);
		}
		
		rs.close();
		conn.close();
		
		return list;
	}
    
    public ArrayList<MarksheetBean> search() throws Exception{
    	ResourceBundle rb=ResourceBundle.getBundle("com.javaResourceBundle.www.app");
    	Class.forName(rb.getString("driver"));
		Connection conn =DriverManager.getConnection(rb.getString("url"), rb.getString("user"), rb.getString("passwd"));
		PreparedStatement ps = conn.prepareStatement("select * from marksheet ");
		ResultSet rs =ps.executeQuery();
		
		ArrayList<MarksheetBean> list= new ArrayList<MarksheetBean>();
		while(rs.next())
		{
		MarksheetBean bean=new MarksheetBean();
		 bean.setId(rs.getInt("id"));
		bean.setRoll_no(rs.getString("roll_no"));
		bean.setFname(rs.getString("fname"));
		bean.setLname(rs.getString("lname"));
		bean.setPhysics(rs.getInt("physics"));
		bean.setChemistry(rs.getInt("chemistry"));
		bean.setMaths(rs.getInt("maths"));
		list.add(bean);
		}
		
		rs.close();
		conn.close();
		
		return list;
    }
	 
	
		
	


}
