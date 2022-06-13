<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>Calculate Taxi</title>
</head>
<body>
	<form name="formcalc">
		РОЗРАХУНОК ЧИСТОГО ЗАРОБІТКУ:<p>
		Заробіток, грн: <input type="number" name = "txtnum1">
		<br><br>
		Дистанція, км: <input type="number" name="txtnum2" >
		<br><br>
		Пальне вартість 1л, грн: <input type="number" name="txtnum3" >
		<br><br>
		Розхід на 100км : <input type="number" name="txtnum4" >
		<br><br>
		Амортизація грн/км: <input type="number" name="txtnum5" >
		<br><br>
		<input type="button" value="Calculate" onclick="sumValues()">
		<p>
		Чистий дохід : <input type="number" name="txtres" readonly>

		
	</form>
	<script type="text/javascript">
		
		function sumValues()
		{
			var num1, num2, num3, num4, num5, res;
			num1 = Number(document.formcalc.txtnum1.value);
			num2 = Number(document.formcalc.txtnum2.value);
			num3 = Number(document.formcalc.txtnum3.value);
			num4 = Number(document.formcalc.txtnum4.value);
			num5 = Number(document.formcalc.txtnum5.value);
			res = num1 - (((num4 * num3)/100) * num2) - (num5 * num2)
			document.formcalc.txtres.value=res;
		}

	</script>
</body>
</html>
