## Feature
As a user, I want to create a public gist. <br />
(To create a public gist, user must create a GitHub's account first.)

### Test Scenario (Positive)
Verify that User can Sign Up with correct terms.
### Test Case
Given User has successfully access the URL https://gist.github.com/ <br />
And User should see Sign Up button. <br />
When User clicks Sign Up button. <br />
Then User should directed to Join GitHub page. <br />
When User filled the Username form with "mzuhairiy". <br />
And User filled the Email address with "atasnamazuhair@gmail.com". <br />
And User filled the Password with correct terms. <br />
And User clicks the checkbox of Email preferences. <br />
And User has successfully verify the account with verification challenge. <br />
And User has clicks the Create account button. <br />
Then User should directed to Launch Code page. <br />
And User should received Launch Code at Email. <br />
When User filled the form with correct Launch Code. <br />
Then User should see "Welcome to GitHub" text. <br />
And User should see "Skip personalization" hyperlink text. <br />
When User clicks "Skip personalization" hyperlink text. <br />
Then User should directed to the URL https://gist.github.com/ <br />

### Test Scenario (Negative)
Verify that User can not Sign Up with incorrect terms.
### Test Case
Given User has successfully access the URL https://gist.github.com/ <br />
And User should see Sign Up button. <br />
When User clicks Sign Up button. <br />
Then User should directed to Join GitHub page. <br />
When User filled the Username form with "mzuhairiy". <br />
Then Warning "username mzuhairiy is not avaliable" should appear. <br />
And User should see suggestion for the username. <br />
When User filled the Email address with "atasnamazuhair@gmail.com". <br />
Then Warning "Email is invalid or already taken" should appear. <br />
When User filled the Password with incorrect terms. <br />
Then Warning "Password is too short (minimum is 8 characters), needs at least 1 lowercase letter, and is in a list of passwords commonly used on other websites" should appear. <br />
When User failed to verify the account with verification challenge. <br />
Then Warning "Whoops! That's not quite right" should appear. <br />
And User should see Try Again button. <br />

### Test Scenario (Positive)
Verify that User can Sign In with correct credential
### Test Case
Given User has successfully access the URL https://gist.github.com/ <br />
And User should see Sign In button. <br />
When User clicks Sign In button. <br />
Then User should directed to Sign In page. <br />
And User should see "Sign in to GitHub to continue to Gist" text. <br />
When User filled the Username or email address form with correct credential. <br />
And User filled the Password form with correct credential. <br />
And User clicks the Sign in button. <br />
Then User directed to Discover gist page. <br />
And User should see Discover gist text. <br />

### Test Scenario (Negative)
Verify that User can not Sign In with incorrect credential.
### Test Case
Given User has successfully access the URL https://gist.github.com/ <br />
And User should see Sign In button. <br />
When User clicks Sign In button. <br />
Then User should directed to Sign In page. <br />
And User should see "Sign in to GitHub to continue to Gist" text. <br />
When User filled the Username or email address form with incorrect credential. <br />
And User filled the Password form with incorrect credential. <br />
And User clicks the Sign in button. <br />
Then Warning "Incorrect username or password." should appear. <br />

### Test Scenario (Positive)
Verify that User able to create a public gist.
### Test Case
Given User has successfully login and directed to the URL https://gist.github.com/ <br />
When User clicks the "+" navigation bar.
Then User should see "Instantly share code, notes, and snippets." text. <br />
And User should see "Create secret gist" button.
When User filled the Gist description form with "This is a description."
And User filled the Filename form with name and extension type "Plato.js"
And User filled the text area with "I wanna create a public gist"
When User clicks the select menu button.
And User clicks the "Create public gist".
And User should see the "Create public gist" button.
When User clicks the "Create public gist" button.
And User directed to the Code page.
Then User has succesfully create a public gist.


