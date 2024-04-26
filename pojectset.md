# PROJECT 1

```JAVASCRIPT

const buttons = document.querySelectorAll('.button');
const body = document.querySelector('body');
//hello
buttons.forEach(function (buton) {
  console.log(buton);
  buton.addEventListener('click', function (color_change) {
    console.log(color_change);
    console.log(color_change.target);
    if (color_change.target.id == 'grey') {
      //body.style.backgroundColor = 'grey';
      body.style.backgroundColor = color_change.target.id;
    }
    if (color_change.target.id == 'white') {
      //body.style.backgroundColor = 'white';
      body.style.backgroundColor = color_change.target.id;
    }
    if (color_change.target.id == 'blue') {
      //body.style.backgroundColor = 'blue';
      body.style.backgroundColor = color_change.target.id;
    }
    if (color_change.target.id == 'yellow') {
      //body.style.backgroundColor = 'yellow';
      body.style.backgroundColor = color_change.target.id;
    }
  });
});
```

## PROJECT 2

```Javascript

const form = document.querySelector('form');

form.addEventListener('submit', function (wha) {
  wha.preventDefault();
  const height = parseInt(document.querySelector('#height').value);
  const weight = parseInt(document.querySelector('#weight').value);
  const results = document.querySelector('#results');
  if (height === '' || height < 0 || isNaN(height)) {
    results.innerHTML = 'invalid number';
  } else if (weight === '' || weight < 0 || isNaN(weight)) {
    results.innerHTML = 'invalid number';
  } else {
    const bmi = (weight / ((height * height) / 10000)).toFixed(2);
    results.innerHTML = `<span>${bmi}</span>`;
  }
});
```

### PROJECT 3

```JAVASCRIPT

const clock = document.querySelector('#clock');
setInterval(function () {
  let date = new Date();
  //console.log(date.toLocaleString());
  clock.innerHTML = date.toLocaleTimeString();//  'Hours: " + h + " Minutes: " + m + " Seconds:
}, 1000);
```
