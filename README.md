# librarySystem
import javax.swing.*;
import javax.swing.border.EmptyBorder;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.print.Book;

public class LibrarySystemGUI extends JFrame implements ActionListener {
	
    public LibrarySystemGUI() {
        
    	setTitle("NU LIBRARY SYSTEM");
		setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		setBounds(100, 100, 450, 300);
		JPanel panel1= new JPanel();
		panel1.setBorder(new EmptyBorder(5, 5, 5, 5));
		setContentPane(panel1);
		panel1.setLayout(null);
		
		JLabel label1 = new JLabel("NU LIBRARY SYSTEM");
		label1.setFont(new Font("Tahoma", Font.BOLD, 20));
		label1.setToolTipText("");
		label1.setHorizontalAlignment(SwingConstants.TRAILING);
		label1.setBounds(-13, 25, 344, 29);
		panel1.add(label1);
		
		
		JButton adminButton = new JButton("Admin");
		adminButton.setFont(new Font("Tahoma", Font.PLAIN, 15));
		adminButton.setBounds(160, 98, 89, 23);
		panel1.add(adminButton);
		adminButton.addActionListener(new ActionListener() {
			
	
				JFrame frame2 = new JFrame("LOGIN");
				setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
				setBounds(100, 100, 450, 300);
				JPanel panel2 = new JPanel();
				panel2.setBorder(new EmptyBorder(5, 5, 5, 5));

				setContentPane(panel2);
				panel2.setLayout(null);
				
				JLabel usernameLabel1 = new JLabel("Username:");
				usernameLabel1.setFont(new Font("Verdana", Font.BOLD, 12));
				usernameLabel1.setBounds(71, 70, 79, 14);
				panel2.add(usernameLabel1);
				
				JLabel passwordLabel1 = new JLabel("Password:");
				 passwordLabel1.setFont(new Font("Verdana", Font.BOLD, 12));
				 passwordLabel1.setBounds(71, 101, 79, 14);
				panel2.add(passwordLabel1);
				
				JButton LoginButton1 = new JButton("Login");
				LoginButton1.setBounds(157, 137, 89, 23);
				panel2.add(LoginButton1);
				
				JTextField usernametextfield1 = new JTextField();
				usernametextfield1.setBounds(160, 68, 86, 20);
				panel2.add(usernametextfield1);
				usernametextfield1.setColumns(10);
				String username1 = usernametextfield1.getText();
				
				JTextField passwordtextfield1 = new JTextField();
				passwordtextfield1.setBounds(160, 98, 86, 20);
				panel2.add(passwordtextfield1);
				passwordtextfield1.setColumns(10);
				
			
				
		});

		
		JButton librarianButton = new JButton("Librarian");
		librarianButton.setFont(new Font("Tahoma", Font.PLAIN, 15));
		librarianButton.setBounds(160, 132, 89, 23);
		panel1.add(librarianButton);
		
		librarianButton.addActionListener(new ActionListener() {
			public void actionPerformed2(ActionEvent e2) {
				JFrame frame3 = new JFrame("LOGIN");
				setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
				setBounds(100, 100, 450, 300);
				JPanel panel3 = new JPanel();
				panel3.setBorder(new EmptyBorder(5, 5, 5, 5));

				setContentPane(panel3);
				panel3.setLayout(null);
				
				JLabel usernameLabel2 = new JLabel("Username:");
				usernameLabel2.setFont(new Font("Verdana", Font.BOLD, 12));
				usernameLabel2.setBounds(71, 70, 79, 14);
				panel3.add(usernameLabel2);
				
				JLabel passwordLabel2 = new JLabel("Password:");
				 passwordLabel2.setFont(new Font("Verdana", Font.BOLD, 12));
				 passwordLabel2.setBounds(71, 101, 79, 14);
				panel3.add(passwordLabel2);
				
				JButton LoginButton2 = new JButton("Login");
				LoginButton2.setBounds(157, 137, 89, 23);
				panel3.add(LoginButton2);
				
				JTextField usernametextfield2 = new JTextField();
				usernametextfield2.setBounds(160, 68, 86, 20);
				panel3.add(usernametextfield2);
				usernametextfield2.setColumns(10);
				String username2 = usernametextfield2.getText();
				
				JTextField passwordtextfield2 = new JTextField();
				passwordtextfield2.setBounds(160, 98, 86, 20);
				panel3.add(passwordtextfield2);
				passwordtextfield2.setColumns(10);
				String password2 = passwordtextfield2.getText();
                 
			}


		public static void main(String[] args) {
			new LibrarySystemGUI();
		}
	}
