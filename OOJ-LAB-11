import java.awt.*;
import java.awt.event.*;
class DivisionInteger extends Frame implements ActionListener{
    TextField num1TextField;
    TextField num2TextField;
    Button calculate;
    int a,b;
    float result;
    String msg="Enter the numbers";
    public DivisionInteger(){

        setLayout(new FlowLayout());

        calculate=new Button("Calculate");
        num1TextField=new TextField(5);
        Label num1Label=new Label("Number 1",Label.RIGHT);
        num2TextField=new TextField(5);
        Label num2Label=new Label("Number 2",Label.RIGHT);

        add(num1Label);
        add(num1TextField);
        add(num2Label);
        add(num2TextField);
        add(calculate);
        num1TextField.addActionListener(this);
        num2TextField.addActionListener(this);
        calculate.addActionListener(this);

        addWindowListener(new MyWindowAdapter());
    }
    public void actionPerformed(ActionEvent ae){
        try{
            result=divideNumbers();
            msg=("The result is "+result);
            repaint();
        }catch(NumberFormatException e){
            msg="Number is not Integer."+e;
            repaint();
        }catch(ArithmeticException e){
            msg="Divide By zero not Allowed."+e;
            repaint();
        }
    }
    public float divideNumbers(){
        a=Integer.parseInt(num1TextField.getText());
        b=Integer.parseInt(num2TextField.getText());
        if(b==0){
            throw new ArithmeticException();
        }
        return (float)a/b;
    }
    public void paint(Graphics g){
        g.drawString(msg,50,100);
    }
    public static void main(String args[]){
        DivisionInteger div=new DivisionInteger();
        div.setSize(new Dimension(500,500));
        div.setTitle("Division Calculater");
        div.setVisible(true);
    }
}
class MyWindowAdapter extends WindowAdapter{
    public void windowClosing(WindowEvent event){
        System.exit(0);
    }
}
