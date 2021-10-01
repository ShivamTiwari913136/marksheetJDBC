package com.oopl.www;



public class Account {
	
	private String name;
	private String number;
	private String type;
	private double balance;
	
	public Account(String name,String number,String type,double balance) {
		this.name=name;
		this.number=number;
		this.type=type;
		this.balance=balance;
	}
		public void showAccountDetails(String accountNo) {
		if(this.number==accountNo) {
			System.out.println("Account Holder Name : "+this.name);
			System.out.println("Account Number : "+this.number);
			System.out.println("Account Type : "+this.type);
			System.out.println("Account Balance : "+this.balance);
		}
	}
		
	public void deposit(double amount) {
		this.balance=balance+amount;
	}
	
	public void withdrawal(double amount) {
		if(this.balance>amount) {
			this.balance=this.balance-amount;
		}else {
			System.out.println("Insufficient Fund");
			return;
		}
	}
	
	public static void fundTransfer(Account source,Account destination,double amount) {
		if(source.balance<amount) {
			System.out.println("Insufficient Fund");
			return;
		}
		source.withdrawal(amount);
		destination.deposit(amount);
	}
	


}
