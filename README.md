# Web Page for Mathematical Calculations

## AIM:

To design a static website with validation to perform mathematical calculations in client side.

## DESIGN STEPS:

### Step 1:

Requirement collection.

### Step 2:

Creating the layout using HTML and CSS.

### Step 3:

Write javascript to perform the calculations.

### Step 4:

Include regularexpression based input validation.

### Step 5:

Validate the layout in various browsers.

### Step 6:

Validate the HTML code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mathematical Calculations</title>
    <style>
    * {
    box-sizing: border-box;
    font-family: Arial, Helvetica, sans-serif;
    }
    body {
    background-color: rgb(85, 193, 236);
    color:black;
      
    }
    .container {
    width: 1080px;
    margin-left: auto;
    margin-right: auto;
    }
    .content {
    display: block;
    width: 100%;
    background-color: cornsilk;
    margin-top: 75px;
    min-height: 300px;
    }
    .content2 {
    display: block;
    width: 100%;
    background-color: cornsilk;
    min-height: 300px;
    }
    .footer{
    display:inline-block;
    width: 1080px;
    height: 35px;
    background-color: #bd6fbd;
    color:black;
    text-align: center;
    padding-top: 8px;
    margin-left:auto;
    margin-right: auto;
    font-size: 18px;
    }
    h1{
        text-align: center;
        padding-top: 20px;
        font-size: 28px;
    }
    .formelement{
        text-align: center;
        padding-top: 12px;
        font-size:large
    }
    </style>
</head>
<body>
    <div>
        <div class="container">
            <div class="content">
                <h1>Volume of Rectangular Tank</h1>
                <form>
                    <div class="formelement">
                        <label for="lengthedit">length:</label>
                        <input type="text" id="lengthedit" value="0"/> Meters
                    </div>
                    <div class="formelement">
                        <label for="heightedit">Height:</label>
                        <input type="text" id="heightedit" value="0"/> Meters
                    </div>
                    <div class="formelement">
                        <label for="widthedit">width:</label>
                        <input type="text" id="widthedit" value="0"/> Meters
                    </div>
                    <div class="formelement">
                        <input type="button" value="CALCULATE" id="addbutton"/>
                    </div>
                    <div class="formelement">
                        <label for="volumeedit">Volume:</label>
                        <input type="text" id="volumeedit" readonly value="0" /> Meter <sup>3</sup>
                    </div>
                </form>
            </div>
                <div class="footer">Developed by Vaishnavi M</div>
                </div>
            </div>
        </div>
    <div>
    <div class="container">
        <div class="content2">
            <div>
                <h1>Area Of Triangle</h1>
                <form>
                    <div class="formelement">
                        <label for="theightedit">Height:</label>
                        <input type="text" id="theightedit" value="0"/> Meters
                    </div>
                    <div class="formelement">
                        <label for="baseedit">Base:</label>
                        <input type="text" id="baseedit" value="0"/> Meters
                    </div>
                    <div class="formelement">
                        <input type="button" value="AREA" id="areabutton"/>
                    </div>
                    <div class="formelement">
                        <label for="areaedit">Area:</label>
                        <input type="text" id="areaedit" readonly value="0" /> Meter <sup>2</sup>
                    </div>
                </form>
            </div>
            </div>
            <div class="footer">Developed by Vaishnavi M</div>
        </div>
        </div>
    </div>
<script>
    var button;
    button=document.querySelector("#addbutton");
    button.addEventListener("click",function(){
        var lengthtext,heighttext,widthtext,volumetext;
        var lengthval,heightval,widthval,volumeval;
        var res,res1,res2,reg;
  
        lengthtext=document.querySelector("#lengthedit");
        heighttext=document.querySelector("#heightedit");
        widthtext=document.querySelector("#widthedit");
        volumetext=document.querySelector("#volumeedit");
        reg=new RegExp("^[1-9]+[0-9]*$")

        lengthval=lengthtext.value;
        res=lengthval.match(reg);
        heightval=heighttext.value;
        res1=heightval.match(reg);
        widthval=widthtext.value;
        res2=widthval.match(reg);

        if(res==null)
        {
            alert("Please Enter Positive Integers Only for length");
        }
        if(res1==null)
        {
            alert("Please Enter Positive Integers Only for Height");
        }
        if(res2==null)
        {
            alert("Please Enter Positive Integers Only for Width");
        }
        volumeval=lengthval*heightval*widthval;
        volumetext.value=""+volumeval;
      
    });
</script>
<script>
    var button;
    button=document.querySelector("#areabutton");
    button.addEventListener("click",function(){
        var theighttext,basetext,areatext;
        var theightval,baseval,areaval;
        var res,res1,reg;

        theighttext=document.querySelector("#theightedit");
        basetext=document.querySelector("#baseedit");
        areatext=document.querySelector("#areaedit");
        reg=new RegExp("^[1-9]+[0-9]*$")

        theightval=theighttext.value;
        res=theightval.match(reg);
        baseval=basetext.value;
        res1=baseval.match(reg);
        if(res==null)
        {
            alert("Please Enter Positive Integers Only for Radius");
        }
        if(res1==null)
        {
            alert("Please Enter Positive Integers Only for Height");
        }
        areaval=1/2*theightval*baseval;
        areatext.value=""+areaval;
    });
</script>
</body>
</html>

```

## OUTPUT:
![output](./output.png)
![output](./voutput.png)
## Result:

Thus a website is designed to perform mathematical calculations in the client side.
