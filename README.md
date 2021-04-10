# tabledesign
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
   <style>
   body{
       display:flex;
       justify-content: center;
       height: 100vh;
       margin:200px auto;
       align-content: center;
   }
   /* table style */
   table{
       border-collapse: collapse;
       padding:10px;
       width:100px;
       border-radius: 10px;
       overflow: hidden;
       box-shadow: 0px 10px 10px rgba(0,0,0,0.3);
   }
   table thead{
       background:orange;
       padding: 10px;
       
   }
   table thead th{
    padding: 20px;
   }
   table tbody tr td{
       text-align: center;
       padding:20px;
       margin:10px;
      
   }
    table tbody tr:nth-last-of-type(even){
    background: rgb(155, 153, 153);
    }
    table tbody tr:hover{
        background:#ddd ;
    }
   </style>
</head>
<body> 
   <table>
       <thead>
           <th>Roll</th>
           <th>Name</th>
           <th>Marks</th>
       </thead>
       <tbody id="tbody">
       </tbody>
   </table>
   <script>
       var a = [{
    name:"Gking",
    roll:1,
    marks:95
},
{
    name:"Rking",
    roll:2,
    marks:98
},
{
    name:"raj",
    roll:3,
    marks:99
}
]
newTable(a);
function newTable(data){
    var table = document.getElementById("tbody");
    for(let i = 0; i<data.length;i++)
    {
       var row  = `<tr>
                 <td>${data[i].roll}</td>
                 <td>${data[i].name}</td>
                 <td>${data[i].marks}</td>
                </tr>`;
      table.innerHTML += row;
    }
}
   </script>
</body>
</html>
