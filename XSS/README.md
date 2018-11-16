User ***REMOVED*** will be submitted when the password is changed.
![change password](1.png "")
![change password](2.png "")
The code to change the password is 43 lines in seacms/member.php. There is no security or even format detection for $email before inserting, directly insert into the database, resulting in storage XSS
![change password](3.png "")
Code is executed when a user visits or an administrator visits a website.
![change password](4.png "")
![change password](5.png "")