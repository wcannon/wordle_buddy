# wordle_buddy

**Usage**:
The general idea is to pass in all data guessed so far (in 1 concise string) from a wordle game and have the possible wordle words left as output.  

**The guess string is in single quotes and in two parts**:  
**part 1**: the guess characters that match or have no match yet.    
The character is either in the correct spot, or in the word but in the incorrect spot. (green background or orange background)  
If no match is found so far, the position should be represented by a # character  

Each position in the word is separated by a comma  
If a letter was found it is simply listed followed by a comma  
If 1+ letters are in the word but not in that position they are listed together prepended with a - sign.  

**part 2**: the letters guessed and not found in the word  

**Example for the word "sable"**  
python3 ./guesses.py '#,r,-w,#,e:adjxq'

**Here is the 'translation' of the guess above:**    
Position 1: no matches at all  
Position 2: letter 'r' matched (green background)  
Position 3: letter '-w' matched but in incorrect position (orange background)  
Position 4: no matches at all    
Position 5: letter 'e' matched (green background)   
Second part: these letters were guessed but not in the word 'adjxq'  

**Output from above is:**  

Candidate words found:  
write  
wrote  
