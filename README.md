SDI-Project4-1304
=================
//alert("JavaScript works!");
// Cerelia Williams
// SDI 1304
// Project 4
// 5/2/13
// Library of Functions

var myLibrary = function(){

// NUMBER

  // Number Format
function fixDecimal(moneyAmt) {
    var money = moneyAmt
    money.toFixed(2)
    return console.log(money.toFixed(2));	
	
	// Fuzzy-Match


	// Hours & Dates
function getDays(testDate) {
    var realDay = testDate;
    today = newDate(2013, 02, 05);
    var one_day = 1000 * 60 * 60 * 24;
    console.log(Math.ceil((today.getTime() - realDay.getTime()) / (one_day)) + " days have gone by since " + testDate)
}

// Actual Number Data

return {
		"fixDecimal" : fixDecimal
		"getDays" : getDays

}


var newLib = new myLibrary();{

}

console.log(

