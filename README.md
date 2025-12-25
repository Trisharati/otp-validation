# otp-validation project
**Architecture overview**
------------------------
Backend
-------
node js has been used with controller and router files.Environment variables has been stored in .env file
.env file consists of required fields of mobile otp validation and token generating key
In short login has been implemented with phone number or email field only
code for otp has been written but it is commented out. Due to app-password generation with demo account for email and regional issue with the number collected from the 
npm package real time otp was not delivered. The OTP passed by to frontend is hard coded. It is just collected from api response and put on to the otp field to proceed.
On validation api it sends a jwt token to the frontend which has been kept valid for 2 minutes.

Frontend
--------
Validation for email and phone fields are done in the frontend.
After OTP submission it goes to the dashboard.
It will auto logout after 2 minutes and also clear the token stored in localstorage.
The dashboard is protected with the token.

The blocking of the user due multiple attempts has not been implemented due to non real time OTPs.
auth before the roots has not been used as only page was to protect and it has been taken care in the frontend.
