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


Llibreries de logs en altres llenguatges

| Característica                             | Python (logging)                                                                                 | Java (Log4j)                                                                   |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Nom de la llibreria                        | logging                                                                                          | Log4j                                                                          |
| És nativa del llenguatge?                  | Sí, inclosa a la llibreria estàndard.                                                            | No, s'ha d'importar com una dependència externa.                               |
| URL per descarregar-se la llibreria        | [https://docs.python.org/3/library/logging.html](https://docs.python.org/3/library/logging.html) | [https://logging.apache.org/log4j/2.x/](https://logging.apache.org/log4j/2.x/) |
| Inicialització de l’objecte de logger      | `logger = logging.getLogger('nom_logger')`                                                       | Declaració en el codi o configuració al fitxer `log4j2.xml`                    |
| Nivells de log disponibles                 | DEBUG, INFO, WARNING, ERROR, CRITICAL                                                            | TRACE, DEBUG, INFO, WARN, ERROR, FATAL                                         |
| Mètode per fer log                         | `logger.info("Missatge")`, `logger.error("Error!")`                                              | `logger.info("Missatge");`, `logger.error("Error!");`                          |
| Tipus de manegadors (pantalla, fitxer...)  | `StreamHandler`, `FileHandler`, `SMTPHandler`, `RotatingFileHandler`                             | `ConsoleAppender`, `FileAppender`, `RollingFileAppender`, `SocketAppender`     |
| Opcions de format                          | Utilitza `Formatter`: `%(asctime)s - %(levelname)s - %(message)s`                                | Es defineixen a `PatternLayout` (per ex., `%d{ISO8601} %p - %m%n`)             |


Exercici 3: Aplicació amb introducció de dades i generació de gràfiques

Eines proposades

1. Pandas
   - Funcionalitat: 
     Pandas és una llibreria de Python per a la manipulació i anàlisi de dades estructurades. Permet treballar amb dades tabulars (en format de taula, com els fitxers CSV o Excel) de manera senzilla, amb operacions com filtres, agrupacions, unió de taules, i càlculs estadístics.
   - Ús: 
     És ideal per carregar, netejar i preparar dades per a la seva visualització o anàlisi.
   - Prova:
     Fitxer CSV carregat i analitzat amb Pandas. (Codi i fitxers CSV en el directori comú).

2. Jupyter Notebook
   - Funcionalitat:
     Jupyter Notebook és una eina interactiva que permet crear i compartir documents amb codi en Python, visualitzacions i text explicatiu en format Markdown. És ideal per al desenvolupament iteratiu i per presentar els resultats de forma clara.
   - Ús: 
     És útil per combinar codi, explicacions i gràfiques en un mateix document.
   - Prova:
     Codi que genera un gràfic simple dins un Notebook. (Codi i fitxers CSV en el directori comú).

3. ReportLab
   - Funcionalitat:
     ReportLab és una llibreria de Python per generar documents PDF. Permet afegir text, gràfics i imatges de forma programada, útil per crear informes automàtics.
   - Ús:
     S’utilitza per generar un informe PDF amb dades i gràfiques generades a partir de les altres eines.
   - Prova:
     Exemple de codi per generar un PDF amb text i gràfiques. (Codi i fitxers CSV en el directori comú).

---

Decisió final sobre eines i llibreries

Per a l'aplicació que es vol desenvolupar, s'han triat les següents eines:
- Pandas: Per carregar i manipular les dades des de fitxers JSON, TXT o CSV.
- Jupyter Notebook: Per desenvolupar i provar el codi de manera interactiva, i per presentar les gràfiques.
- ReportLab: Per generar informes finals en PDF amb les gràfiques i resultats obtinguts.

Argumentació:
- Pandas és imprescindible per gestionar les dades d'una manera eficient i flexible.
- Jupyter Notebook proporciona una manera intuïtiva de combinar desenvolupament i documentació.
- ReportLab permet crear un informe professional amb els resultats finals, cosa que és molt útil per presentar la informació als treballadors.

---

Exercici 4 al notebook complet i explicat

Exercici 5: 
Anàlisi de dades dels alumnes
Resultats obtinguts:
1. Mitjana de nota final per alumne: Es mostre a la taula al Notebook.
2. Mitjana general de tots els alumnes: 7.01
3. Percentatge d'aprovats i suspesos: 
   - Aprovats: 100%
   - Suspesos: 0%
4. Nota més alta i més baixa:
   - Nota més alta: 8.50 (Alumne: Lopez)
   - Nota més baixa: 5.50 (Alumne: Ruiz)
5. Alumnes amb totes les notes ≥ 7: Es mostre a la taula al Notebook.

Exercici 6: Gràfics de dades visuals

Gràfic 1: Mitjana de notes per alumne
Gràfic 2: Percentatge d'aprovats i suspesos
Gràfic 3: Mitjana de les notes per assignatura
Gràfic 4: Relació entre les notes M01 i M04
