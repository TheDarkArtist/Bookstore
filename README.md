# Bookstore
A Django Project

# Requirements for the project
1. Check if you have PostgreSQL install in your system or not, if not, install it, and set it up.
2. Now you will have to create a Database in PostgreSQL named < bookstore > (without the angle brackets :)
That's it

# Setting up the project
1. Clone the git reop whereever you want
 
2. cd into the reop
   
3. Run the folowing command to install the pip requirements(dependencies) for the project 

    ```
     pip install -r requirements.txt
   ``` 
   Note: you can also setup a virtual enviornment if you want
   
5. Now run the fullowing comand to migrate the database 
 
   ```
   python manage.py migrate
   ```
   
Now you're all set up, all you gotta do is run the server by following command 

  ```
  python manage.py runserver
  ```

The Bookstore should be live at ```localhost:8000```      
