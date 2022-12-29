# Unit5Program
Unit5
public class it213Unit5AssignmentPart2 {

	public static void main(String[] args) 
	{

// Create a string variable called sentence and initialize it with the phrase
	String sentence = "The quick brown fox jumps over the lazy dog";
	
	//declare variables to track position in sentence, blank position and word count
	int current =0;
	int blankPosition =0;
	int wordcount = 0;
	
	//Starting at the beginning of the sentence, examine each character, until you reach the end of the sentence
	for (int i = 0; i < sentence.length(); i++)
	{
	
		current = i;
		String word;
		
		blankPosition =sentence.indexOf(" ", current);
		
		//if at end of sentence, extract the current word and set counter variable i to sentence length to stop looping
		if (blankPosition == -1)
			
			//extract the word
			word = sentence.substring(current);
		    i=sentence.length();
		    }
	
	          else
	          {

		//if not at end of sentence, extract the current word and sent counter variable i to position of blank to keep looping
		word = sentence.substring(current, blankPosition);
		int i = blankPosition;
		
	}
	//increment the word count
	wordcount++;
	//print the word
	System.out.println(wordcount + " " + word);
	
	}
	//Print the total word count
	System.out.println("Total word count " + wordcount);

}

}//end of program for unit5 assignment
