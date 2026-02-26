using System;

class GameSuite
{
	static Random rand = new Random(); 					
	static void Main(string[] args) 					
	{
		bool running = true;				 
		while (running)							
		{
			Console.WriteLine("-----------------------------------");
			Console.WriteLine("Game Menu");
			Console.WriteLine("-----------------------------------");
			Console.WriteLine("knots and crosses press 1");
			Console.WriteLine("-----------------------------------");
			Console.WriteLine("Scissors Paper Rock press 2");
			Console.WriteLine("----------------------------------");
			Console.WriteLine("Exit press 3");
			Console.WriteLine("----------------------------------");
			string choice = Console.ReadLine(); 				
			switch (choice) 							
			{
				case "1":
					PlayNC();
					break;
				case "2":
					PlayRPS();
					break;
				case "3":
					running = false; 		
					break;
				default: 				
					Console.WriteLine("Invalid key entered press following (1,2,3)");
					break;
			}
		}

		static void PlayNC()
		{
			
			
	string[] board = {"1", "2", "3", "4", "5", "6", "7", "8", "9"};
	
	string player = "X"; 
	bool gameRunning = true;

	while (gameRunning == true)
	{
		// elements manually to show the board
		Console.WriteLine("\n " + board[0] + " | " + board[1] + " | " + board[2]);
		Console.WriteLine("---+---+---");
		Console.WriteLine(" " + board[3] + " | " + board[4] + " | " + board[5]);
		Console.WriteLine("---+---+---");
		Console.WriteLine(" " + board[6] + " | " + board[7] + " | " + board[8]);

		Console.WriteLine("Player " + player + ", type a number:");
		string input = Console.ReadLine();

		
		int index = int.Parse(input) - 1; 
		board[index] = player; // places x or o

		// 4. Checking for a win
		bool win = false;
		// Rows
		if (board[0] == board[1] && board[1] == board[2]) win = true;
		if (board[3] == board[4] && board[4] == board[5]) win = true;
		if (board[6] == board[7] && board[7] == board[8]) win = true;
		// Columns
		if (board[0] == board[3] && board[3] == board[6]) win = true;
		if (board[1] == board[4] && board[4] == board[7]) win = true;
		if (board[2] == board[5] && board[5] == board[8]) win = true;
		// Diagonals
		if (board[0] == board[4] && board[4] == board[8]) win = true;
		if (board[2] == board[4] && board[4] == board[6]) win = true;

		if (win == true)
		{
			Console.WriteLine("Victory! Player " + player + " wins!");
			gameRunning = false;
		}
		else
		{
		
			if (player == "X") 
			{
				player = "O";
			}
			else 
			{
				player = "X";
			}
		}
	}
	Console.WriteLine("Press Enter to return to the menu.");
	Console.ReadLine();
}
			
			
			
		}

		static void PlayRPS()
	{
        string[] tools = { "Exit", "Rock", "Paper", "Scissors" }; 

        while (true)                                   
        {
            Console.WriteLine("\n--- Rock Paper Scissors ---");
            Console.WriteLine("1: Rock, 2: Paper, 3: Scissors, 0: Menu");

            string input = Console.ReadLine();          
            
            
            if (!int.TryParse(input, out int userInput) || userInput < 0 || userInput > 3)
            {
                Console.WriteLine("Pick the following input 0-3!");
                continue;                              
            }

            if (userInput == 0) return;                 

            int computerInput = randomNumberGenerator(); 

           
            if (userInput == computerInput)
            {
                Console.WriteLine("Draw!");
            }
            else if ((userInput == 1 && computerInput == 3) || // player chose rock computer choose scissors										  
                     (userInput == 2 && computerInput == 1) || // player choose paper computer choose rock
                     (userInput == 3 && computerInput == 2))   // player choose scissors computer choose paper
            {
                Console.WriteLine("You Win!");
            }
            else
            {
                Console.WriteLine("You Lose!");
            }
            
			Console.WriteLine($"The player chose {userInput}");
		    Console.WriteLine($"computer chose {computerInput}");
			
            Console.WriteLine("Press Enter to continue game ");
            Console.ReadLine(); 
	
        }
    }

    static int randomNumberGenerator()                  // A method that must send back a number (int)
    {
        return rand.Next(1, 4);                         // Picks a random number: 1, 2, or 3
    }
}
