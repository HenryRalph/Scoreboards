============
*Scoreboard without listener*

import javax.swing.*;
import java.awt.Color;

public class Assignment6 {
public static void main(String[] args) {
	
	JFrame.setDefaultLookAndFeelDecorated(true);
	
	JFrame window = new JFrame();
	window.setTitle("JButton Scoreboard");
	window.setSize(350, 250);
	window.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
	window.setVisible(true);
	
	//Creation of bottom panel to place everything on
	JPanel AllGUI = new JPanel();
	AllGUI.setLayout(null);
	window.add(AllGUI);
	
	//Creation of JPanel to Place initial JLabel
	JPanel Textpanel = new JPanel();
	Textpanel.setLayout(null);
	Textpanel.setLocation(10, 0);
	Textpanel.setSize(320, 50);
	AllGUI.add(Textpanel);
	
	//Creation of the JLabel
	//1st JLabel
	JLabel redlabel = new JLabel("Red Team");
	redlabel.setLocation(30, 0);
	redlabel.setSize(60, 50);
	redlabel.setForeground(Color.red);
	redlabel.setHorizontalAlignment(0);
	Textpanel.add(redlabel);
	
	//2nd JLabel
	JLabel bluelabel = new JLabel("Blue Team");
	bluelabel.setLocation(210, 0);
	bluelabel.setSize(60, 50);
	bluelabel.setForeground(Color.blue);
	bluelabel.setHorizontalAlignment(0);
	Textpanel.add(bluelabel);
	
	//Creation of JPanel to place the next JLabel
	JPanel Numberpanel = new JPanel();
	Numberpanel.setLayout(null);
	Numberpanel.setLocation(10, 60);
	Numberpanel.setSize(320, 50);
	AllGUI.add(Numberpanel);
	
	//Creation of the JLabel
	//1st JLabel
	JLabel zero1 = new JLabel("0");
	zero1.setLocation(30, 0);
	zero1.setSize(50, 50);
	zero1.setHorizontalAlignment(0);
	Numberpanel.add(zero1);
	
	//2nd JLabel
	JLabel zero2 = new JLabel("0");
	zero2.setLocation(210, 0);
	zero2.setSize(50, 50);
	zero2.setHorizontalAlignment(0);
	Numberpanel.add(zero2);
	
	//Creation of JPanel to place the first two JButtons
	JPanel Labelbuttons = new JPanel();
	Labelbuttons.setLayout(null);
	Labelbuttons.setLocation(10, 110);
	Labelbuttons.setSize(320, 50);
	AllGUI.add(Labelbuttons);
	
	//Creation of the JButton
	//1st JButton
	JButton Rbutton = new JButton("Red Score!");
	Rbutton.setLocation(10, 0);
	Rbutton.setSize(100, 30);
	Labelbuttons.add(Rbutton);
	
	//2nd JButton
	JButton Bbutton = new JButton("Blue Score!");
	Bbutton.setLocation(190, 0);
	Bbutton.setSize(100, 30);
	Labelbuttons.add(Bbutton);
	
	//Creation of JPanel to place the last JButton
	JPanel resetpanel = new JPanel();
	resetpanel.setLayout(null);
	resetpanel.setLocation(10, 160);
	resetpanel.setSize(320, 50);
	AllGUI.add(resetpanel);
	
	//Creation of the JButtton
	JButton Resetbutton = new JButton("Reset Score");
	Resetbutton.setLocation(10, 0);
	Resetbutton.setSize(280, 30);
	resetpanel.add(Resetbutton);
}
}
