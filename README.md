# CodeWars

* Lost Without a Map -> Get the double of every int in a list -->
```
List<int> maps(List<int> arr) => arr.map((i) => i * 2).toList();
```

* Reverese a string -->
```
String solution(str) => str.split('').reversed.join();
```

* Getting the Sun of the list and returning 0 if list is empty -->
```
num sum(List<num> arr) => arr.fold(0, (previousValue, newValue) => previousValue + newValue);
```

* Convert a Boolean to a String -->
```
String booleanToString(bool b) => b.toString();
```

* Odd or Even of total sum of list -->
```
String oddOrEven(List<int> array) =>array.reduce((a, b) => a + b).isEven ? 'even' : 'odd';
```

* Get Vowels count in a given string -->
```
int getCount(String inputStr){
  var count = 0;
  var vowels = <String>["a","e","i","o","u"];
  for(int i=0;i < inputStr.length;i++){
    if(vowels.contains(inputStr[i]))
      count++;
  }
  return count;
}
```
* You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters. -->
```
String getMiddle(String s) {
  final middleIndex = s.length ~/ 2;
  return s.length.isOdd ? s[middleIndex] : s.substring(middleIndex - 1, middleIndex + 1);
}
```
* Given an array of digitals numbers, return a new array of length number containing the last even numbers from the original array (in the same order). The original array will be not empty and will contain at least "number" even numbers. 

For Example

**([1, 2, 3, 4, 5, 6, 7, 8, 9], 3) => [4, 6, 8]**

**([-22, 5, 3, 11, 26, -6, -7, -8, -9, -8, 26], 2) => [-8, 26]**

**([6, -25, 3, 7, 5, 5, 7, -3, 23], 1) => [6]**/ -->
```
List<int> evenNumbers(List<int> arr, int n) {
  var result = <int>[];
  for (var i = arr.length - 1, count = 0; i >= 0 && count < n; i--) {
    if (arr[i] % 2 == 0) {
      result.add(arr[i]);
      count ++;
    }
  }
  return result.reversed.toList();
}
```
