import javax.swing.*;
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.net.InetAddress;
import java.net.UnknownHostException;

public class IpFinder {
    public static void main(String[] args) {

        JFrame jFrame = new JFrame("IP Finder Program");
        jFrame.setSize(300, 200);
        jFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JPanel panel = new JPanel();
        panel.setLayout(null);

        // IP Finder Program
        JLabel label = new JLabel("Enter URL: ");
        label.setBounds(20, 30, 80, 20);

        JTextField textField = new JTextField();
        textField.setBounds(100, 30, 150, 20);

        JButton button = new JButton("Find IP");
        button.setBounds(100, 70, 100, 30);

        JLabel resultLabel = new JLabel("");
        resultLabel.setBounds(20, 110, 250, 20);

        button.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                String url = textField.getText();
                try {
                    InetAddress ia = InetAddress.getByName(url);
                    String ip = ia.getHostAddress();
                    resultLabel.setText("IP Address: " + ip);
                } catch (UnknownHostException unknownHostException) {
                    resultLabel.setText("Unable to find IP address for the specified domain: " + url);
                    unknownHostException.printStackTrace();
                }
            }
        });

        panel.add(textField);
        panel.add(label);
        panel.add(button);
        panel.add(resultLabel);

        jFrame.add(panel);
        jFrame.setVisible(true);
    }
}
