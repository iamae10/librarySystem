import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class LibrarySystemGUI extends JFrame implements ActionListener {
	
    // GUI components
    private JLabel usernameLabel, passwordLabel;
    private JTextField usernameField;
    private JPasswordField passwordField;
    private JButton loginButton, adminButton, librarianButton;
    
     
    public  LibrarySystemGUI() {
    	
        // Set the title and size of the window
        setTitle("NU Library System");
        setSize(400, 200);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        
        // Create the GUI components
        usernameLabel = new JLabel("Username:");
        passwordLabel = new JLabel("Password:");
        usernameField = new JTextField(20);
        passwordField = new JPasswordField(20);
        loginButton = new JButton("Login");

        
        // Add the components to the window
        JPanel panel = new JPanel(new GridLayout(3, 2));
        panel.add(usernameLabel);
        panel.add(usernameField);
        panel.add(passwordLabel);
        panel.add(passwordField);
        panel.add(new JLabel(""));
        panel.add(loginButton);
        add(panel);

        // Register the login button to handle clicks
        loginButton.addActionListener(this);
        
        // Show the window
        setVisible(true);
    }

    public void actionPerformed(ActionEvent e) {
        String username = usernameField.getText();
        String password = new String(passwordField.getPassword());

        // Check if the user is an admin
        if (username.equals("Admin_01") && password.equals("AdminOne") ||
            username.equals("Admin_02") && password.equals("AdminTwo") ||
            username.equals("Admin_03") && password.equals("AdminThree")) {
            // Redirect to welcome screen for admin
            WelcomeScreen welcomeScreen = new WelcomeScreen("Admin");
            welcomeScreen.setVisible(true);
            dispose(); // Close the login screen
            
          JFrame  bookFrame = new JFrame("Book Rental");
            bookFrame.setSize(500, 400);
            bookFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
            bookFrame.setLocationRelativeTo(null);
            bookFrame.setLayout(null);
            
           
        }
        // Check if the user is a librarian
        else if (username.equals("Librarian_01") && password.equals("LibOne") ||
                 username.equals("Librarian_02") && password.equals("LibTwo") ||
                 username.equals("Librarian_03") && password.equals("LibThree")) {
            // Redirect to welcome screen for librarian
            WelcomeScreen welcomeScreen = new WelcomeScreen("Librarian");
            welcomeScreen.setVisible(true);
            dispose(); // Close the login screen
        }
        // Display an error message for invalid username/password
        else {
            JOptionPane.showMessageDialog(this, "Invalid username or password");
        }
    }

    public static void main(String[] args) {
        // Create a new login screen
        new LibrarySystemGUI();
    }
}

class WelcomeScreen extends JFrame {
    // GUI components
    private JLabel welcomeLabel;

    public WelcomeScreen(String userType) {
        // Set the title and size of the window
        setTitle("NU Library System - Welcome");
        setSize(400, 200);
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        // Create the GUI components
        welcomeLabel = new JLabel("Welcome to NU Library System, " + userType + "!");
        JPanel panel = new JPanel(new GridLayout(1, 1));
        panel.add(welcomeLabel);
        add(panel);

        // Show the window
        setVisible(true);
        
        
    }
}

