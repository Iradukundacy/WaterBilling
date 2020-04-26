<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
  <meta content="text/html; charset=utf-8" http-equiv="Content-Type" />
    <title>Water Billing</title>
       <link rel="stylesheet" type="text/css" href="mycssfinal.css">
</head>
<body>
   <div>
    <br />
   <h1 style="color:white;text-align:center;font-style:italic;font-weight:bold" id="title">Water Billing Calculator</h1>
  </div>
      <div style="width:70%; margin:5% 15% 5% 15%; height: auto " id="globaldv">
      <div style="background-color: #034A50" id="containt">

     <div style="width:65%; height: auto;background-color: #07AA95; z-index:5" id="form">
	  <h1 style="color:white;text-align:center; font-weight:bold" id="title">Water Meter</h1>
     <form action="billingform.php" method="get">

         <div class="row">
         <div class="col-25">
         <label for="lastm3">Initial Number of m<sub>3</sub></label>
      </div>
       <div class="col-75">
       <input type="number"name="last" min="1" max="99" id="lastm3" placeholder="The last number of m3 "/>
	  </div>
    </div>
       <div class="row">
       <div class="col-25">
       <label for="currentm3">Current Number of <sub>3</sub></label>
      </div>

    <div class="col-75">
      <input type="number" name="current" min="1" max="99" id="currentm3" placeholder="The current number of m3 "/>
    </div>
   </div>

     <div class="row">
     <div class="col-25">
       <label for="Category">Category</label>
     </div>

         <div class="col-75">
         <select id="Category" name="category">
           <option value="PublicTop">Public Tap</option>
           <option value="Residential">Residential</option>
           <option value="NoResidential">Non Residential</option>
           <option value="Industries">Industries</option>
         </select>
        </div>
       </div>

            <div class="row">
            <div class="col-25">
            </div>

       <div class="col-75">
         <input type="submit" value="Calculate"/>
         <input type="reset" value="Reset"/>

         </div>
       </div>
     </form>
    </div>

       <div style=" float:right;width:35%; height: auto;margin-top:-42.5%;margin-left:20px" id="result" >
      <br />

       <h2 style="color:white;text-align:center; font-weight:bold" id="title">Money To Pay</h2>

       <p style="color:white;text-align:center; font-weight:bold;text-align:center" >


<spam>
<?php
              $last = $_GET["last"];
              $current = $_GET["current"];
              $category = $_GET["category"];

if($category == "PublicTop"){
                $used = ($current - $last)*323;              
echo $used;

}elseif($category == "Residential"){
                  $used = ($current - $last)*340;              
echo $used;
}elseif($category == "Residential"){
                  $used = ($current - $last)*720;              
echo $used;
}elseif($category == "Residential"){
                  $used = ($current - $last)*845;              
echo $used;

}elseif($category == "Residential"){
                  $used = ($current - $last)*877;              
echo $used;

}elseif($category == "NoResidential"){
                  $used = ($current - $last)*877;              
echo $used;

}elseif($category == "NoResidential"){
                  $used = ($current - $last)*895;              
echo $used;

}else{
                  $used = ($current - $last)*736;              
echo $used;
              }

            ?><em>&nbsp;&nbsp; Rwanda Francs</em></spam>

 </p>

    </div>
   </div>
  </div>
 </body>
</html>



                            Sytlesheet codes




body{
	/*background-color: teal;*/
	background-image:url('water-1.jpg');
	background-repeat: no-repeat;
    background-size: cover;
 
}
#globaldv {
  border-radius: 15px 15px 15px 15px;
  padding: 2px;
  /*background: #73AD21;  
  width: 200px;
  height: 150px;*/
}

#form {
  border-radius: 20px 0px 900px 20px;
  padding:2% 0% 2% 0%;

  /*background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;*/
}

#containt {
  border-radius: 15px  5px  5px 15px;

  /*background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;*/
}

#result {
  border: 1px solid white;

  /*background: #73AD21;
  padding: 20px;
  width: 200px;
  height: 150px;*/
}




