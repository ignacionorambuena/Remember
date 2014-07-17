$reg=mysql_query("select * from region",$link);
while($rowReg=mysql_fetch_array($reg)){
?>
<div class="checkbox">
<label>
<input type="checkbox" name="region[]" value="<?php echo $rowReg['idReg']; ?>" <?foreach ($region as &$key) { if($key==$rowReg['idReg']){echo "checked"; }}?>>
<?php echo $rowReg['nameReg'];?>
</label>
</div>
<?
}
