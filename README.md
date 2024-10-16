# addSum
To Add a string of comma-separated numbers


function add(str) {
 const numbers = str.split(/[, ;// \n]+/).map(Number);
 let negatives = numbers.filter(e => e < 0);
 if(negatives.length > 0) {
   return `negative numbers not allowed ${negatives.join(', ')}`;
 }
 console.log(numbers)
 let ans = numbers.reduce((a,b) => a+b,0)
  return ans
}

//add('12')
console.log(add(''));
console.log(add('1'));
console.log(add('1,5'));
console.log(add('1,2,-3'));
console.log(add('1\n2,3'));
console.log(add('//;\n1;2;4'));
