## Student Registration Portal  
This portfolio outlines a student registration portal for a fictional college called Loney University.  The portal contains the critical elements to register for a class, including a database consisting of the registered students and the available courses for registration.  Functionality has been built, using mySQL and PHP, to register for classes and view registrations once they have been made.  There have also been admin pages added to perform general CRUD operations on the student and class tables via an html interface.  

For reference, the full code can be viewed at https://github.com/Thelius42/studentRegistrationPortal

### Phase 1

For the first phase of this project, I developed and planned the setup.  The setup was based on a design from a college course, where we had planned a student registration portal.  I decided to build that planned project from scratch for this portfolio.  The question was in how to approach it from a coding perspective.  

In the end, I decided to code it in PHP with a mySQL database.  For the look and feel of the overall site, I decided to use jquery and bootstrap styling rules for the look of the buttons and the alerts in particular.  Once I had settled on this layout, I built the database and the basic index.html home page for the site, as well as got a localhost webserver up and running on my workstation.

Below is a sample of some of that bootstrap code at work:



```markdown
This code sets up the button clicks on the main page

      <a href='getClasses.php' class ="btn btn-primary"> Register for a Class</a>&nbsp &nbsp &nbsp &nbsp &nbsp &nbsp
      <a href='viewRegistered.php' class ="btn btn-primary"> View Registered Classes</a> 

```

For an example of how the look came out, the site is fully published at http://ianmloney.com and is fully functional.

### Phase 2

For the second phase, I focused on the administrative pages of the site.  I created a page for modifying each of the classes and students tables.  Upon launch, the entries for each table are listed.  This is using php to pull a basic GET query on the table and listing the contents in a bootstrap table output. Below is the table syntax code:

```markdown
<form action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"] . "?studentID={$studentID}");?>" method="post">
	<table class='table table-hover table-responsive table-bordered'>
		<tr>
			<td>Last Name</td>
			<td><input type='text' name='lastName' value="<?php echo htmlspecialchars($lastName, ENT_QUOTES);  ?>" class='form-control' /></td>
		</tr>
		<tr>
			<td>First Name</td>
			<td><textarea name='firstName' class='form-control'><?php echo htmlspecialchars($firstName, ENT_QUOTES);  ?></textarea></td>
		</tr>
		<tr>
			<td></td>
			<td>
				<input type='submit' value='Save Changes' class='btn btn-primary'/>&nbsp &nbsp
				<a href='maintainStudent.php' class='btn btn-default'>Return to Maintain Students  </a>&nbsp &nbsp
				<a href='index.html' class='btn btn-danger'>Back to Main Menu</a>
			</td>
		</tr>
	</table>
</form>

```


### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
