
# HUD-BUD DOCUMENTATION
## Annika Huprikar, Brandon Demkowicz

### We created a web application in Python that performs web scraping of the Harvard University Dining Services (HUDS) website on the daily to access, read, and manipulate the menu data for appropriate placement in our HUD-BUD SQL Database on the backend. Functionally, this application allows users to set daily calorie/nutrition goals and eating preferences/allergies/restrictions according to the food tags offered by HUDS, to thus generate useful combinations of meals for a daily meal plan that matches the user's intended goals. This project grew out of Harvard University's CS50 course.

### DEMO VIDEO LINK
https://youtu.be/KLs-Tke6zDg

## Below is more information about how to use our web application HUD-BUD!

## ACCESSING FILES
Change directory into this HUD-Bud repository folder and in the command line, run “flask run” to begin the program.

## REGISTERING USER
In the top right corner of the screen, click the “Register” tab. Enter in a username and a password, and then re-enter the same password in the confirmation box.
Clicking submit will create your account, and redirect you to the profile initialization page.

## INITIALIZING PROFILE SETTINGS
On the profile initialization page, enter in a non-zero, integer amount of calories (without any commas) into the “Calorie Goal” box, which will set the upper-limit for the number of calories you want in your diet plan. Then, in the box where it prompts you to select any dietary restrictions, check all of the allergens/restrictions that you would like omitted from your plan. Click confirm to complete the initialization step.

## WEB SCRAPING
After submitting the profile initialization page, the HUDS menu site will be web scraped, according to the given date and meal type (breakfast, lunch, or dinner) to dynamically construct the series of URLs to web scrape. For each meal of the day, a food item and all of its relevant nutritional information (calories, any allergens, fats, carbs, etc…) will be stored amongst a few tables in the HUDS sqlite3 database. Note: This will take some time, as several different pages are being web scraped to retrieve all of the relevant food information.

## GENERATING PLAN
After the daily menu information has been stored in the database, the daily food plan will be generated in accordance with your daily caloric intake and prescribed dietary restrictions/allergens specified in your profile page. The breakdown of the food plan by meal will be displayed on the webpage in tables, with an aggregate “summary” table at the bottom of the page, detailing overall caloric and nutrient intake.

## EDIT PROFILE
You can edit your profile any time by clicking the “My Profile” in the upper right corner of the screen, wherein you can modify your caloric intake and dietary
restrictions/allergens. After confirming those changes, a new plan will be generated accordingly.

## LOG OUT → LOG IN
If you wish to log out, click “Log Out” in the top right corner of the screen, which will redirect you back to the login page. If you wish to log back in, type in your username and password credentials into the corresponding fields. 

This is... HUD-Bud! Voila!
