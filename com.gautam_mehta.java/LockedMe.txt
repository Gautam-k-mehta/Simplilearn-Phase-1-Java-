package com.gautam_mehta.java;

import java.io.File;
import java.io.IOException;
import java.util.Arrays;
import java.util.Scanner;

public class LockedMe {
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		LockedMe C = new LockedMe();
		C.crown_method();
		System.out.println("      **LockedMe.com***" + "\n" + "      *****************" + "\n" + "       -Developed By Gautam");
		Scanner s = new Scanner(System.in);
		System.out.println("\n" + "Enter your name to access the menu");
		String name = s.next();
		System.out.println("Hello " + name + "\n" + "Welcome to Lockedme.com. Please enter an input");
		LockedMe M = new LockedMe();
		M.Mainmenu();
		s.close();
	}
	
	  private void Mainmenu() {
		System.out.println("**************Main Menu*************" + "\n" + "Enter 1 to show files in ascending orders in a directory" + "\n" + "Enter 2 for file Manager" + "\n" + "Enter 3 to close the application");
		
		try {
			Scanner s1 = new Scanner (System.in);
		Integer input2 = s1.nextInt();
		//try {
		switch (input2){
		case 1: {
			showFiles();
		}
			//break;
		case 2: {
		filemanager2();
		}
		    //break;
		case 3: {
			System.out.println("Program has been Closed");
			System.exit(input2);
			//break;
		} } }
		catch(Exception e) {
			System.out.println("Please enter a valid input");
			Mainmenu();
		}
		}

	 File folder_name;
	private void showFiles() {
		try {
		System.out.println("Enter path");
		Scanner sf = new Scanner(System.in);
		String path1 = sf.nextLine();
		File f = new File(path1);
	String[] showfile = f.list();
	Arrays.sort(showfile);
	for (String pathname:showfile) {
	System.out.println(pathname + "\n");
	}
	//sf.close(); it keeps repeating the execution
		}
		catch(Exception e) {
	System.out.println("File not found\n\n");
		}
	Mainmenu();
        }
	
	private void filemanager2() {
		System.out.println("Enter 1 to create a file" + "\n" + "Enter 2 for delete the file" + "\n" + "Enter 3 to search the file" + "\n" + "Enter 4 to Go back to main menu");
	Scanner i = new Scanner(System.in); //User input
	Integer input = i.nextInt(); //Store input to "input" variable
	//i.close(); it keeps repeating the execution
	try {
	switch (input){
		case 1:
			System.out.println("Enter filename");
			Scanner j = new Scanner(System.in);
			String file1 = j.nextLine().trim().toLowerCase();
			 try {
			      File myObj = new File(file1);
			      myObj.createNewFile();
			        System.out.println("File created: " + myObj.getName()+"\n"); //file created
			        filemanager2();
			      } catch (Exception e) {
			        System.out.println("Invalid file path or name");
			       // e1.printStackTrace();
			        filemanager2();
			      }
			break;
		case 2:
			System.out.println("Enter filename");
			Scanner k = new Scanner(System.in);
			String file2 = k.nextLine();
			File f = new File(file2);
			boolean bool1 = f.exists();
			if (bool1 == true) {
			File myObj = new File(file2);
		  myObj.delete();
		    System.out.println("File deleted: " + myObj.getName()); //file created
		    filemanager2();
	} else {
		System.out.println("File not found");
		filemanager2();
	}
			break;
		case 3:
			Scanner sf = new Scanner(System.in);
			System.out.println("Enter path");
			String path1 = sf.nextLine();
			System.out.println("Enter filename");
			String searchfile = sf.nextLine();
			File f1 = new File(path1);
		String[] showfile = f1.list();
		System.out.println("search results:\n");
		for (String pathname:showfile) {
			if(pathname.contains(searchfile)) {
		System.out.println(pathname + "\n");
	        }
		}
		case 4:
			Mainmenu(); 
	}
	}
	catch (Exception e) {
		System.out.println("Please Enter a valid input");
		Mainmenu();
	}
	}
	
	private void crown_method(){
		{
			
			{
		     for(int i=1; i<=5; i++)
		     {
		         for(int k=1; k<=i; k++)
		          {
		             System.out.print(" ");
		        } 
		        for(int j=1; j<=i; j++)
		        {
		            System.out.print("*");
		        } 
		        for(int k=1; k<=3*(4-i+1); k++)
		        {
		            System.out.print(" ");
		        } 
		        for(int j=1; j<=2*i-1; j++)
		        {
		            System.out.print("*");
		        } 
		        for(int k=1; k<=3*(4-i+1); k++)
		        {
		            System.out.print(" ");
		        } 
		        for(int j=1; j<=i; j++)
		        {
		            System.out.print("*");
		         } 
		         System.out.println();
		     }
		    for(int i=1; i<=2; i++)
		    {
		        for(int k=1; k<=5+i-1; k++)
		       {
		           System.out.print(" ");
	        } 
		         for(int j=1; j<=2*(9-i+1)+1; j++)
		        {
		            System.out.print("*");
		        } 
		         System.out.println();
		     }
		}
	}
	}
}

