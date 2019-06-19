
#Stack Datastructer

import java.util.*;
public class Stack {
    
    private int top=-1;
    private int n;
    private int []a=new int[20];
    public static void main(String[] args) {
        Stack e=new Stack();
        e.choice();
        
    }
    
    public void choice()
    {
        while(true)
        {
        
        Scanner sc=new Scanner(System.in);
        System.out.println("\n1. Push\n2. Pop\n3. Top\n4. Display \n5. Exit");
        int ch=sc.nextInt();
        
        switch(ch)
        {
            case 1:
              System.out.println("Enter the element: ");
              int a=sc.nextInt();
              push(a);
              break;
            case 2:
                pop();
                break;

            case 3:
                top();
                break;
            case 4:
                display();
                break;

            case 5: 
                System.exit(-1);
                
            default : 
                System.out.println("Wrong choice");
                    
                 
        }

        }
    }
    public void push(int x)
    {
        top++;
        a[top]=x;
        System.out.println("Data inserted");
    }

    public void pop()
    {
        if(top==-1)
            System.out.println("The stack is empty can't pop");
        else
        {
            top--;
            System.out.println("The element poped");
        }
    }
    public void top()
    {
        System.out.println("The top element is: "+a[top]);
    }

    public void display()
    {
        if(top==-1)
            System.out.println("Stack is empty");
        else
        for(int i=0;i<=top;i++)
        {
            System.out.print(" "+a[i]);
        }
    }
}
