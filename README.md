# Multiplication-table

const times1 = [1,2,3,4,5,6,7,8,9,10,11,12];//use for both x and y axis
var myLine = ''; //line for each times table row
var x; //just a variable to hold my multiplication results before concatenation

function timesTables(e, e2) {
  times1.forEach(function(e) { //x axis
    times1.forEach(function(e2) { //y axis
      //begin multiplication, e will go through e2's 1-12 and multiply each number
      x = e * e2; 
      //concatenate multiplication and space for each number/forEach in the first row of 1-12
      myLine =  `${myLine} ${x}`; 
    });
    //print out line of the multiplication table
    console.log(myLine);
    //clear line before starting the next line of table
    myLine = '';
  });
}
//call function with arrays containing numbers to be multiplied to create table
timesTables(times1, times1);
