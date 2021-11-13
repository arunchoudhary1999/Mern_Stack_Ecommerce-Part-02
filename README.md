# MERN_STACK_ECOMMERCE_PROJECT-REACT-REDUX-EXPRESS-NODE-MONGODB-COMPLETE-PART-02
# Hello Everyone, I am Arun Choudhary

# Backend error handling :-
1. We have to first create a class error handling, So that it handles all the errors in the backend itself, for which we do not have to write much code, we have to write only 1 line.
2. Before this we will create a folder utils and inside it we will create a file named errorhander.js.
3. After this we will create a folder named middleware, in it we will have a file named error in which we will import errorhander.js
   and
   Now by importing the errorhandle in productController file we will use it to getProductDetails.
4. After doing all these things, we will aslo go to test on the postman.
5. The errorhander is complete, but what about async error? -> Whenever we are told to use async/await function, We should always use try/catch block with it. Try block will run only when the code inside it is successfully true., Otherwise the code inside catch will run then we will create an errorhandle for it which will be special for async.

-> Why are we using ty/catch what type of error will the try/catch block run on?
   For Example:- When this thing will come in handy, when we create the product, if we dosn't put some details in it then it will continue to be processed in the server, so our server will keep getting ruined.
   So to solve this problem we use try/catch block so that if it work successfully it will give result, else show error it will work in our try/catch block.
6. Now these is only one type of error which is -- that when we put the database link wrong, then what kind of error will we get from it this type of error is called Unhandled Promise Rejection.
   So the reason for getting this kind of error is that from where our server has crashed, this is the error for that.
   Solution :- What we have to do when this kind of error comes that we have to shutdown the server as soon as possible then we will coding for that.
7.If someone also search for undefined thing on our website the we will show him this undefined error. we call this type of error as UnCaughter error.
8. Now only the last type of error remains that mangodb error before resolvong it we see what kind of error show us in mongodb. http://localhost:4000/api/v1/product/645 <-- And mongodb know that the product has no such Id. "cast to pbjectId failed for value\*645\*(type string at path\*_id\* for model\"Product\" <-- Will show this kind of error, showing this kind of error because we have put something like this 645 id in place of product id which is not accessible is.
9. After this errorhander, we will add some feature beacuse right now our website does not have the facility of search filtering and pagination that we can filter through category or can shot according od rating this thing if not, then what is the use of our website, we are going to create it first --> Search, Filter, and Pagination.
10. For this we will create a file named apifeature.js which will be in the folder named utils, inside it we will create a class named apifeature.
11. Search Function :- We have used search function because if a user comes to our website and search by entering the name of the product in the search box then all the information related to that product will be shown and if the product which is not in our list then if user search then it will show null to that user.
12. Filter Function :- We have used filter function because any user will  come to our E-ecommerce website and enter any price range related to the product i.e if any person wants to check any product between 10000 to 15000, he/she can check this can use filter.
13. Pagination Function :- We have created Pagination function because it will work to show limited product only on one page instead of showing together, it works pagination function.
    * Even our search, filter, pagination i completed, after that we start user password authentication. *

# BACKEND USER & PASSWORD AUTHENTICATION:-
# * Now will do backend Authentication *
14.Basically the model of the user will be created how the user will login and register.
15. So to make this we have to install some package. like - bcryptjs, jsonwebtoken, validator, nodemailer, cookie-parsar, body-parsar.
    1. bcryptjs :- what is bcrypt :- when we save our or user's password, it will be saved in the database, so before they are saved. we will convert the password to a hash with the help of bcrypt. so that no one can see the correct password of anyone, so we will install bcrypt.
    2. jsonwebtoken :- what will the jsonwebtoken do it is basically used to generate the token.
    3. validator :- validator is neccesary to check whether the data is correct or not, so this module is easy to use and validator data quickly and easily.
    4. Nodemailer :- What does nodemailer do, if a user forwards the password then reaches the link on his email as OTP or as per reset password this is how notemailer works and we don't need to type any special message which it automatically sends.
16. Even we have finished the work of registration and pasword hash Now after this we will see that if a user registers and we want to get him automatic loging. then we will see how we will do that.
17. After the registration and token generation is ouer, now we will create the login function.
18. But let's make a function for authentiaction, we will work in this that the user who is logged in can access the product, for this we will do authentication, for this we will create a file named auth.js inside the middleware in which we will autheticate.
19. * So for what we have done is that if the user login he/she can see the product get meaning but he/she can not create, update and delete any thing which we have done. And by admin login, he/she can do all the work, he/she can create, update and delete any product all this we have dome in authentication. * 
20. Now we are going to create a method in userModel because w have to provide facility to reset password so if someone forget password then he can also set password by generating reset token like we do by clicking on foerword password.
21. Then we started creating getresetpasswordToken and forgetpassword functions -- why did we do this?
    If a user wants to break the password, then before breaking the password from him, we have to get the reset token again so that we can forget the user.
    After doing this, we will create a URL to break the password on the user's email, which we will send to the user's email, so that he can break the password by linking on the link.
22. Even by sending an email to the user, we asked him to change the password.
23. After this we will solve the minor errors
24. And till now our backend authentication is completed
