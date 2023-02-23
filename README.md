# RANDOM PARALLEL TESTING   
## USING RANDOOP AND EMMA

GitHub Actions per il testing parallelo randomico di classi java utilizzando randoop per la generazione dei test ed Emma per ottenere il report sulla coverage.

## Utilizzo

- Carica il file .jar nella repository all' interno della directory "jars".
- Modifica il file "lista.txt" inserendo il nome delle classi da testare.
- Modifica lo script main.yml inserendo appositamente il nome del progetto da testare in Emma instr(rigo 46) e in Randoop(rigo 49). 
- Runnare il workflow manualmente dalla sezione "Action"(se è la prima esecuzione assicurarsi di aver correttamente eliminato la cartella merge/coverage), finchè non si ottiene una coverage soddisfacente, o la stessa si stabilizza.


## Output


L' action genera nella repository la cartella merge/coverage, in cui sono presenti i file di coverage, ottenuti dal merge delle sessioni parallele e il merge con il risultato della precedente esecuzione

Al termine di ogni esecuzione GitHub Action saranno creati 2 Artifacts(Si trovano in basso nella sezione summary).
- Emma Reports, che contiene le cartelle "coverage_?", in cui sono presenti i report parziali "coverage_?.html" delle singole sessioni e i test generati che trovano un fallimento.
- Coverage, che contiene il report "coveragemerge.html" finale sulla copertura di tutti i test eseguiti.

Cliccando sugli Artifacts vengono scaricati i .zip.

## COVERAGE

![Coverage Badge](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/Giovannircc/99488398e05ca4ebe8bddedc60dbc49e/raw/ParallelRandomTesting__.json)

![Coverage Badge](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/Giovannircc/99488398e05ca4ebe8bddedc60dbc49e/raw/ParallelRandomTesting2__.json)

![Coverage Badge](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/Giovannircc/99488398e05ca4ebe8bddedc60dbc49e/raw/ParallelRandomTesting3__.json)

![Coverage Badge](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/Giovannircc/99488398e05ca4ebe8bddedc60dbc49e/raw/ParallelRandomTesting4__.json)


### Note

A causa di alcuni problemi di comunicazione della piattaforma GitHub con GitHubGist, su cui vengono memorizzati i badge, gli stessi potrebbero non risultare aggiornati subito dopo l' esecuzione del workflow. Per visualizzare correttamente i valori di coverage si consiglia di attendere qualche minuto e riaggiornare la pagina della repository
