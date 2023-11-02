<table>
  <tr>
   <td colspan="6" ><strong>Test cases for login form ('Login to TeamCity server' form')</strong>
   </td>
  </tr>
  <tr>
   <td colspan="6" >Preconditions:
<p>
- TeamCity server is installed and started
<p>
- correct user credentials: user - admin, password - admin
<p>
- login page<a href="http://localhost:8111/login.html"> http://localhost:8111/login.html</a> is opened
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td><strong>N</strong>
   </td>
   <td><strong>Name</strong>
   </td>
   <td><strong>Preconditions</strong>
   </td>
   <td><strong>Steps</strong>
   </td>
   <td><strong>Data</strong>
   </td>
   <td><strong>Expected result</strong>
   </td>
  </tr>
  <tr>
   <td colspan="6" ><strong>UI verification</strong>
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
0</p>

   </td>
   <td>Check form UI
   </td>
   <td>
   </td>
   <td>- open Login form
   </td>
   <td>
   </td>
   <td>Form should contain the following componenets:
<p>
- TeamCity logo
<p>
- 'Log in to TeamCity' caption
<p>
- 'Username' label
<p>
- Empty Textbox for username
<p>
- 'Password' label
<p>
- Empty testbox for password
<p>
- 'Remember me' checkbox. On by default
<p>
- 'Reset password' link
<p>
- 'Log in' button
<p>
- version and build number label
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
1</p>

   </td>
   <td>Check tab orders
   </td>
   <td>
   </td>
   <td>- set cursor on username text box
<p>
- press Tab button on keyboard several times
   </td>
   <td>
   </td>
   <td>tabulation order on the page should go from top to bottom and from left to right:
<p>
username textbox, password textbox, Remember me checkbox, Reset password link, Login button.
   </td>
  </tr>
  <tr>
   <td colspan="6" ><strong>Username and password positive and negative cases</strong>
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
2</p>

   </td>
   <td>Successful login with correct username and password
   </td>
   <td>
   </td>
   <td>- Enter correct credentials.
<p>
- "remember me" option is On
<p>
- Press Log in button
   </td>
   <td>User - admin,
<p>
password - admin
   </td>
   <td>System is logged in with admin user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
3</p>

   </td>
   <td>Change password and relogin
   </td>
   <td><span style="text-decoration:underline;">Login with existing user</span>
   </td>
   <td>- in user profile change password
<p>
- Logout
<p>
- enter username and new password
   </td>
   <td>
   </td>
   <td>User successfully logged in with the new password
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
4</p>

   </td>
   <td>Login fails with empty username and password
   </td>
   <td>
   </td>
   <td>- leave username and password fields empty
   </td>
   <td>
   </td>
   <td>'Incorrect username or password' message is shown
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
5</p>

   </td>
   <td>Login fails with Incorrect username
   </td>
   <td>
   </td>
   <td>- Enter incorrect username:
<p>
- press Login button
   </td>
   <td>username - admin1,
<p>
password - admin
   </td>
   <td>'Incorrect username or password' message is shown
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
6</p>

   </td>
   <td>Login fails with Incorrect password
   </td>
   <td>
   </td>
   <td>- Enter incorrect password for correct user
<p>
- press Login button
   </td>
   <td>username - admin,
<p>
password - admin1
   </td>
   <td>'Incorrect username or password' message is shown
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
7</p>

   </td>
   <td>Login fails with Empty username
   </td>
   <td>
   </td>
   <td>- Enter password without username:
<p>
- press Login button
   </td>
   <td>username -
<p>
password - admin
   </td>
   <td>'Incorrect username or password' message is shown
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
8</p>

   </td>
   <td>Login fails with Empty password
   </td>
   <td>
   </td>
   <td>- Enter username without password:
<p>
- press Login button
   </td>
   <td>username - admin,
<p>
password -
   </td>
   <td>'Incorrect username or password' message is shown
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
9</p>

   </td>
   <td>Successful login with changed case in username
   </td>
   <td>
   </td>
   <td>- enter username in uppercase
<p>
- press Login button
   </td>
   <td>User - ADMIN,
<p>
password - admin
   </td>
   <td>System is logged in with admin user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
10</p>

   </td>
   <td>Failed login with changed case in password
   </td>
   <td>
   </td>
   <td>- enter password in uppercase
<p>
- press Login button
   </td>
   <td>User - admin,
<p>
password - Admin
   </td>
   <td>'Incorrect username or password' message is shown
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
11</p>

   </td>
   <td>User with max symbols in username is able to login
   </td>
   <td>Create a user with max symbols in username
   </td>
   <td>- enter username and password
<p>
- press Login button
   </td>
   <td>Username - contains max symbols
<p>
password - any
   </td>
   <td>System is logged in with the user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
12</p>

   </td>
   <td>User with max symbols in password is able to login
   </td>
   <td>Create a user with max symbols in password
   </td>
   <td>- enter username and password
<p>
- press Login button
   </td>
   <td>username - admin
<p>
password - contains max symbols
   </td>
   <td>System is logged in with the user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td colspan="6" ><strong>Special cases in username or password</strong>
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
13</p>

   </td>
   <td>SQL, XSS injection is not performed
   </td>
   <td>
   </td>
   <td>- enter script text as username
<p>
- press Login button
   </td>
   <td>1. &lt;script> alert( 'Hello, world!' ); &lt;/script>
<p>
2. Drop table Users
   </td>
   <td>- ''Incorrect username or password' message is shown
<p>
- no script is performed
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
14</p>

   </td>
   <td>Special symbols in username are correctly processed
   </td>
   <td>
   </td>
   <td>- enter special symbols as username
<p>
- press Login button
   </td>
   <td>±!@#$%^&*()_+{}"|:?>&lt;§[];'\,./
   </td>
   <td>- ''Incorrect username or password' message is shown
<p>
- no error in developer console
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
15</p>

   </td>
   <td>Special symbols in password are correctly processed
   </td>
   <td>register user with password that contains alphanumeric symbols, and special symbols
   </td>
   <td>- enter correct username and password, described in preconditions
<p>
- press Login button
   </td>
   <td>username - user
<p>
password - qWsD±!@#$%^&*()_+{}"|:?>&lt;§[];'\,./
   </td>
   <td>System is logged in with the user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
16</p>

   </td>
   <td>Special symbols in username are correctly processed
   </td>
   <td>register user with username that contains alphanumeric symbols, and special symbols
   </td>
   <td>- enter correct username and password, described in preconditions
<p>
- press Login button
   </td>
   <td>username - qWsD±!@#$%^&*()_+{}"|:?>&lt;§[];'\,./
<p>
password - admin
   </td>
   <td>System is logged in with the user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td colspan="6" ><strong>Lock period after failed login attempts</strong>
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
17</p>

   </td>
   <td>Lock period after 5 failed login attempts
   </td>
   <td>
   </td>
   <td>- enter incorrect password for existing user 5 times in 1 minute
   </td>
   <td>username - admin
<p>
password - incorrect
   </td>
   <td>'You made 5 failed login attempts in 1m. Due to security reasons you will be able to login only in %d s.' message is shown with time left to 1 min
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
18</p>

   </td>
   <td>login blocked during lock period
   </td>
   <td><span style="text-decoration:underline;">5 failed login attempts</span>
   </td>
   <td>- during lock period enter correct username and password
   </td>
   <td>User - admin,
<p>
password - admin
   </td>
   <td>'You made 5 failed login attempts in 1m. Due to security reasons you will be able to login only in %d s.' message is shown with time left to 1 min. Timer should be updated after page refresh
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
19</p>

   </td>
   <td>successful login after lock period
   </td>
   <td><span style="text-decoration:underline;">5 failed login attempts</span>
   </td>
   <td>- enter correct username and password
   </td>
   <td>User - admin,
<p>
password - admin
   </td>
   <td>System is logged in with admin user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td colspan="6" ><strong>'Remember me' option</strong>
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
20</p>

   </td>
   <td>Login is saved after reopen browser with ''Remember me' is on
   </td>
   <td><span style="text-decoration:underline;">login with remember me On</span>
   </td>
   <td>- Quit browser
<p>
- open Projects page again
   </td>
   <td><a href="http://localhost:8111/favorite/projects">http://localhost:8111/favorite/projects</a>
   </td>
   <td>Projects view with admin user logged in is opened again
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
21</p>

   </td>
   <td>Login successful with ''Remember me' is OFF
   </td>
   <td>
   </td>
   <td>- Enter correct credentials.
<p>
- "remember me" option is Off
<p>
- Press Log in button
   </td>
   <td>User - admin,
<p>
password - admin
   </td>
   <td>System is logged in with admin user. Projects view is opened
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
22</p>

   </td>
   <td>Login is reset after reopen browser with ''Remember me' is OFF
   </td>
   <td><span style="text-decoration:underline;">login with Remember me Off</span>
   </td>
   <td>- Quit browser
<p>
- open Project page again
   </td>
   <td><a href="http://localhost:8111/favorite/projects">http://localhost:8111/favorite/projects</a>
   </td>
   <td>Login page is opened
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
23</p>

   </td>
   <td>Login is saved after reopen browser tab with 'Remember me' option On or Off
   </td>
   <td><span style="text-decoration:underline;">login with Remember me On</span>
   </td>
   <td>- close tab while browser is still opened
<p>
- open Projects page again
   </td>
   <td><a href="http://localhost:8111/favorite/projects">http://localhost:8111/favorite/projects</a>
   </td>
   <td>Projects view with admin user logged in is opened again
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
24</p>

   </td>
   <td>Login is saved after reopen browser tab with 'Remember me' option On or Off
   </td>
   <td><span style="text-decoration:underline;">login with Remember me off</span>
   </td>
   <td>- close tab while browser is still opened
<p>
- open Projects page again
   </td>
   <td><a href="http://localhost:8111/favorite/projects">http://localhost:8111/favorite/projects</a>
   </td>
   <td>Projects view with admin user logged in is opened again
   </td>
  </tr>
  <tr>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td colspan="6" ><strong>Reset password option</strong>
   </td>
  </tr>
  <tr>
   <td><p style="text-align: right">
25</p>

   </td>
   <td>'Reset password' button open Reset password page
   </td>
   <td>
   </td>
   <td>Click 'Reset password' button
   </td>
   <td>
   </td>
   <td>'Reset password' form is opened
   </td>
  </tr>
</table>

