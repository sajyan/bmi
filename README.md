# bmi
<html>
<head><title>BMI計算機</title></head>
<body>
<table>
<tr><td>体重 (Kg):</td><td><input type="text" id="weight_box"></td></tr>
<tr><td>身長 (cm):</td><td><input type= "text" id= "height_box"></td></tr>
<tr><td><button type="button" id="submit" onClick="bmi_calc()">計算</button></td>
<td><div id="bmi">BMI結果</div></td></tr>
</table>
<script type="text/javascript">
const round= (v) => { return (Math.round(v * 10)) / 10; }
const bmi_calc = () => {
const weight= document.getElementById("weight_box").value;
const height= (document.getElementById("height_box").value) / 100;
const bmi = weight / height**2;
let msg = "";
if (bmi < 18.5) {
msg ="低体重";
} else if (18.5 <= bmi && bmi < 25.0) {
msg ="標準体重";
} else if (25.0 <= bmi && bmi < 30.0) {
msg ="前肥満";
} else {
msg ="肥満";
}
document.getElementById ("bmi").innerHTML = "BMI:" + round(bmi) + " " +msg;
}
</script>
</body>
</html>
