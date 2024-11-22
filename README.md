# Info_lesson-57 
1. Линейные алгоритмы выполняются последовательно, Разветвляющиеся алгоритмы включают в себя условия, которые определяют, какой путь выполнения будет выбран в зависимости от истинности или ложности определённых условий
2. некоторые задачи требуют принятия решений на основе условий. задачи где необходимо сравнивать элементы между собой.
3. если програама легкая то да, но основном нет
4. изначально значение переменной b будет перезаписано значением -a, и в результате оба переменных будут иметь одно значение, вместо обмена
5.  Полные условные операторы имеют все возможные ветвления, в то время как неполные указывают только часть условий. В некоторых задачах можно обойтись только неполной формой, если не требуется учитывать все возможные варианты
6.  < > = <>
7.  состоит из нескольких простых условий, связанных логическими операторами и используется для проверки нескольких условий одновременно
8.   определяется по правилам приоритета логических операторов, где NOT имеет наивысший приоритет, затем AND, и в конце OR.
9.   ля выполнения разных действий в зависимости от значения переменной. Без него можно использовать цепочку условных операторов if, однако это усложнит код и сделает его менее читаемым
10.   В школьном алгоритмическом языке оператор выбора может быть более специфичным и удобным в использовании, тогда как в Паскале используется конструкция case, которая более формальна и требует строгого указания переменных
11.   else, чтобы указать действия, если ни одно из условий не подошло
12.   нужно обернуть эти операторы в begin и end, например: case x of 1: begin writeln('Выбор 1'); writeln('Действие 1'); end; 2: writeln('Выбор 2'); end;



ЗАДАЧИ 

1.  когда все три числа одинаковые
2.   var a,b,c,d,e,max,min:integer; begin readln(a,b,c,d,e); max:=a; if b>max then max:=b; if c>max then max:=c; if d>max then max:=d; if e>max then max:=e; min:=a; if b<min then min:=b; if c<min then min:=c; if d<min then min:=d; if e<min then min:=e; writeln('Максимальное число: ',max); writeln('Минимальное число: ',min); end
3.   Программа для проверки трёхзначности числа: var x: integer; begin write('Введите число: '); readln(x); if ((x>=100) and (x<=999)) then writeln('Число является трёхзначным') else writeln('Число не является трёхзначным'); end.
4.   var month: integer; begin writeln('Введите номер месяца: '); readln(month); if (month>=3) and (month<=5) then writeln('Весна') else if (month>=6) and (month<=8) then writeln('Лето') else if (month>=9) and (month<=11) then writeln('Осень') else if (month=12) or (month<=2) then writeln('Зима') else writeln('Ошибка: неверный номер месяца'); end
5.   var month: integer; begin writeln('Введите номер месяца: '); readln(month); case month of 3,4,5: writeln('Весна'); 6,7,8: writeln('Лето'); 9,10,11: writeln('Осень'); 12,1,2: writeln('Зима'); else writeln('Ошибка: неверный номер месяца'); end; end.
6.   var month,days:integer; begin write('Введите номер месяца: '); readln(month); case month of 1,3,5,7,8,10,12: days:=31; 4,6,9,11: days:=30; 2: days:=28; else begin writeln('Ошибка: неверный номер месяца'); exit; end; end; writeln('Число дней: ',days); end.
7.   var month, day, days, days_in_month:integer; begin write('Введите номер месяца и день: '); readln(month, day); if (month<1) or (month>12) or (day<1) or (day>31) then begin writeln('Ошибка: неверный номер месяца или день'); exit; end; days:=0; days_in_month:=31; repeat case month of 4,6,9,11: days_in_month:=30; 2: days_in_month:=28; end; days:=days+days_in_month-day; month:=month+1; day:=0; until month=13; writeln('Дней до Нового года: ', days); end.
8.   var age: integer; begin write('Введите возраст: '); readln(age); case age of 1..4, 21..24, 31..34, 41..44, 51..54, 61..64, 71..74, 81..84, 91..94, 101..104, 111..114: writeln(age,' года'); 0, 5..20, 25..30, 35..40, 45..50, 55..60, 65..70, 75..80, 85..90, 95..100, 105..110, 115..120: writeln(age,' лет'); else writeln('Ошибка: неверное значение возраста'); end; end.
9.   var x,n: integer; s: string; begin write('Введите число: '); readln(x); if (x>100) then begin writeln('Ошибка: число не должно превышать 100'); exit; end; case x of 1: s:='один'; 2: s:='два'; 3: s:='три'; 4: s:='четыре'; 5: s:='пять'; 6: s:='шесть'; 7: s:='семь'; 8: s:='восемь'; 9: s:='девять'; 10: s:='десять'; 11: s:='одиннадцать'; 12: s:='двенадцать'; 13: s:='тринадцать'; 14: s:='четырнадцать'; 15: s:='пятнадцать'; 16: s:='шестнадцать'; 17: s:='семнадцать'; 18: s:='восемнадцать'; 19: s:='девятнадцать'; 20: s:='двадцать'; 30: s:='тридцать'; 40: s:='сорок'; 50: s:='пятдесят'; 60: s:='шестьдесят'; 70: s:='семьдесят'; 80: s:='восемьдесят'; 90: s:='девяносто'; 100: s:='сто'; else begin n:=x div 10 * 10; s:=s+' '+s(n mod 100); if (x mod 10 > 0) then s:=s+' '+s(x mod 10); end; end; writeln(s); end.
10.    var x,y: real; begin write('Введите координаты: '); readln(x, y); if ((y<=(-x)) and (y>=(-2-x)) and (y>=0.5) or ((y>=(-x)) and (y<=(-2-x)) and (y<=0.5))) then writeln('Точка попадает в заштрихованную область') else writeln('Точка не попадает в заштрихованную область'); end.
