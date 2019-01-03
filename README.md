# pro-Milana
//úkol

//do promenne 'data' chci ukladat cisla
let data = [1,2,3];

//uklada nove hodnoty a kontroluje, zda jde o cisla
function addNum(cisla) {
  for (let i = 0; i < cisla.length; i++) {
    if (typeof cisla[i] === 'number') {
      data.push(cisla[i]);
  } else {
     console.log('pouze cisla');
    }
  }
}

// pocita prumer, max a min
function statistika () {
  let suma = 0;
  let min = data[0];
  let max = data[0];
  for (let j = 0; j < data.length; j++) {
    suma = suma + data[j];
    if (min < data[j]) {
      min = data[j]
    }
    if (max > data[j]) {
      max = data[j]
    }
  }
  return  console.log('Soucet je '+ suma, '. Minimum je '+ min, '. Maximum je '+ max)  
}

// take pocita max a min (objevil jsem tyhle fce az po tom, co jsem napsal tu predchozi)
function statistika2 () {
  let max = Math.max(...data);
  let min = Math.min(...data);
  return console.log("max = " , max, "min = ", min)
}


addNum ([5,'fs',6,44,true,564]) 
console.log(data)
statistika() 
statistika2()
