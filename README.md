package com.movies;

import java.sql.*;

public class MovieTable {

	public static void main(String[] args) throws SQLException {
		Connection con =DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe","uday","udaykumar");
		System.out.println("connection established");
		Statement st = con.createStatement();
		String cmd = "CREATE TABLE MOVIES(MOVIE_NAME VARCHAR2(50),LEAD_ACTOR VARCHAR2(50), ACTRESS VARCHAR2(50),YEAR_OF_RELEASE NUMBER(4), DIRECTOR VARCHAR2(50))";
		int i = st.executeUpdate(cmd);
		st.close();
		con.close();
		
		

	}

}






package com.movies;

import java.sql.*;

public class MovieData {

	public static void main(String[] args) throws SQLException {
	    Connection con =DriverManager.getConnection("jdbc:oracle:thin:@localhost:1521:xe","uday","udaykumar");
	    Statement st =con.createStatement();
	    System.out.println("statement called");
	    String cmd1 ="INSERT INTO MOVIES VALUES('BAHUBALI','PRABHAS','THAMANNAH',2015,'RAJAMOULI')";
	    int i =st.executeUpdate(cmd1);
	    String cmd2 ="INSERT INTO MOVIES VALUES('SAAHO','PRABHAS','SHRADDHA KAPOOR',2019,'SUJEETH')";
	    int J =st.executeUpdate(cmd2);
	    String cmd3 ="INSERT INTO MOVIES VALUES('RAGHU VARAN B-TECH','DHANUSH','AMALA PAUL',2014,'R.VELRAJ')";
	    int k =st.executeUpdate(cmd3);
	    String cmd4 ="INSERT INTO MOVIES VALUES('SARAINODU','ALLU ARJUN','RAKUL PREET SINGH',2016,'BOYAPATI SREENU')";
	    int l =st.executeUpdate(cmd4);
	    System.out.println("data inserted successfully");
	    

	}

}
