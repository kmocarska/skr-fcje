1
```bash
#Karolina Mocarska
#Napisz funkcję posiadającą 2 argumenty będące przekątnymi deltoidu ("latawiec") i obliczające pole ze wzoru P=ef/2. Przetestuj działanie tej funkcji.

pole()
{
	echo $[$1*$2/2];
	
}

pole 5 30
```

2

```bash
#Karolina Mocarska
#Napisz funkcję obliczająca wartość wyrażenia zadanego wzorem:f(x) = { 1 dla x>0, 0 dla x=0, -1 dla x<0.

f()
{
	x=$1
	
	if [ $x -gt 0 ]
	then
		wynik=1
	elif [ $x -eq 0 ]
	then 
		wynik=0
	else
		wynik=-1
	fi

	echo "dla x = $x    =>    F($x) = $wynik"
}

echo -n "podaj X: "
read xx
f $xx
```

3

```bash
#Karolina Mocarska
#Napisz funkcję obliczającą a do n, a - liczba całkowita, n - liczba naturalna (z zerem). Funkcja ma posiadać dwa argumenty a i n. Przetestuj działanie tej funkcji.

f()
{
	
	a=$1
	n=$2
	t=$a;
	
	if [ $n -gt 0 ] #czy potega jest liczba naturalna
	then
		i=1;
		while [ $i -lt $n ]
		do			
			t=$[t*a];
			i=$[i + 1];
		done
		
		echo "Liczba $a do potęgi $n wynosi: $t";

	else
		echo "Potęga nie jest liczba naturalna.";
	fi

}

echo -n "   Liczba: "
read a;

echo -n  "do potęgi: "
read n;

f $a $n;
```

4

```bash
#Karolina Mocarska
#Napisz rekurencyjną definicję funkcji obliczającą silnię ze swojego argumentu. (n!=1*2*3*...*n) Przetestuj działanie tej funkcji.

silnia()
{
	if [ $1 -ge 0 ]
	then
		t=1;
		i=1;
		while [ $i -le $1 ]
		do
			t=$[t * i];
			i=$[i + 1];
		done
		return $t;
	else
		echo "N nie jest liczbą naturalną";
		exit;
	fi
}

echo "Program Obliczający silnię.";
echo -n "n! := "; 
read input;

silnia $input;
echo "$input! = $t";
exit 0;
```

5 

```bash
#Karolina Mocarska
#Napisz skrypt wczytujący 5 imion (użyj tablic), sortujący imiona w kolejności alfabetycznej (tak jak w książce telefonicznej) i wypisujący posortowane imiona na ekranie.

echo "Podaj Imie nr. 1: ";
read name[1];

echo "Podaj Imie nr. 2: ";
read name[2];

echo "Podaj Imie nr. 3: ";
read name[3];

echo "Podaj Imie nr. 4: ";
read name[4];

echo "Podaj Imie nr. 5: ";
read name[5];
```
