package com.jdbcproject.www;

import java.util.ArrayList;
import java.util.Iterator;



public class TestMarksheetModel {

	public static void main(String[] args) throws Exception {
		// TODO Auto-generated method stub
		TestMarksheetModel md=new TestMarksheetModel();
		//md.testadd();
		//md.testupdate();
	    //md.testdelete();
		//md.testget();
	    md.testgetMerritlist();
		//md.testsearch();

	}
	

	
	public  void testadd() throws Exception {
		MarksheetBean bean = new MarksheetBean();
		bean.setId(10);
		bean.setRoll_no("CZ1010");
		bean.setFname("CHANDAN");
		bean.setLname("YADAV");
		bean.setPhysics(80);
		bean.setChemistry(66);
		bean.setMaths(90);

		MarksheetModel model = new MarksheetModel();
		model.add(bean);

	}

	public  void testupdate() throws Exception {
		MarksheetBean bean = new MarksheetBean();

		bean.setRoll_no("CZ1011");
		bean.setFname("TANU");
		bean.setLname("JHA");
		bean.setPhysics(77);
		bean.setChemistry(66);
		bean.setMaths(65);
		bean.setId(6);

		MarksheetModel model = new MarksheetModel();
		model.update(bean);
	}

	public void testdelete() throws Exception {
		MarksheetBean bean = new MarksheetBean();
        bean.setId(10);

		MarksheetModel model = new MarksheetModel();
		model.delete(bean);
	}

	public void testget() throws Exception {
		MarksheetBean bean=new MarksheetBean();
		bean.setRoll_no("CZ104");
		
		MarksheetModel model=new MarksheetModel();
		model.get(bean);
	}
	
	public  void testgetMerritlist() throws Exception{
			MarksheetModel model = new MarksheetModel();
			ArrayList<MarksheetBean> list=model.getmeritlist();
			
			Iterator<MarksheetBean> it =list.iterator();
			while (it.hasNext()) 
			{
				MarksheetBean mb = (MarksheetBean) it.next();
				System.out.print(mb.getId());
				System.out.print("\t"+mb.getRoll_no());
				System.out.print("\t"+mb.getFname());
				System.out.print("\t"+mb.getLname());
				System.out.print("\t"+mb.getPhysics());
				System.out.print("\t"+mb.getChemistry());
				System.out.println("\t"+mb.getMaths());
			}
				
			
		}
		
    public void testsearch() throws Exception {
    	MarksheetModel model = new MarksheetModel();
		ArrayList<MarksheetBean> list=model.getmeritlist();
		
		Iterator<MarksheetBean> it =list.iterator();
		while (it.hasNext()) 
		{
			MarksheetBean mb = (MarksheetBean) it.next();
			System.out.print(mb.getId());
			System.out.print("\t"+mb.getRoll_no());
			System.out.print("\t"+mb.getFname());
			System.out.print("\t"+mb.getLname());
			System.out.print("\t"+mb.getPhysics());
			System.out.print("\t"+mb.getChemistry());
			System.out.println("\t"+mb.getMaths());
		}

    	
    }

}
