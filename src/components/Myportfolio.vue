<template>
    <div class="wrapper">

      <nav class="navbar">
      <ul>
        <li><a href="#contact">Contact</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#Expertise">Expertise</a></li>
        <li><a href="#about-me">About</a></li>
        <li><a href="#home">Home</a></li>
      </ul>
    </nav>

    <div class="content" id="home">
        <img src="@/assets/image/rey.jpg" alt="home" class="home"/>

        

           <h1> Hello, My Name Is</h1>
           <p class="a">CAHOYLA, REYMELYN</p>

        <p>
         --- A Creative Freelancer and Full Stack Developer
        </p>
        

    <div class="cta-buttons">
         <router-link to="/rankingstudents"></router-link>
    </div>
    <div class="social-media">
    <a href="https://www.facebook.com/ReymieCahoyla" target="_blank"><i class="fab fa-facebook"></i></a>
    <a href="https://twitter.com/CahoylaReyms" target="_blank"><i class="fab fa-twitter"></i></a>
    <a href="https://www.instagram.com/reymieee___/" target="_blank"><i class="fab fa-instagram"></i></a>
    <!-- Add more social media icons and links as needed -->
  </div>
</div>


    <div class="about" id="about-me">
        <h2> ABOUT ME </h2>

            <p class="abc"> 
               Hi there! I'm Reymelyn B. Cahoyla,  and I am currently a student at Cordova Public College, pursuing a degree in Information Technology. 
               As an IT student, I am passionate about exploring the dynamic world of technology and its endless possibilities. 
               I am dedicated to honing my skills in programming, web development, and digital innovation.
                With a curious mind and a drive for excellence, I am eager to learn and grow in this ever-evolving field.
                 Beyond academics, I enjoy exploring new technologies, participating in coding competitions,
                  and contributing to projects that make a positive impact. I am excited about the opportunities ahead and look forward to 
                  leveraging my knowledge and skills to make meaningful contributions to the tech industry.
                  <br>                           
                                         
 Let's connect and collaborate on your next project!   
</p>
    </div>
        



    <div class="ab" id="portfolio">
      <h2 >Projects</h2>

<div v-for="(link, index) in links" :key="index" class="card">
  <a :href="link.url" target="_blank">
    <img :src="link.imageUrl" alt="Link Image">
    <h2>{{ link.title }}</h2>
    <p>{{ link.description }}</p>
  </a>
</div>
    </div>
    <div class="c" id="Expertise">
        <h2>Programming Languages Expertise</h2>

    <div class="grid-container">
       <div v-for="(language, index) in languages" :key="index" class="language">
          <p class="language-name">{{ language.name }}</p>

       <div class="stars-container">
          <span v-for="n in 5" :key="n" :class="{ 'filled': n <= language.expertiseLevel }">★</span>
      </div>
    </div>
  </div>
</div>


    <div class="b" id="contact">
        <h2> Contact Information </h2>

        <div class="contact" id="all">

          
         
          <div class="contact-item">
            <label for="email"><i class="fas fa-envelope"></i> Email:</label><br>
            <span id="email"><b>{{ contact.email }}</b></span>
          </div>

          <div class="contact-item">
            <label for="phone"><i class="fas fa-phone"></i> Phone:</label><br>
            <span id="phone"><b>{{ contact.phone }}</b></span>
          </div>

          <div class="contact-item">
            <label for="address"><i class="fas fa-map-marker-alt"></i> Address:</label><br>
            <span id="address"><b>{{ contact.address }}</b></span>
          </div>
     </div>
     </div>

  </div>
  </template>
  
    
<script>
import exampleImage1 from '@/assets/image/vv.jpg'; // Import image using relative path
import exampleImage2 from '@/assets/image/req.jpg';
import exampleImage3 from '@/assets/image/accc.jpg';
  export default {
    data() {
      return {
        links: [
        { title: 'Example Link 1',  description: 'Voters Tracker Management', imageUrl: exampleImage1 },
        { title: 'Example Link 2',  description: 'CPC Appointment System', imageUrl: exampleImage2 },
        { title: 'Example Link 3', description: 'Account Management', imageUrl: exampleImage3 }
        ],
        contact: {
        email: 'cahoylareymelyn@gmail .com',
        phone: '639-329-123-656',
        address: 'Purok 4, Sudtonggan, Lapu-Lapu City'
      },
      languages: [
        { name: 'JavaScript', expertiseLevel: 4 }, // Expertise level out of 5
        { name: 'Python', expertiseLevel: 3 },
        { name: 'Java', expertiseLevel: 5 },
        { name: 'C++', expertiseLevel: 2 },
        { name: 'HTML/CSS', expertiseLevel: 4 },
        { name: 'Ruby', expertiseLevel: 3 },
        { name: 'PHP', expertiseLevel: 1 }
      ]
      };
    }
  };
</script>
  
<style scoped>

  .wrapper {
    /* flex: 1; */
    overflow-y: auto;
    /* background: linear-gradient(to top, #ffffff, #f0f0f0, #7FD625); */
    background: #536878;
    color: white;
  }
/* 
  .navbar {
  padding: 5px;
 } */

 .navbar li {
  display: inline;
 float: right;
 margin-right: 5%;
}

.navbar a {
  text-decoration: none;
  color: #fff;
}
  
.content {
  margin-top: 5%;
  position: relative;
  border: 5px solid rgba(255, 255, 255, 0.5); /* Border with faded white color */
  border-radius: 30px; /* Add border radius for rounded corners */
  padding: 40px; /* Add padding to content */
  overflow: hidden; /* Hide overflowing content */
  /* Other styles for the content container */
}

.a {
  font-family: "Arial Rounded MT Bold", Arial, sans-serif;
  font-size: 50px;
  font-weight: bold;
  color: white;
}
  
.ab {
    font-family: Arial, Helvetica, sans-serif;
    letter-spacing: 1px;
    text-align: justify;
    line-height: 2;
    /* display: flex;
    justify-content: space-around;
    align-items: center;
    height: 100vh; */

}
  
.cta-buttons {
    margin-top: 20px;
 margin-left: 10%;
  padding: 15px 30px; /* Adjust padding to make button bigger */
  width: 120px;
  font-size: 1.2em; /* Increase font size */
  background-color:#536878;; /* Light color for the button */
  border: none; /* Remove border */
  border-radius: 25px; /* Add border radius */
  cursor: pointer; /* Add cursor pointer */
  /* Other styles for the button */
}

.abc {
  font-family: Times New Roman;
  letter-spacing: 1px;
  text-align: justify;
  line-height: 1.5;
  width: 85%;
}
  

  .home {
    width: 300px; /* Set width and height to define the size of the circle */
    height: 300px;
    float: right;
    margin-left: 10px;
    border-radius: 50%; /* Make the border radius 50% to create a circle */
    overflow: hidden; /* Ensure that the image is clipped to the circular shape */
  }
 
  .about {
    text-align: center;
    margin-top: 10%;
    
  }

  h2 {
    font-family: "Arial Rounded MT Bold", Arial, sans-serif;
  font-weight: bold;
  color: white;
  }
  .ab {
    text-align: center;
    margin-top: 10%;
    
  }

  .b {
    text-align: center;
    margin-top: 10%;
    font-size: 40px;
    margin-bottom: 5%;
  }

  .c{
    text-align: center;
    margin-top: 10%;
  }

p {
 font-family: Times New Roman;
 font-size: 25px;
 margin-left: 8%;
 width: 80%;
 text-align: center;
 color:  #080808;
 letter-spacing: 2px;
}

  .card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 15px;
  margin-bottom: 20px;
  transition: transform 0.3s ease;
  width: 50%;
  margin-left: 25%;
}

.card:hover {
  transform: translateY(-5px);
}

.card a {
  text-decoration: none;
  color: #333;
}

.card h2 {
  margin-top: 0;
}

.card p {
  margin-bottom: 0;
}

.card img {
  max-width: 30%;
 
}

.contact {
  display: flex;
  flex-wrap: wrap;
}



.contact-item {
 
  background-color: #778899;
  border: 2px solid #778899;
  color: black;
  border-radius: 10px;
  margin-bottom: 1px;
  padding: 5px;
  font-size: 20px;
  width:20%;
  margin-left: 3%;
  font-family: Times New Roman;
  letter-spacing: 2px;
  text-align: center;
  line-height: 2;
  
}
.grid-container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 20px;
}


.language {
  display: flex;
  flex-direction: column;
}

.language-name {
  margin-bottom: 5px;
    font-weight: bold;
    color: #f5fffa;
}

.stars-container {
  display: flex;
  margin-left: 30%;
}

.stars-container span {
  color: #ffd700;
  font-size: 25px;
}

.stars-container span.filled {
  color: #00008b; /* Change the color as per your requirement */
  
}

.social-media {
  margin-top: 10px;
 

}

.social-media a {
  
  text-decoration: none;
  color: #fff; /* Change the color of the icons as needed */
  margin-right: 50px;
 float: right;

}

.social-media a i {
  font-size: 30px; /* Adjust the size of the icons as needed */
}


  </style>







