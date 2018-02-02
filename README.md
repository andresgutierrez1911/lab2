# lab2

import java.awt.Polygon;
import java.awt.Rectangle;
import java.util.Scanner;

public class intersection {

	public static void main(String[] args) {
		
		Scanner keyboard = new Scanner(System.in);
		
		int x1,y1,x2,y2,x3,y3,x4,y4,x5,y5;
		
		System.out.print("What are the vertices of the 5 sided polygon?");
		x1 = keyboard.nextInt();
		y1 = keyboard.nextInt();
		x2 = keyboard.nextInt();
		y2 = keyboard.nextInt();
		x3 = keyboard.nextInt();
		y3 = keyboard.nextInt();
		x4 = keyboard.nextInt();
		y4 = keyboard.nextInt();
		x5 = keyboard.nextInt();
		y5 = keyboard.nextInt();
		
		
		Polygon poly = new Polygon();
		poly.addPoint(x1, y1);
		poly.addPoint(x2, y2);
		poly.addPoint(x3, y3);
		poly.addPoint(x4, y4);
		poly.addPoint(x5, y5);
		
		
		int x, y, width, height;
		
	
		System.out.print("Please specify a rectangle (x,y,w,h):");
		x = keyboard.nextInt();
		y = keyboard.nextInt();
		width = keyboard.nextInt();
		height = keyboard.nextInt();
		
		Rectangle myRect = new Rectangle(x, y, width, height);
		myRect.add(x,y);
		myRect.add(width,height);
		
		
	
			if (poly.intersects(x, y, width, height)){
				System.out.print("It is true that the polygon and rectangle intersects");}
				else { 
				System.out.print("It is not true that the polygon and rectangle intersects");}
			keyboard.close();
	}
}

