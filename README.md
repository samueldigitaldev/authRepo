# authRepo

Description: This is the authentication portion of the application. Currently the user information is encrypted using the bcrypt library and salt. The application uses JWT authentication and Local Strategy for authentication. Database Schema is simple and only requires email and password.

Getting Started:
Omit all of the double quotes when running the commands
1. "npm install"
2. Set up MongoDB and run the "mongod" file through the terminal to get the database running
3. Create a config.js file in the root directory and input this text:
module.exports = {
    secret: 'anytextyouwant'
};
This will configure your secret string that they use to encrypt.
4. "npm run dev"
5. Make a POST request on Postman ie: localhost:3090/signup, it requires an email and password ie:
{
	"email": "test20@example.com",
	"password": "123"
}
Select Raw and JSON in the Body section of Postman
6. Change the URL to: localhost:3090/signin and use the same email and password to sign in. You should get a token from this action.
7. Change URL to localhost:3090 and do a GET request with the token from the previous step. You should get:
{
    "hi": "there"
}
