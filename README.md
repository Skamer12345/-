import java.io.*;
import java.util.*;
public class Helper {

	private static final String alphabet = "abcdefg";
	private int gridLenght = 7;
	private int gridSize = 49;
	private int [] grid = new int[gridSize];
	private int shCount = 0;
	
	public String getUserInput(String prompt) {
		String inputLine = null;
		System.out.print(prompt + " ");
		try {
			BufferedReader is = new BufferedReader(new InputStreamReader(System.in));
			inputLine = is.readLine();
			if(inputLine.length() == 0 ) return null;
			
		} catch (IOException e) {
			System.out.println("IOException: " + e);
		}
		return inputLine.toLowerCase();

	}
	
	public ArrayList<String> placeDotCom(int shSize) {
		ArrayList<String> alphaCells = new ArrayList<String>();
		String [] alphacoords = new String [shSize];
		String temp = null;
		int [] coords = new int[shSize];
		int attempts = 0;
		boolean success = false;
		int location = 0;
		
		shCount++;
		int incr = 1;
		if ((shCount % 2) == 1) {
			incr = gridLenght;
		}
		
		return alphaCells;
	}

}
