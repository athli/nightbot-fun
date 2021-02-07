# nightbot-fun
Best way to learn JavaScript: make Nightbot more annoying

Hello internet people! This is a repository of custom Nightbot functions for the Twitch streamer frostfireflakes (twitch.tv/frostfireflakes). All code is written in JavaScript and all files on the main branch have been confirmed to perform the way they are expected to.
If you fork this repository for any purpose, I would appreciate being acknowledged as the original source ^^ thanks friends.

How to use this thing:
  1. All commands have their own separate text files.
  2. Code templates for different "types" of commands can be found in the "templates" folder.
  3. After editing, submit and make a pull request.
  4. If the newest version of the code doesn't work, go back to a version that works by looking at past commits.
  5. Learn to use git/GitHub in general.
 
Tips and Tricks:

  1. Nightbot recognizes a function as one string of characters with no whitespace. Any input in the same message after the first whitespace is considered to be a part of $(query). The variable query is not a String object; we aren't quite sure what it is yet. To process the query as a string, place the expression in quotes like so: "$(query)".
  
    Valid function names: help, discord, !uptime, 13098417, rickroll_me
    Invalid function names: I need help, lol lol lol, what is the uptime
  
  2. Above, we said $(query) is not a String object. It seems to be a list of some items, where the items can be typecast to String objects without loss. As noted above, the entire "list" can also be typecast as a String while preserving whitespace and punctuation. Since $(query) has a list structure of sorts, it is possible to access elements of $(query) by index. $(query) indexes from 1 beginning at the first word after the command name, i.e., in the following message, if "This" is a command name, then "is a test message to explain how Nightbot reads messages." would be $(query), "is" would be $(1), "a" would be $(2), and so on.
  
    This is a test message to explain how Nightbot reads messages.
    
  3. Users making commands in Discord, take note: double quotes (" ") are different for some users on mobile versus on computer; please feel free to copy/paste any of the following:
  
    ""     // empty string
    
    " "    // string with one space inside
    
    "word" // string that is a word (or phrase)
