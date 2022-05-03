# php-code-tutorial
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 2</title>
    <style>

        .table1{
            font-size: small;
            background-color: blueviolet;
            width: 50vw;
            height: 80vh;
            margin:50px;
            color: white;
            padding: 60px;
        }
        .table2{
            width: 500px;
            height:200px;
            border-collapse: collapse;

             }

            .table2 td{
                border: black solid 2px; 
            }
        h1{
            background: black;
            color: white;
         
            box-sizing: border-box;
            display: inline;
            margin-left: 50px;
            align-content: center;
        }
         

        div{

            font-size:small;
            background:grey;
            color: black;
            width: 50vw;
            margin: 50px;

        }
    </style>
</head>
<h1 align="center">Student Registration Form</h1>
<body> 
    <form action="index.php" method="post" >
    <table class="table1"> 

        <tr>
          <td> FRIST NAME</td>
          <td colspan="5"> <input type="text" name="fname" maxlenght="30" >(max30 characters a-z and A-Z)</td>
        </tr>
        <tr>
        <td> LAST NAME</td>
        <td colspan="5"><input type="text" name="lname" maxlenght="30">(max30 characters a-z and A-Z)</td>
        </tr>
        <tr>
            <td>DATE OF BIRTH</td>
            <td colspan="5">
                <select name="day" id="" name="day">
                    <option value="day" selected>day</option>
                    <?php 
                        for($i=0; $i<=31; $i++){
                    ?>
                    <option value="<?php echo $i ?> "> <?php echo $i ?></option>
                   
                    <?php } ?> 
                </select>
                <select name="month" id="" name="month">
                    <option value="month" selected>month</option>
                    <option value="january">january</option>
                    <option value="february">february</option>
                    <option value="march">march</option>
                    <option value="april">april</option>
                    <option value="may">may</option>
                    <option value="june">june</option>
                    <option value="jully">jully</option>
                    <option value="september">september</option>
                    <option value="october">october</option>
                    <option value="november">november</option>
                    <option value="december">december</option>
                </select>
                
                <select name="year" id="">
                    <option value="year" selected>year</option>
                    <?php 
                        for($i=1970; $i<=2022; $i++){
                    ?>
                    <option value="<?php echo $i ?> "> <?php echo $i ?></option>
                    <?php } ?>
                    
                </select>
            </td>
        </tr>
        <tr>
            <td>EMAIL ID</td>
            <td colspan="3"><input type="text" name="email"></td>

        </tr>
        <tr>
            <td>MOBILE NUMBER</td>
            <td colspan="4"><input type="text" maxlength="10" name="mobnumber">(10 digit number)</td>
            
        </tr>
        <tr>
            <td>GENDER</td>
            <td colspan="5">
            Male<input type="radio" name="gender" value="male">Female<input type="radio" name="gender" value="female"></td>
            </tr>
            
            <tr>
                <td>ADDRESS</td>
                <td colspan="4"><textarea name="address" id="" cols="30" rows="5"></textarea></td>
            </tr>
            <tr>
                <td>
                    CITY
                </td>
                <td colspan="5"> <input type="text" name="city" maxlenght="30"> (max30 characters a-z and A-Z)</td>
                
            </tr>
            <tr>
                <td>PIN CODE</td>
                <td colspan="5"><input type="number" id="pin" name="password" value="" maxlenght="6">(6 digit number)</td>
            
            </tr>
            <tr>
                <td>STATE</td>
                <td colspan="5"><input type="text" name="state"maxlenght="30">(max30 characters a-z and A-Z)</td>
             
            </tr>
            <tr>
                <td>COUNTRY</td>
                <td colspan="4"><input type="text" value="India" name="country"></td>
            </tr>
            <tr>
                <td>HOBBIES</td>
                <td colspan="3">Drawing<input type="checkbox" name="hobby[]" value="Drawing">
                    Singing<input type="checkbox" value="singing" name="hobby[]">
                    Dancinng <input type="checkbox" value="dancing" name="hobby[]">
                    sketching<input type="checkbox" value="sketching" name="hobby[]">
                    Others <input type="checkbox" value="others" name="hobby[]">
                    <input type="text" name="hobby[]">
                 </td>
            </tr>
            <tr>
            <td rowspan="6">QUALIFICATION</td>
            </tr>
            <tr>
            
                     <td>SI.No Examination</td>
                     <td>Board</td>
                     <td>Percentage</td>
                     <td>Year of passing</td>
            </tr>
       <tr>
           <td>1.Class X</td>
          <td><input type="text" name="Board1"></td>
           <td><input type="text"name="Percentage1"></td>
           <td><input type="text" name="yearofp1"></td>
       </tr>
       <tr>
        <td>2.Class XIII</td>
        <td><input type="text" name="Board2"></td>
        <td><input type="text"name="Percentage2"></td>
        <td><input type="text"name="yearofp2"></td>
       </tr>
    <tr>
        <td>3.Graduation</td>
        <td><input type="text" name="Board3"></td>
        <td><input type="text"name="Percentage3"></td>
        <td><input type="text" name="yearofp3"></td>
    </tr>
    <tr>
        <td>4.Masters</td>
        <td><input type="text" name="Board4"></td>
        <td><input type="text"name="Percentage4"></td>
        <td><input type="text" name="yearofp4"></td>
    </tr>
    <tr>
        <td>
        <p></p>
        </td>
        <td></td>
        <td align="center">(10 characters max)</td>
        <td align="center">(up to 2 decimal)</td>
        <td></td>
    </tr>
    <tr>
        <td>COURSE APPLIED FOR  :</td>
        <td colspan="5">BCA <input type="radio" name="course" value="BCA">
            B.Com <input type="radio" name="course" value="B.Com">
             B.Sc <input type="radio" name="course" value="B.Sc">
           B.A <input type="radio" name="course" value="B.A"> </td>
    </tr>
    <tr>
        <td colspan="6" align="center">
            <input type="submit" value="printpreview">
            <input type="reset" value="reset">
        </td>
    </tr>

    </table>
    
    </form>
    <h1> Report Form</h1> <br>

    
    <!-- php codes start here! -->


    <div>
    
    First name : <?php echo $_POST ['fname']?><br><br>
    Last name  :  <?php echo $_POST ['lname']?> <br> <br>
    Date of birth : <?php echo $_POST ['day'] ."/".$_POST ['month']."/".$_POST ['year']?> <br> <br>
    E-mail: <?php echo $_POST ['email']?> <br><br>
    Mobile Number:<?php echo $_POST['mobnumber']?> <br><br>
    Gender: <?php echo $_POST['gender']?> <br><br>
    <div cols=20 rows="5"> <?php echo $_POST ['address']?></div> <br><br>
    CITY:<?php echo $_POST ['city']?><br><br>
    STATE:<?php echo $_POST ['state']?><br><br>
    COUNTRY:<?php echo $_POST ['country']?><br><br>
    HOBBIES:<?php 
        foreach ($_POST['hobby'] as $hob) { echo $hob." "; }?><br><br>
       
    <table class="table2">


    <tr>
            
     <td>SI.No Examination</td>
     <td>Board</td>
     <td>Percentage</td>
     <td>Year of passing</td>
    </tr>
   <tr>
     <td>1.Class X</td>
     <td><?php echo $_POST ['Board1']?></td>
     <td><?php echo $_POST ['Percentage1']?></td>
     <td><?php echo $_POST ['yearofp1']?></td>
    </tr>
       <tr>
        <td>2.Class XIII</td>
        <td><?php echo $_POST ['Board2']?></td>
        <td><?php echo $_POST ['Percentage2']?></td>
        <td><?php echo $_POST ['yearofp2']?></td>
       </tr>
    <tr>
           <td>3.Graduation</td>
           <td><?php echo $_POST ['Board2']?></td>
           <td><?php echo $_POST ['Percentage3']?></td>
           <td><?php echo $_POST ['yearofp3']?></td>
    </tr>
    <tr>
           <td>4.Masters</td>
           <td><?php echo $_POST ['Board4']?></td>
           <td><?php echo $_POST ['Percentage4']?></td>
           <td><?php echo $_POST ['yearofp4']?></td>
    </tr>
    </table> <br><br>

   Course Applied For: <?php echo $_POST ['course'] ?><br><br>
</div>

</body>
</html>
