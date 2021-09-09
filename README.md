# les2  
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <!-- 1. Почему код даёт именно такие результаты? -->
    <script>
        var a = 1,
            b = 1,
            c, d;
        c = ++a;
        alert(c); // 2 /* ++a означает что мы к переменной а прибавляем единицу */
        d = b++;
        alert(
            d
        ); // 1 /* ++ после переменной означает, что мы прибавляем единицу, но выводим предыдущее значение переменной * /
        c = (2 + ++a);
        alert(
            c
        ); // 5 /* в первом примере мы прибавили единицу в переменную а  и ее значение стало равно двум (2). В данном примере прибавляем еще единицу и а становится равно 3, отсюда ответ 5 * /
        d = (2 + b++);
        alert(
            d
        ); // 4 /* во втором примере мы прибавили единицу в переменную b ее значение стало равно двум (2). В данном примере прибавляем еще единицу и а становится равно 3, но выводим предыдущее значение т.е .2, отсюда получаем 4 * /
        alert(a); // 3	/* прибавили единицу в примере 1 и примере 3 */
        alert(b); // 3	/* прибавили единицу в примере 2 и примере 4 */
    </script>

    <!-- 2. Чему будет равен x в примере ниже? -->
    <script>
        var a = 2;
        var x = 1 + (a *= 2);
        /* X будет равен 5 т.к. оператор *= это сокращенный оператор, полностью он будет выглядеть x = 1 + (a = a * 2 ) */
    </script>

    <!-- 3. Объявить две целочисленные переменные a и b и задать им произвольные начальные значения. Затем 		
            написать скрипт, который работает по следующему принципу:
            * если a и b положительные, вывести их разность;
            * если а и b отрицательные, вывести их произведение;
            * если а и b разных знаков, вывести их сумму;
            ноль можно считать положительным числом. -->
    <script>
        var a = 5;
        var b = 3;
        if (a > 0 && b > 0) {
            x = a - b;
            alert(x);
        } else if (a < 0 && b < 0) {
            x = a * b;
            alert(x);
        } else if (a > 0 && b < 0 || a < 0 && b > 0) {
            x = a + b;
            alert(x);
        }
    </script>

    <!--  4. Присвоить переменной а значение в промежутке [0..15]. С помощью оператора switch организовать вывод 	
           чисел от a до 15. -->
    <script>
        a = +prompt('Введите число от 1 до 15');
        switch (a) {
            case 1:
                alert('Ваше число 1');
                break;
            case 2:
                alert('Ваше число 2');
                break;
            case 3:
                alert('Ваше число 3');
                break;
            case 4:
                alert('Ваше число 4');
                break;
            case 5:
                alert('Ваше число 5');
                break;
            case 6:
                alert('Ваше число 6');
                break;
            case 7:
                alert('Ваше число 7');
                break;
            case 8:
                alert('Ваше число 8');
                break;
            case 9:
                alert('Ваше число 9');
                break;
            case 10:
                alert('Ваше число 10');
                break;
            case 11:
                alert('Ваше число 11');
                break;
            case 12:
                alert('Ваше число 12');
                break;
            case 13:
                alert('Ваше число 13');
                break;
            case 14:
                alert('Ваше число 14');
                break;
            case 15:
                alert('Ваше число 15');
                break;
        }
    </script>

    <!-- 5. Реализовать основные 4 арифметические операции в виде функций с двумя параметрами. Обязательно использовать оператор return. -->
    <script>
        var a = 2;
        var b = 3;

        function plus(a, b) {
            return a + b;
        }

        function minus(a, b) {
            return a - b;
        }

        function div(a, b) {
            return a / b;
        }

        function mult(a, b) {
            return a + b;
        }
    </script>

    <!-- 6. Реализовать функцию с тремя параметрами: function mathOperation(arg1, arg2, operation), где arg1, 	
            arg2 – значения аргументов, operation – строка с названием операции. В зависимости от переданного 		
            значения операции выполнить одну из арифметических операций (использовать функции из пункта 3) и 		
            вернуть полученное значение (использовать switch). -->
    <script>
        function mathOperation(arg1, arg2, operation) {
            switch (operation) {
                case 'сложение':
                    return arg1 + arg2;
                    break;
                case 'вычитание':
                    return arg1 - arg2;
                    break;
                case 'деление':
                    return arg1 / arg2;
                    break;
                case 'умножение':
                    return arg1 * arg2;
                    break;
            }
        }
    </script>
    <script>
        null == 0 // false
        null == "" // false
        undefined == 0 // false
        undefined == "" // false
        null == undefined // true
        0 == "" // true
        //Почему null == 0 // false 
        //ведь null ToNumber +0
    </script>

</body>

</html>
