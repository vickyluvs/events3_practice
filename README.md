# Exercise Link: <br>
https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Test_your_skills:_Events#events_1<br>

# Instructions: <br>
In the next events-related task, you need to set an event listener on the `<button>s'` parent element <br>
`(<div class="button-bar"> … </div>)`, which when invoked by clicking any of the buttons will set the background of the `button-bar` to the color contained in the button's `data-color` attribute.<br>

We want you to solve this without looping through all the buttons and giving each one their own event listener.<br>

# My Solutions: <br>
Solution 1: <br>
```
 const buttonBar = document.querySelector(".button-bar");
//Add your code here
let redBtn = document.getElementsByTagName("button")[0];
      let yelloBtn = document.getElementsByTagName("button")[1];
      let greenBtn = document.getElementsByTagName("button")[2];
      let purpleBtn = document.getElementsByTagName("button")[3];

      const changeColor = () => {
        redBtn.style.backgroundColor = "red";
        yelloBtn.style.backgroundColor = "yellow";
        greenBtn.style.backgroundColor = "green";
        purpleBtn.style.backgroundColor = "purple";
      };

      buttonBar.addEventListener("click", changeColor);
```
solution 2 using for loop <br>
```
const changeColor = () => {
  const allBtn = document.getElementsByTagName("button");
  for (let i = 0; i < allBtn.length; i++) {
    allBtn[0].style.backgroundColor = "red";
    allBtn[1].style.backgroundColor = "yellow";
    allBtn[2].style.backgroundColor = "green";
    allBtn[3].style.backgroundColor = "purple";
  }
};
buttonBar.addEventListener("click", changeColor);
```
solution 3 using map and push array method <br>
```
const colorChanger = () => {
  let arrayBtn = [];
  let buttonColor = document.getElementsByTagName("button");
  arrayBtn.push(buttonColor);

  let newButton = arrayBtn.map((buttons) => {
    buttons[0].style.backgroundColor = "red";
    buttons[1].style.backgroundColor = "yellow";
    buttons[2].style.backgroundColor = "green";
    buttons[3].style.backgroundColor = "purple";
  });
  return newButton;
};
buttonBar.addEventListener("click", colorChanger);
```

