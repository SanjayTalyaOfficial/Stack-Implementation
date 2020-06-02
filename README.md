# Stack-Implementation
Implementation of Stack using linkedlist

// The below code can be implemented in either Eclipse IDE or in NetBeans.
import java.util.Scanner;
public class Stack_pgm
{
	
	Node head;
	class Node
	{
		int data;
		Node next;
		
		Node(int n)
		{
			data = n;
			next = null;
		}
	}
	
	public void push_element(int x)
	{
		Node new_node = new Node(x);
		if(head == null)
		{
			head = new_node;
		}
		else
		{
			new_node.next = head;
			head = new_node;
		}
	}
	
	public void peek_element()
	{
		if(head == null)
		{
			System.out.println("Stack is empty");
		}
		else
		{
			System.out.println(head.data);
		}
	}
	
	public void display()
	{
		Node temp = head;
		while(temp != null)
		{
			System.out.println(temp.data);
			temp = temp.next;
		}
	}
	
	public void pop_element()
	{
		if(head == null)
		{
			System.out.println("Stack is empty / Underflow condition / Deletion is not possible");
		}
		else
		{
			Node temp = head;
			head = temp.next;
			//head = head.next;
			
		}
	}
	
	public static void main(String[] args)
	{
		Scanner sc = new Scanner(System.in);
		Stack_pgm sp = new Stack_pgm();
		int n = sc.nextInt();
		int i;
		for(i = 1; i <= n; i++)
		{
			int x = sc.nextInt();
			sp.push_element(x);
		}
		
		System.out.println("Peek element / Top element of the stack");
		sp.peek_element();
		
		System.out.println("Display the elements of the stack before deletion");
		sp.display();
		System.out.println("Delete the element from the stack");
		sp.pop_element();
		
		System.out.println("Display the elements of the stack after deletion");
		sp.display();
	}
}

//The program can be compiled post this stage. 
