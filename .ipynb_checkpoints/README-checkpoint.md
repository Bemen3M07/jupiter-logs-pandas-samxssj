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

Exercici 2
Pregunta:
Què creieu que és millor, mostrar els logs a la terminal durant l'execució del programa o bolcar-los en un fitxer de text?

Resposta:
· Mostrar logs a la terminal és útil per depuració en temps real, especialment durant el desenvolupament.
· Bolcar-los en un fitxer és millor per auditoria, monitoratge, o depuració posterior.
· En entorns de producció, sovint s'utilitza una combinació de tots dos.

 Avantatges i desavantatges de diferents maneres de fer logs

| Exemple                                                                         | Avantatges                                                                                             | Desavantatges                                                                                         |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Fent servir la configuració per defecte del mòdul logging                       | - Fàcil d'implementar, sense gaire configuració prèvia necessària.                                     | - Configuració molt limitada, no pots personalitzar ni escalar.                                       |
| Instanciant un objecte logger i parametritzant-lo des del programa              | - Permet control i flexibilitat en configuració (diferents handlers, formatadors).                     | - Requereix més codi i complexitat en programes grans.                                                |
| Instanciant un objecte logger a partir d’una configuració emmagatzemada a fitxer| - Permet gestionar configuracions complexes i reutilitzar-les fàcilment (ideal per equips grans).      | - Requereix mantenir el fitxer de configuració actualitzat i una càrrega inicial de configuració.     |
