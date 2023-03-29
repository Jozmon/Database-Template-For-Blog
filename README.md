<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Jozmon/ip-dec2bin-private">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">DB For Fashion Blog</h3>

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

tbl_arthra
-------------------------------------
id_arthrou      | int primary_key
titlos_arthrou  | varchar(70)
keimeno_arthou  | varchar(10000)
<br>


tbl_eikones_arthrou
-------------------------------------
id_eikonas      | int
path_eikonas    | varchar
id_arthrou      | int fk_key
<br>


tbl_sxolia
-------------------------------------
id_sxoliou      | int primary_key
ipv4_sxoliasti  | varchar(15)
keimeno         | varchar(1000)
id_arthrou      | int fk_key
<br>


tbl_xristes
-------------------------------------
id_xristi            | int primary_key
kodikos              | varchar
email                | varchar
arithmos             | numeric
hmerominia_geniseis  | date
id_rolou             | int     fk_key
<br>

tbl_rolou
-------------------------------------
id_rolou         | int primary_key
onoma_rolou      | varchar(70)
perigrafi_rolou  | varchar(1000)
<br>

tbl_katigories
-------------------------------------
id_katigorias        | int
onoma_katigorias     | varchar
id_yperkatigorias    | int fk_key
<br>


tbl_yperkatigories
-------------------------------------
id_yperkatigorias    | int
onoma_yperkatigorias | varchar

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

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
[product-screenshot]: images/screenshot.png
[repo-link]: https://github.com/Jozmon/shitbox
