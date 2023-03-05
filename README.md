# test para conectar servidor mysqlserver

import java.sql.*;

public class Main {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/mydb";
        String username = "root";
        String password = "password";

        try {
            Connection connection = DriverManager.getConnection(url, username, password);
            System.out.println("Connected to the database!");

            Statement statement = connection.createStatement();
            String sql = "SELECT * FROM users";
            ResultSet
