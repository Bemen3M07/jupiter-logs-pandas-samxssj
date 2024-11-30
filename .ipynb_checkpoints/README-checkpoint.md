[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/ULiw8LbN)
# Empty

Exercici 1
1: Comandes de Linux per analitzar logs

Veure contínuament els logs que es van escrivint a un arxiu:
    Comanda: tail -f <nom_arxiu.log>
Aquesta comanda permet veure les línies afegides en temps real a un fitxer de log.

Cercar una paraula concreta dintre d’un arxiu de log:
    Comanda: grep "paraula" <nom_arxiu.log>
Aquesta comanda busca i mostra totes les línies del fitxer que contenen la paraula especificada.

Si vols cercar sense distingir majúscules de minúscules:
    grep -i "paraula" <nom_arxiu.log>

Si vols comptar les línies on apareix la paraula:
    grep -c "paraula" <nom_arxiu.log>

