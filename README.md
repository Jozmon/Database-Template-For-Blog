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
      <a href="#getting-started">Getting Started</a>
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

A database made for a fashion blog

which will contain the following entities and attributes:

<br>
<br>
<br>
<br>
<br>

<pre>
Tbl_Arthra
-------------------------------------
ID Arthrou      |int primary_key
Titlos Arthrou  |varchar(70)
Keimeno Arthou  |varchar(10000)
<br>


Tbl_Eikones_Arthrou
-------------------------------------
ID Eikonas      |int
Path Eikonas    |varchar
ID Arthrou      |int fk_key
<br>


Tbl_Sxolia
-------------------------------------
ID Sxoliou      |int primary_key
IPv4 Sxoliasti  |varchar(15)
Keimeno         |varchar(1000)
ID Arthrou      |int fk_key
<br>


Tbl_Xristes
-------------------------------------
ID Xristi            |int primary_key
Kodikos              |varchar
Email                |varchar
Arithmos             |numeric
Hmerominia Geniseis  |date
ID Rolou             |int     fk_key
<br>


Tbl_Katigories
-------------------------------------
ID Katigorias        |int
Onoma Katigorias     |varchar
ID Yperkatigorias    |int fk_key
<br>


Tbl_Yperkatigories
-------------------------------------
ID Yperkatigorias    | int
Onoma Yperkatigorias | varchar

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


