PROJECT ASSIGNMENT

1. We’ve seen that counting common elements between sets is crucial to counting the total number of elements in their union. For this assignment, write a function in JavaScript that takes two arrays as inputs and returns the number of common elements between them. For simplicity, assume that the arrays contain all distinct values.



<!--
    1. We’ve seen that counting common elements between sets is crucial to counting the total number of
elements in their union. For this assignment, write a function in JavaScript that takes two arrays as inputs
and returns the number of common elements between them. For simplicity, assume that the arrays
contain all distinct values.

-->


<!DOCTYPE html>

<html>
<head>
    <title></title>
	<meta charset="utf-8" />
</head>
<body>
    <script>
        
        var arr1 = [1, 2, 3, 4, 5];
        var arr2 = [2, 5, 6, 7, 8];
        for (var i = 0; i < arr1.length; i++) {
            for (var j = 0; j < arr2.length; j++) {
                if (arr1[i] == arr2[j]) {
                    document.write(arr1[i] +"<br>");
                }
                else { }
            }
        }
    </script>

</body>
</html>






2. In JavaScript, implement the p(n,k) and c(n,k) functions and . You may use the function fact(n) defined in the chapter in your code or write your own that calculates the factorial of. There are a number of ways you can write the factorial function. Be as creative as you can!



<!DOCTYPE html>

<!--
    2. In JavaScript, implement the p(n,k) and c(n,k) functions and . You may use the function fact(n) defined in
the chapter in your code or write your own that calculates the factorial of . There are a number of ways
you can write the factorial function. Be as creative as you can!

-->
<html>
<head>
    <title></title>
	<meta charset="utf-8" />
    

</head>
<body>
    N:<input type="number"  id="n1" name="n1"  placeholder="Enter n:" class="i1" />
    r:<input type="number"  id="n2" name="n2"  placeholder="Enter r:" class="i2" />
    <input type="button" value="Calculate Combination" onclick="combination()"/>
    <input type="button" value="Calculate Permutation" onclick="permutation()" />
    
    <script>
        
       
        function combination() {
           

            var n = document.getElementById("n1").value;

            var r = document.getElementById("n2").value;
           

            var comb=(fact(n)/(fact(r)*fact(n-r)));
            document.write(comb);

        }
        function permutation() {


            var n = document.getElementById("n1").value;

            var r = document.getElementById("n2").value;


            var comb = (fact(n) / (fact(n - r)));
            document.write(comb);

        }
        function fact(num) {
            var fact = 1;
            while (num !== 0) {
                fact *= num;
                num--;
            }
            return fact;
        }


    </script>
</body>
</html>


