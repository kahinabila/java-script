<script>
	document.write("<h1>Les tableax</h1>");
	document.write("Structures contenant plusieurs valeurs de meme type.</br>");
	var tab1 = [1, 2, 3, 4, 5];
	document.write ("<h3>Mon tableau TAB1</h3>");
	for (i = 0; i < tab1.length; i++) {
		document.write("Valeur de la case indice " + i + " : " + tab1[i] + "<br/>");
	}
	var tab2 = new Array(5);
	tab2[0] = "aaa";
	tab2[1] = "bbb";
	tab2[2] = "ccc";
	tab2[3] = "ddd";
	tab2.push ("eee"); //push - for the last valeur
	tab2.push ("fff");
	document.write ("<h3>Mon tableau TAB2</h3>");
	for (i in tab2) {
		document.write("Valeur de la case indice " + i + " : " + tab2[i] + "<br/>");
	}
	document.write ("<h3>EXO1: calculer la somme de TAB1</h3>");
	var s = 0;
	for (i in tab1) {
		//s = s + tab1[i];
		s += tab1[i];
	}
	document.write("La somme de TAB1 est " + s + ".<br/>");
	document.write ("<h2>Les tableaux associatiffs</h2>");
	document.write ("Sont indexes avec chaines de characteres.<br/>");
	var capitales = new Array();
	capitales["France"] = "Paris";
	capitales["Angleterre"] = "Londres";
	capitales["Luxembourg"] = "Luxembourg";
	document.write ("<h3>Mon tableau Capitales</h3>");
	for (i in capitales) {
		document.write("La capital de " + i + " est " + capitales[i] + "<br/>");
	}
	document.write ("<h2>Les tableaux multidimensionnels</h2>");
	var tabart = ["Chemise", "Pantalon", "Chausettes", "Tee-shirt"];
	var tabprxgrd = [40, 120, 15, 10];
	var tabprxmoy = [35, 110, 13, 8];
	var tabprxpet = [30, 100, 11, 6];
	var tab2D=new Array(tabart,tabprxgrd,tabprxmoy,tabprxpet);
	document.write ('<table width="300" border ="1">');
		for(i=0;i<tab2D.length;i++){
			document.write ('<tr>');
				for(j=0;j<tab2D[i].length;j++){
					document.write ('<td>' + tab2D[i][j] + '</td>');
				}
				document.write ('</tr>');
			}
			document.write ('</table><br/>');
			document.write ('<br/>EXO2 :Ajouter une colonne avec les taills.<br/>');
			var tabart = ["Chemise", "Pantalon", "Chausettes", "Tee-shirt"];
			var tabprxgrd = [40, 120, 15, 10];
			var tabprxmoy = [35, 110, 13, 8];
			var tabprxpet = [30, 100, 11, 6];
			var tabtaille = ["grand","moyen","petit"];
			var tab2D=new Array(tabart,tabprxgrd,tabprxmoy,tabprxpet);
			document.write ('<table width="400" border ="1">');
				for(i=0; i<tab2D.length; i++) {
					if(i!=0){
						document.write ('<tr><td>' + tabtaille[i-1] +' </td>');
						}
						else {
							document.write ('<tr><td></td>');
							}
							for(j=0; j<tab2D[i].length; j++) {
								document.write ('<td>' + tab2D[i][j] + '</td>');
							}
							document.write ('</tr>');
						}
						document.write ('</table><br/>');
document.write ('<br/>EXO3 : Mettre la ligne de titre avec les articles.<br/>');

						var tabart = ["Chemise", "Pantalon", "Chausettes", "Tee-shirt"];
						var tabprxgrd = [40, 120, 15, 10];
						var tabprxmoy = [35, 110, 13, 8];
						var tabprxpet = [30, 100, 11, 6];
						var tabtaille = ["grand","moyen","petit",""];
						var tabart2 = [1, 1, 1, 1];
						var tab2D=new Array(tabart,tabprxgrd,tabprxmoy,tabprxpet,tabart2);
						document.write ('<table width="400" border ="1">');
							for(i=0; i<tab2D.length; i++) {
								if(i!=0){
									document.write ('<tr><tr>' + tabtaille[i-1] +' </td>');
									}
									else {
										document.write ('<tr><th></th>');

										}
										for(j=0; j<tab2D[i].length; j++) {
											if(i==0){
											document.write ('<th>' + tab2D[i][j] + '</th>');
										}
										else {
											document.write ('<td>' + tab2D[i][j] + '</td>');
										}
									}

										document.write ('</tr>');
									}
									document.write ('</table><br/>');
					</script>
