package day1puzzle1;

import java.io.FileReader;
import java.io.IOException;
import java.util.Locale;
import java.util.Scanner;
import java.util.regex.Pattern;
import java.util.Arrays;
import java.util.List;
import java.util.*;

public class Day1Puzzle1 {
	
	static Scanner scan = new Scanner(System.in);
	static int startx = 0;
	static int starty = 0;
	static int destinationx;
	static int destinationy;
	static int curx = startx;
	static int cury = starty;
	static char facing = 'N';
	static int moveval;
	static char movedir;
	static String Instruction;
	static int difx;
	static int dify;
	static int totalblocks;
	static int loops;
	static int haveVisited[][];
	static int coordinateArray[][];
	static String xCo;
	static String yCo;
	static String coordinates;
	static boolean solution2;
	
	public static 	List<String> haveVisitedList = new ArrayList<String>();
	
	//static int i = 0;
	
	
	

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		

		try (
				Scanner sc = new Scanner(
					new FileReader("C:\\Users\\darkl\\Desktop\\travelinput.txt"));	
						
				) {
			
					sc.useDelimiter(Pattern.compile("(, )|(\r\n)"));
					sc.useLocale(Locale.ENGLISH);
					
					while (sc.hasNext()) {
						loops++;
						Instruction = sc.next();
						movedir = Instruction.charAt(0);
						Instruction = Instruction.substring(1);
						moveval = Integer.parseInt(Instruction);
						
						if(facing == 'N')
						{
							//System.out.println("Loop #: " + loops + ". Started facing North.");
							if(movedir == 'L')
							{
								
								for(int i = 0; i<moveval; i++) {
									curx -= 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								//curx -= moveval;
								
								facing = 'W';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								
								//return;
							}
							 
							else if(movedir == 'R')
							{
								
								for(int i = 0; i<moveval; i++) {
									curx += 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'E';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								
								//return;julo
							}
							
						}
						
						
						else if(facing == 'S')
						{
							//System.out.println("Loop #: " + loops + ". Started facing South.");
							if(movedir == 'L')
							{
								for(int i = 0; i<moveval; i++) {
									curx += 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'E';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								//return;
							}
							
							else if(movedir == 'R')
							{
								for(int i = 0; i<moveval; i++) {
									curx -= 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'W';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								//return;
							}
							
						}
						
						else if(facing == 'E')
						{
							//System.out.println("Loop #: " + loops + ". Started facing East.");
							if(movedir == 'L')
							{
								for(int i = 0; i<moveval; i++) {
									cury -= 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'N';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								//return;
							}
							
							else if(movedir == 'R')
							{
								for(int i = 0; i<moveval; i++) {
									cury += 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'S';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								//return;
							}
							
						}
						
						else 
						{
							//System.out.println("Loop #: " + loops + ". Started facing West.");
							if(movedir == 'L')
							{
								for(int i = 0; i<moveval; i++) {
									cury += 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'S';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								//return;
							}
							
							else if(movedir == 'R')
							{
								for(int i = 0; i<moveval; i++) {
									cury -= 1;
									xCo = Integer.toString(curx);
									yCo = Integer.toString(cury);
									coordinates = (xCo+yCo);
									if(solution2 == false)
									Visited(coordinates, haveVisitedList);
									
								}
								
								facing = 'N';
								//System.out.println("Loop #: " + loops + ". " +Instruction + " Moved " + moveval + " blocks to the " + movedir + ". Now facing " + facing);
								//return;
							}
							
						}
						
					}
					
					
		}
					catch (IOException e) {
						
						e.printStackTrace();
					}
			
		scan.close();
		
		countBlocks(destinationx, destinationy);
		System.out.println("Solution 1: " + totalblocks);
		

	}
	
public static void Visited(String currentco, List<String> coordinateList) {
	
	
	currentco = coordinates;
	//System.out.println(coordinates);
	if(coordinateList.contains(currentco)) {
		//System.out.println("The coordinates of the actual HQ are: " + curx + " " + cury);
		countBlocks(curx, cury);
		System.out.println("Solution 2: " + totalblocks);
		solution2 = true;
	
		return;
	}
	
	else {
	haveVisitedList.add(coordinates);
	}
	
	
}



public static void countBlocks(int x, int y) {
	x = curx;
	y = cury;
	System.out.println("The destination is at coordinates " + curx + "X and " + cury + "Y.");
	x = Math.abs(x);
	y = Math.abs(y);
	
	
	if(x < startx)
	{
		startx -= x;
		difx = startx;
	}
	
	else if(x > startx)
	{
		x -= startx;
		difx = x;
	}
	
	if(y < starty)
	{
		starty -= y;
		dify = starty;	
	}
	
	else if(y > starty)
	{
		y -= starty;
		dify = y;
	}
	
	difx += dify;
	totalblocks = difx;
	
	
	return;
}

}
