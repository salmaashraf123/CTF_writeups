# Image Flag - Forensics challenge

  platform: ctflearn 
  category: Forensics   30points

## Challenge Description: 
A '.jpg' image file was provided , and the goal was to extract the hidden flag.
No additional hints were given.
----

## Analysis Steps:
### 1. checked Metadata using 'exiftool' 
      exiftool fore101.jpg  
Result : No unusual metadata was found.
### 2. Attempted to extract embedded data using steghide
       steghide --extract -sf "fore101.jpg"
Result: steghide: could not extract any data with that passphrase!
#### 3. use strings for searching for readable strings inside image
        strings "fore101.jpg" 
Result: Success! the following line was found
        
        flag{wow!_data_is_cool}
---
### The flag: 
       flag{wow!_data_is_cool}

[The challenge link](https://ctflearn.com/challenge/96)



      



 
