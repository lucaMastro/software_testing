# ISW2 Exercises
### Software testing module

List of exercises proposed during the course:
#### <a href="#NOGO">Lecture 10 - slide 16 </a>
-[x] installare MVN in locale
-[x] creare un archetipo di progetto Java
-[x] configurare il pom.xml secondo le specifiche informazioni/proprietà
da assegnare al progetto (i.e. meta-data, dipendenze, conf di build)
-[x] creare una semplice classe Java ed aggiungerla al progetto Maven
-[x] fare il build del progetto e ispezionare il contenuto della directory
target \
La directori `target` contiene 3 sottocartelle:
    - `classes`
    - `generated-sourecs/annotations`: la cartella è vuota
    - `maven-status/maven-compiler-plugin/compile/default-compile`: contiene a sua volta
    due files:
        - `createdFiles.lst`
        - `inputFiles.lst`
    
        Approfondire il loro significato.   
     
-[x] versionare il progetto MAVEN su un nuovo repository in GitHub. \
    La directory `target` è stata esclusa dai commit.
-[x] agganciare il repository su CI-Framework configurando l’ambiente di
esecuzione nel file di configurazione (e.g. travis.yaml)
-[x] fare in modo che venga attivato un build in remoto ad ogni commit
-[x] controllare l’esito del build


#### Lecture 10 - slide 17
-[x] dal proprio account GitHub fare fork/clone del
progetto <a href="https://github.com/apache/bookkeeper">Apache Bookkeeper</a> 
-[x] configurare uno spazio di lavoro locale per
Bookkeeper (e.g. download, o clone del fork)
-[x] fare build di Bookkeeper in locale (<a href="https://cwiki.apache.org/confluence/display/BOOKKEEPER/Developer+Setup">wiki</a>)\
fatta skippando i test, perché altrimenti falliva:\
 `mvn clean package -DskipTests`
-[x] ispezionare il contenuto della cartella target\
La cartella contiene solo due elementi:
    - file `.plxarc`: che contiene come unico testo la scritta `maven-shared-archive-resources`
    - directory `maven-shared-archive-resources/META-INF/`: che contiene al suo interno tre file:
        - `DEPENDENCIES`
        - `LICENSE`
        - `NOTICE`
