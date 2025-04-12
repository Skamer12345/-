	import java.util.ArrayList;
	public class Ship {
		
		private ArrayList<String> locationCells;
	    private int numOfHits;
	    
	    public void setLocationCells(ArrayList<String> location)
		{
			locationCells = location;
		}
	    
	    	public String checkYourself(String userGuess) {
			
			String result = "Мимо";
			
			int index = locationCells.indexOf(userGuess);
			
			if(index >= 0) {
				
				
				locationCells.remove(index);
				
				
				if(locationCells.isEmpty()) {
					result = "Потопил";
				}else {
					result = "Попал";
				}
			}
			
		
			return result;
		}
	}

