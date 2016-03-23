##Project Assignment
```
1. Your task, for this programming problem, is to break up each of the following functions into two parts as we
discussed in the section on functions and write subroutines that implement those functions in JavaScript.
You may use the JavaScript functions listed in the table below.
<br>
<br>
1.gof(x)=sin2(x)+4sinx+4

<!DOCTYPE html>
<html>
<head>
<title></title>
<meta charset="utf-8" />
</head>
<body>
<input type="button" value="first function" onclick="first()" />
<input type="button" value="second function" onclick="second()" />
<script>
var x = 1;
    
function first(fx) {
          
var fx = Math.pow(x,2) + 4 * x + 4;
            
            document.write(fx);

        }
        function second(gx) {
            var gx = Math.sin(x);
            document.write(gx);
        }
        
    </script>
           

</body>
</html>

2.
<!DOCTYPE html>
<html>
<head>
    <title></title>
	<meta charset="utf-8" />
</head>
<body>
    <input type="button" value="first function" onclick="first()" />
    <input type="button" value="second function" onclick="second()" />
    <script>
        var x = 1;

        function first(fx) {

            var fx = 3 * x + 2;


            document.write(fx);

        }
        function second(gx) {
            var gx = Math.exp(x);
            document.write(gx);
        }
    </script>
</body>
</html>

3.
<!DOCTYPE html>
<html>
<head>
    <title></title>
	<meta charset="utf-8" />
</head>
<body>
    <input type="button" value="first function" onclick="first()" />
    <input type="button" value="second function" onclick="second()" />
    <script>
        var x = 1;

        function first(fx) {

            var fx = Math.log(x+2);


            document.write(fx);

        }
        function second(gx) {
            var gx = Math.cos(x);
            document.write(gx);
        }
    </script>
</body>
</html>

2. In JavaScript, write a program to calculate the squares of integers from 0 to 25. Store this information in an
associative array.

<!DOCTYPE html>
<html>
<head>
    <title></title>
	<meta charset="utf-8" />
</head>
<body>
    <script>
        var squares = new Array();
        squares.length = 26;
        var j = 0;
        for (var i = 0; i < 26; i++) {
            
            
            squares[j] = i * i;
            j++;
            
        }
        var k = 0;
        document.write("Square of numbers are as follow:<br>");
        for (var i = 0; i < 26; i++) {
            
                document.write(i + "*" + i + "=" + squares[k]+"<br>");
               
                k++;
            
        }

    </script>

</body>
</html>

3. Assume that you have an array of positive integers A[0], A[1], ... , A[99]. We have seen that
arrays can be thought of as functions from the set of keys to the set of values. Iterate over the array to find
out how many odd and even numbers exist in the array.


<!DOCTYPE html>
<html>
<head>
    <title></title>
	<meta charset="utf-8" />
</head>
<body>
    <script>
        var arr = new Array();
        arr.length = 100;
        var even = 0;
        var odd = 0;
        var j = 1;
        for (var i = 0; i < 100; i++) {
            arr[i] = j;
            j++;
        }
        for (var k = 0; k < 100; k++) {
            if (arr[k] % 2 === 0) {
                even++;
            }
            else
                odd++;
        }
        document.write("Total even number are:" + even + "<br>");
        document.write("Total odd numbers are:"+odd);
        </script>

</body>
</html>
```
