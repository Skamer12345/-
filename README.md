public class Game {
	
	public static void main(String[] args) {
		Helper helper = new Helper();
		 int numOfGuesses = 0;
		int firstCord =   (int)(Math.random() * 5 ) ;
		Ship ship = new Ship();
		int location[] = {firstCord,firstCord+1,firstCord+2} ;
		ship.setLocationCells(location);
		boolean isAlive = true;
		
		while(isAlive) {
			String guess = helper.getUserInput("Введите число") ;
			String result=ship.checkYourself(guess);
			numOfGuesses++;
			
			if(result.equals("Потопил")) {	
				isAlive = false;
				System.out.println("Вам потребовалось " + numOfGuesses + " попыток!");
			}
			
		}
			
	    }
	}

