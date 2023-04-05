<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Jozmon/db-template-for-blog">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Database Template For Blog</h3>

  <p align="center">
    A database template for a web blog
    <br>
    this database is made to meet the requirements of a web blog.
    <br />
    
   

  </p>
</div>



<!-- TABLE OF CONTENTS -->

## Table of Contents

  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#Naming">Naming</a>
    </li>
    <li>
      <a href="#Table Representation">Table Representation</a>
    </li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>

<br>
<br>
<br>

<!-- ABOUT THE PROJECT -->
## About The Project

<p align="left"> This an educational project made by our Team , in order to experiment and practice with Data Base Planning.<br>
      The assignment was requested as part of our class at Data Base Engineering by our professor Mr.Kapelas.<br>
      Our aim is to create a sample database module useful both for students and professionals that could be used for future projects in general.<br>
      For any feedback or suggestions on improving you can find our contact details below<br> <p/>
      
 <br>
 <br>
 <br>

![Product Name Screen Shot][product-screenshot]


<br>
<br>
<br>
A database to be used in blog or news website.

<br>
<br>
<br>



Each user has his details plus the attribute "role_id" 
which allows the admin to select between different roles
using the foreign_key from entity roles.

To give each user a role, the attribute "role_id" was used.
Which can have the following options (Administrator, Moderator, 
Author and Simple-User).<br>

For a user to have the role of the administrator the value 0 must choosen
which correspond in table "tbl_role" role 0 with Name:Administrator

Users will write articles using the attribute "author_id"
in table "tbl_posts" to the corresponding "user_id" 
in the table "tbl_users".

It will have the following tables, features and their properties.



<br>
<br>
<br>
<br>
<br>

### Naming

We used "tbl-" at the beginning of each each entity's name to make their
difference clear in relation to the attributes.

Naming was done in lower case for better compatibility
and to make sure there will be no confusion.

<br>
<br>

<!-- TBL_PRESENT -->
### Table Representation

<p>
Below is a detailed explanation of the various relationships between the objects of the database.

We can identify 8 distinct objective entities that will be represented as tables in our database:

1) Posts that are submitted by users , can have images and comments , and are categorized firstly in categories and the categories are categorized in supecategories.            
   * The association here is one-to-many between the user and the post , as a user can post multiple content.
   * Images and comments association with the post is one-to-many as well as a post can have multiple comments and images

2) Users that have roles and can submit posts like articles.
  
3) Roles that determine the user's accesses and capabilities.
   * The association between the user and its role is one to many between the user and the role as a user can have multiple roles(Can be an admin and an author at the same time)

4) Post Images are paired with a post.
 
5) Comments are paired with a post.
   * An one-to-many association between the post  and the image or the comment , as posts can have multiple data.

6) Categories that will separate posts into one of each.
  
7) Categories_Supercategories that will merge categories into bigger ones   
  
8) Supercategory that will define which will be the available supercatogories
   * The association between the categories and supercategories is many-to-many as multiple values can be assigned to both , so a middle option called Categories_Supercategories is used with a one-to-many association between category and Categories_Supercategories as a category will have a single place to the other table       
   * Additionally a table called Supercategory is used with a one-to-many association between supercategory and Categories_Supercategories where a supercategory will have a single place.
            <br></p>

<h4> About Roles and Posts</h4>
 Roles represent the status of the user regarding the blog (An author,a visitor or an administrator for example) as well as the expected behaviour.
 A user with the role name 'Author' can post an article , and at the same time a user that has logged in as a guest can post a comment about an article<br>
 Post are the actual content of the database , including the articles , pictures and comments
 Post are separated into categories and supercategories to streamline user navigation and enchance the user's experience in general.For example
 an article could be in a category called 'Shirts' which will at the same time belong to a supercategory called 'Men's Wear'<br>
            
<h4>Regarding key distribution</h4>
            
<p>Regarding key distribution that will be used during the setting-up of the base we will add the following:

  About posts

 - The posts table will have a column row called post_id as a primary key
 - The images and comments tables will have rows named image_id and comment_id respectively while at the same time they will have rows called post_id as a foreign key so that   the tables may be associated as described above

  With the same logic we go on about roles and users

- Roles table will have a row called role_id as a primary key
- Users will have a row called user_id a primary key and at the same time a row called role_id as foreign key

 And about categories and supercategories

- They will have rows called category_id and supercategory_id as primary keys and at the same time Categories_Supercategories table will have two rows called
category_id and supercategory_id which will be used both a primary key and foreign key<br><p/>

<p>Below we see the actual table representation:<p/>
<pre>

tbl_posts
-------------------------------------
post_id        | int primary_key NL
post_title     | varchar(70) NL
post_textbody  | varchar(10000) NL
<br>


tbl_post_images
-------------------------------------
image_id      | int primary_key NL
image_path    | varchar NL
post_id       | int fk_key NL
<br>


tbl_comments
-------------------------------------
comment_id      | int primary_key NL
visitors_ipv4   | varchar(15) NL
comment_body    | varchar(1000) NL
post_id         | int fk_key NL
<br>


tbl_users
-------------------------------------
user_id              | int primary_key NL
password             | varchar NL
email                | varchar NL
phonenumber          | numeric
birthdate            | date NL
user_role_id         | int NL fk_key
<br>

tbl_roles
-------------------------------------
role_id           | int primary_key NL
rolename          | varchar(70) NL
role_description  | varchar(1000) NL
<br>

tbl_categories
-------------------------------------
category_id         | int primary_key NL
category_name       | varchar NL
<br>


tbl_categories_supercategories
-------------------------------------
category_id         | int primary_key fk_key NL
supercategory_id    | int primary_key fk_key NL
<br>

tbl_supercategories
-------------------------------------
supercategory_id    | int primary_key NL
supercategory_name  | varchar NL

</pre>

<br>
<br>
<br>
<br>

<!-- LICENSE -->
## License

Distributed under the GPL License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Giannis Kekes - micron00@mail.com

Project Link: - [https://github.com/Jozmon/shitbox][repo-link]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Giannis Kekes](micron00@mail.com)
* [Inki](tzaferisleonidas@gmail.com)
* [Theodosis Tsiavos](theotsiavos92@gmail.com)
* [Alexandra](unknown@example.com)

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
[product-screenshot]: images/screenshot.png
[repo-link]: https://github.com/Jozmon/shitbox
