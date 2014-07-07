===================
// Obinna Ozoalor

import javax.swing.*;

import java.awt.Color;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class Assignment15 extends JFrame {
	
	int R_amount = 0;
	int B_amount = 0;
	JPanel Textpanel, Numberpanel, Labelbuttons, resetpanel;
	JLabel redlabel, bluelabel, zero1, zero2;
	JButton Rbutton, Bbutton, Resetbutton;

	public Assignment15() {
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
	Textpanel = new JPanel();
	Textpanel.setLayout(null);
	Textpanel.setLocation(10, 0);
	Textpanel.setSize(320, 50);
	AllGUI.add(Textpanel);
	
	//Creation of the JLabel
	//1st JLabel
	redlabel = new JLabel("Red Team");
	redlabel.setLocation(30, 0);
	redlabel.setSize(60, 50);
	redlabel.setForeground(Color.red);
	redlabel.setHorizontalAlignment(0);
	Textpanel.add(redlabel);
	
	//2nd JLabel
	bluelabel = new JLabel("Blue Team");
	bluelabel.setLocation(210, 0);
	bluelabel.setSize(60, 50);
	bluelabel.setForeground(Color.blue);
	bluelabel.setHorizontalAlignment(0);
	Textpanel.add(bluelabel);
	
	//Creation of JPanel to place the next JLabel
	Numberpanel = new JPanel();
	Numberpanel.setLayout(null);
	Numberpanel.setLocation(10, 60);
	Numberpanel.setSize(320, 50);
	AllGUI.add(Numberpanel);
	
	//Creation of the JLabel
	//1st JLabel
	zero1 = new JLabel(""+R_amount);
	zero1.setLocation(30, 0);
	zero1.setSize(50, 50);
	zero1.setHorizontalAlignment(0);
	Numberpanel.add(zero1);
	
	//2nd JLabel
	zero2 = new JLabel(""+B_amount);
	zero2.setLocation(210, 0);
	zero2.setSize(50, 50);
	zero2.setHorizontalAlignment(0);
	Numberpanel.add(zero2);
	
	//Creation of JPanel to place the first two JButtons
	Labelbuttons = new JPanel();
	Labelbuttons.setLayout(null);
	Labelbuttons.setLocation(10, 110);
	Labelbuttons.setSize(320, 50);
	AllGUI.add(Labelbuttons);
	
	//Creation of the JButton
	//1st JButton
	Rbutton = new JButton("Red Score!");
	Rbutton.setLocation(10, 0);
	Rbutton.setSize(100, 30);
	Rbutton.addActionListener(new ButtonListener());
	Labelbuttons.add(Rbutton);
	
	//2nd JButton
	Bbutton = new JButton("Blue Score!");
	Bbutton.setLocation(190, 0);
	Bbutton.setSize(100, 30);
	Bbutton.addActionListener(new ButtonListener());
	Labelbuttons.add(Bbutton);
	
	//Creation of JPanel to place the last JButton
	resetpanel = new JPanel();
	resetpanel.setLayout(null);
	resetpanel.setLocation(10, 160);
	resetpanel.setSize(320, 50);
	AllGUI.add(resetpanel);
	
	//Creation of the JButtton
	Resetbutton = new JButton("Reset Score");
	Resetbutton.setLocation(10, 0);
	Resetbutton.setSize(280, 30);
	Resetbutton.addActionListener(new ButtonListener());
	resetpanel.add(Resetbutton);
	}

private class ButtonListener implements ActionListener {
public void actionPerformed(ActionEvent e) {
	
	if(e.getSource() == Rbutton) {
		R_amount = R_amount + 1;
		zero1.setText(""+R_amount);
	}
	else if(e.getSource() == Bbutton) {
		B_amount = B_amount + 1;
		zero2.setText(""+B_amount);
	}
	else if(e.getSource() == Resetbutton) {
		R_amount = 0;
		B_amount = 0;
		zero1.setText(""+R_amount);
		zero2.setText(""+B_amount);
	}
}
}

public static void main(String[] args) {
	 
	JFrame.setDefaultLookAndFeelDecorated(true);
	Assignment15 window = new Assignment15();	
}
}
