# mobile-calculate 
[pt1.html](https://github.com/user-attachments/files/24066253/pt1.html)
[pt1.css](https://github.com/user-attachments/files/24066254/pt1.css)
body{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
    font-family: Georgia, 'Times New Roman', Times, serif;
}

.bentuk1{
    width: 250px;
    background-color: #fff;
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 0 10px(rgb(0,0, 0.1));
}
#display{
    width: 230px;
    height: 50px;
    margin-bottom: 20px;
    font-size: 24px;
    text-align: right;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.button{
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 10px;
}

.btn{
    padding: 15px;
    margin-right: 2px;
    margin-bottom: 5px;
    border: none;
    border-radius: 5px;
    background-color: #f0f0f0;
    cursor: pointer;
}

.btn:active{
    background-color: #ddd;
}
.operator{
    background-color: #f9a825;
}
.operator:active{
    background-color: burlywood;
}
.clear{
    grid-column: span 4;
    background-color: crimson;
    color: white;
    width: 100%;
}
.clear:active{
    background-color:tomato;
}

[pt1.js](https://github.com/user-attachments/files/24066279/pt1.js)
function appendvallue(value){ 
    document.getElementById("display").value+=value;
}
function cleardisplay(){
    document.getElementById("display").value="";
} 
function calcute(){
    const display = document.getElementById("display");
    try{
        display.value = eval(display.value);
    }
    catch{
        display.value = "ERROR";
    }
}
