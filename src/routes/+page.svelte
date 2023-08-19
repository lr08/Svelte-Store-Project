  <!-- <style lang="postcss">
    :global(html) {
      background-color:#FBD5D5
    }
  </style> -->

<div class="start" />
<!-- starting div -->

<div id="color1">
  <h1 class="text">Welcome to Employee Management System</h1>

  <div class="main">
    <h1>EMS</h1>

    <div class="heading">
      <h3 class="check1">What is it</h3>
    </div>

    <div class="para">
      An Employee Management System is a software application designed to streamline and automate various processes related to employee administration within an organization. It serves as a centralized platform that enables businesses to efficiently manage their workforce, track employee information, and optimize HR processes. Here's an overview of key features and benefits of an Employee Management System:
    </div>
  </div>
</div>

<div id="color2">
  <div class="container1">
    <section class="sec1">
      <img class="profile-pic" src="/images/camera.jpg" alt="not available" />
    </section>
    <div class="about-grid">
      <div class="box1">
        <div class="box-heading">
          <h3 class="check">Add Details</h3>
        </div>
        <div class="tile">
          The "Add Employee" feature in an Employee Management System (EMS) allows authorized personnel within an organization to input and store new employee information in a structured and organized manner. This feature streamlines the process of onboarding new employees and ensures that their details are accurately captured.
        </div>
      </div>

      <div class="box1">
        <div class="box-heading">
          <h3 class="check">List all Details</h3>
        </div>
        <div class="tile">
          The "List Employee" feature in an Employee Management System (EMS) provides a convenient and organized way to view and manage employee information within an organization. This feature allows users, typically HR personnel and managers, to access a comprehensive list of all employees and their associated details. 
        </div>
      </div>
    </div>
  </div>

  <div class="container2">
    <div class="about-grid2">
      <div class="box2">
        <div class="box-heading">
          <h3 class="check">Update Details</h3>
        </div>
        <div class="tile">
          The "Update Employee" feature in an Employee Management System (EMS) enables HR administrators or authorized users to modify and update the information associated with an employee's profile. This feature plays a crucial role in keeping employee records accurate and up-to-date
        </div>
      </div>

      <div class="box2">
        <div class="box-heading">
          <h3 class="check">Delete Details</h3>
        </div>
        <div class="tile">
          The "Delete Employee" feature in an Employee Management System (EMS) allows authorized users, typically HR personnel or administrators, to efficiently remove employee records from the system. This feature is a crucial part of maintaining accurate and up-to-date employee information. 
        </div>
      </div>
    </div>
    <section class="sec2">
      <img class="profile-pic2" src="/images/camera.jpg" alt="not available" />
    </section>
  </div>

  <!-- closing div -->
</div>

<!-- styling starts from here -->
<style>

  .container1 {
    display: flex;
    flex-wrap: wrap;
  }

  .container2 {
    display: flex;
    flex-wrap: wrap;
  }

  #color1 {
    padding-top: 1%;
    font-size: smaller;
    background-color: #fef2e2;
  }

  #color2 {
    background-color: #ffffff;
    padding-top: 0.2%;
    padding-bottom: 7%;
  }

  .sec1 {
    float: left;
    margin-left: -2vw;
  }

  .sec2 {
    float: right;
    margin-right: -2vw;
    margin-top: 30vh;
  }

  .start {
    max-width: 840px;
    margin: 0 auto;
  }

  .text {
    height: 90px;
    text-align: center;
    font-weight: bold;
    font-size: 70px;
    background-image: linear-gradient(45deg, #553c9a, #ee4b2b);
    color: transparent;
    background-clip: text;
    -webkit-background-clip: text;
  }

  .main {
    display: flex;
    flex-direction: column;
    text-align: center;
    margin-top: 0.2em;
    color: #0b2e7b;
    font-size: large;
  }

  .check1 {
    margin-top: 2%;
    color: transparent;
    font-weight: 30px;
    background-clip: text;
    -webkit-background-clip: text;
    font-size: 30px;
    font-weight: 500;
    background-image: linear-gradient(
      to right,
      #553c9a,
      #ee4b2b,
      #00c2cb,
      #ff7f58,
      #553c9a
    );
  }

  .para {
    padding: 0 150px;
    margin-top: 0.8%;
    margin-bottom: 2%;
    color: #a8a8a8;
  }

  @media screen and (max-width: 500px) {
    .para {
      width: 100vmax;
    }
    .start {
      width: 100vmax;
    }
  }

  .profile-pic {
    border-radius: 0 50% 50% 0;
    margin-left: -7%;
    margin-top: 4rem;
    width: 40vw;
    height: 63vh;
    box-shadow: 0 4px 6px 0 rgba(34, 60, 80, 0.16);
    transition: all ease-in-out 0.2s;
  }

  .profile-pic2 {
    border-radius: 50% 0% 0% 50%;
    margin-right: -7%;
    margin-left: 1%;
    margin-top: -25vh;
    width: 40vw;
    height: 63vh;
    box-shadow: 0 4px 6px 0 rgba(34, 60, 80, 0.16);
    transition: all ease-in-out 0.2s;
  }

  .profile-pic:hover {
    box-shadow: 0 8px 12px 0 rgba(34, 60, 80, 0.16);
  }

  .box-heading {
    border-bottom: 1px solid black;
    color: rgb(15, 9, 1);
  }

  .about-grid{
    display: grid;
    grid-template-columns: repeat(2, 30vw);
    position: sticky;
  }

  .about-grid2 {
    display: grid;
    grid-template-columns: repeat(2, 30vw);
    position: sticky;
  }

  .box1 {
    background-color: #d9f6fa;
    font-size: smaller;
    margin: 10rem 10% -10% 10%;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(187, 16, 16, 0.822);
    box-sizing: content-box;
    max-height: 200px;
    border-radius: 5%;
    color: #545252;
    word-wrap: break-word;
  }


  .box2 {
    background-color: #d9f6fa;
    margin: 10rem 10% -10% 10%;
    font-size: smaller;
    justify-content: center;
    max-height: 200px;
    justify-self: left;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(187, 16, 16, 0.822);
    box-sizing: content-box;
    border-radius: 5%;
    color: #545252;
  }
</style>
