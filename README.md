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
