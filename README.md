//alert("JavaScript works!");
// Cerelia Williams
// SDI 1304
// Project 4
// 5/2/13
// Library of Functions

var myLibrary = function(){

// STRING

	// Phone Number
var checkNum = function (testNumber) {
        var phoneNumber = testNumber;
        var pattern = /^\(?([0-9]{3})\)?[-. ]?([0-9]{3})[-. ]?([0-9]{4})$/; 
        if (pattern.test(phoneNumber)) { 
            var validPhoneNumber = phoneNumber.replace(pattern, "($1) $2-$3");
            console.log("Valid phone number!");
        } else {
            return console.log("This is not a phone number!"); 
        }
    }
	
	
	// Email Address
function checkValidEmail(emailToCheck) {
    var emailAddress = emailToCheck
    var emailPattern = /^[a-zA-Z0-9._-]+@[a-zA-Z0-9._-]+\.[a-zA-Z]{2,4}$/
    if (emailPattern.test(emailAddress)) {
        console.log("This is a valid email address.");
    } else {
        console.log("This is not a valid email address.");
    }
}
	

	// URL
function checkUrl(testUrl) {
    var url = testUrl
    var re = /^(http[s]?:\/\/){0,1}(www\.){0,1}[a-zA-Z0-9\.\-]+\.[a-zA-Z]{2,5}[\.]{0,1}/;
    var isUrl = re.test(url);
    console.log("This is a " + isUrl + " url.");
    if (url.charAt(4) == "s") {
        console.log("This is a https url");
    }
    if (url.charAt(4) == ":") {
        console.log("This is a http url");
    }
}
	

	// Title Cased String
function fixCase(fixThis) {
    String.prototype.toProperCase = function () {
        return this.replace(/\w\S*/g, function (txt) {
            return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
        });
    };
    
    fixThis.toProperCase();
    console.log(fixThis.toProperCase()); 
}
	

	// String w/ Separator
function changeSeparator(changeThis) {
    if (changeThis) {
        return console.log("a/" + "b/" + "c/");
    }
}
	

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

	
// ARRAY

	// Smallest Value
function getSmallest() {
    function chosenNum(element, index, array) {
        return (element >= 5);
    }
    var filtered = [2, 0, 7, 20, 100, 11].filter(chosenNum);
    chosenNum();
    filtered.sort(function (a, b) {
        return a - b;
    });
       
    return console.log(filtered.shift());
	
	// Total Value

	// Array of Objects
	


	return {
		"checkNum" : checkNum
		"checkValidEmail" : checkValidEmail
		"checkUrl" : checkUrl
		"fixCase" : fixCase
		"changeSeparator" : changeSeparator
		"fixDecimal" : fixDecimal
		"getDays" : getDays
		"getSmallest" : getSmallest
		
		
}


var newLib = new myLibrary();{

}

console.log("checkUrl: " + newLib.checkUrl("http: or https:")); 



