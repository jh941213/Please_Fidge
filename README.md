## 1. Introduction  
To reduce food waste and promote various cooking activities by recognizing the contents of the user's refrigerator, recommending possible cooking menus and providing related cooking videos.\

**Expected Benefits**  
- Reduces food waste by efficiently utilizing the remaining ingredients in the refrigerator.
- Helps users easily try different dishes, adding interest and enjoyment to cooking.


## 2. Components  
**Raspberry Pi and the Pi Camera**    
Capture the contents of the refrigerator and use object recognition to identify ingredients.  

**Object recognition system**  
Use YOLOv5 to accurately recognize ingredients from images.  

**OpenAI API**   
Recommend possible dishes based on the recognized ingredients.  

**YouTube crawling module**  
Automatically search and fetch YouTube links to cooking videos related to the suggested menu.  

**Telegram notification system**  
Sends menu recommendations and YouTube video links to users in Telegram messages.  

**3. 
