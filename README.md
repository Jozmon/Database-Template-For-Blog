<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Jozmon/ip-dec2bin-private">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Database Template For Blog</h3>

  <p align="center">
    A database for a fashion blog
    <br>
    this database is made to meet the fashion's blog requirements
    <br />
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

![Product Name Screen Shot][product-screenshot]

<br>
<br>
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
### Table representation
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
category_id         | int NL
category_name       | varchar NL
supercategory_id    | int fk_key NL
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
