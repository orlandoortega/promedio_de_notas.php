# promedio_de_notas.php
visualizacion de como ver la implementacion de promedio de notas de php con html
<html>
<head>
	<title>promedio de estudiantes</title>
</head>
<body>
	<table border="1" style="margin: 0 auto;">
		<tr>
			<th>nombre</th>
			<th>nota1</th>
			<th>nota2</th>
			<th>nota3</th>
			<th>nota4</th>
			<th>promedio</th>
		</tr>
	</form>
	<?php
		$notas= array("orlando"=>array(10,20,17,15),
              "luna"=>array(20,12,11,20),
              "victor"=>array(10,7,8,15),
              "gerardo"=>array(6,14,15,18));
		
		
		foreach($notas as $clave=>$valor){
			?>
			<tr> 
				<td>
					<?php
					echo "{$clave}";
				?>
				</td>
			
			<?php

			$promedio=0;
			$cont=0;
			foreach($valor as $nota){
				?>
				<td><?php
					echo "{$nota} ";
				?>
				</td>
				<?php
				$promedio+=$nota;
				$cont+=1;

			}
		$promedio=$promedio/$cont;
		?> <td><?php
		echo "{$promedio} ";?>
		</td>
		</tr><?php
		echo "\n";
		}


	?>
</body>
</html>
