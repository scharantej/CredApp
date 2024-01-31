## Flask Application Design for Sign-up and Login with Email and Password

### HTML Files

1. **signup.html:** This HTML file will contain the form for new user signup. It will include fields for email address, password, and password confirmation.

2. **login.html:** This HTML file will contain the form for user login. It will include fields for email address and password.

3. **profile.html:** This HTML file will display the user's email address once they have successfully logged in.

### Routes

1. **@app.route('/signup', methods=['GET', 'POST'])**: This route will handle the signup process. When the user accesses the '/signup' URL, the GET method will display the signup form. When the user submits the form, the POST method will validate the submitted data, hash the password, and create a new user in the database.

2. **@app.route('/login', methods=['GET', 'POST'])**: This route will handle the login process. When the user accesses the '/login' URL, the GET method will display the login form. When the user submits the form, the POST method will validate the submitted data, compare the password with the hashed password in the database, and if they match, log the user in and redirect them to their profile page.

3. **@app.route('/profile')**: This route will display the user's profile page. When the user accesses the '/profile' URL, the route will check if the user is logged in. If the user is logged in, the route will retrieve their email address from the database and display it on the profile page. If the user is not logged in, the route will redirect them to the login page.