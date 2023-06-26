// JavaScript program to find the number of charters
      // in the longest word in the sentence.
      function LongestWordLength(str)
      {
        var n = str.length;
        var res = 0,
          curr_len = 0;
        for (var i = 0; i < n; i++)
        {
         
          // If current character is not
          // end of current word.
          if (str[i] !== " ") curr_len++;
          // If end of word is found
          else
          {
            res = Math.max(res, curr_len);
            curr_len = 0;
          }
        }
 
        // We do max one more time to consider
        // last word as there won't be any space
        // after last word.
        return Math.max(res, curr_len);
      }
 
      var s = "I am an intern at gomycodeniger";
      document.write(LongestWordLength(s));
       