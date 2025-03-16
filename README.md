# Prise en main de la bibliotheque Pddl4j. Guide d'Installation et d'Exécution de pddl4j

Ce guide explique comment configurer et exécuter un exemple avec pddl4j.

## Étapes à Suivre

1. **Télécharger JDK et JRE Java** :
   - Téléchargez JDK sur [ce liens](https://www.oracle.com/java/technologies/downloads/)
   - Téléchargez JRE sur [ce lien](https://www.java.com/fr/download/manual.jsp)

2. **Télécharger Gradle** :
   - Téléchargez Gradle depuis [ce lien](https://gradle.org/install/).
   - creer un dossier C:\Gradle et y extraire les fichiers.
   - Ajouter le path C:\Gradle\gradle-8.13\bin dans les variables d'environnement

3. **Créer la Structure des Dossiers** :
   - Créez un dossier pour le projet.
   - Dans ce dossier, créez les sous-dossiers suivants :
     ```
     src/fr/uga/pddl4j/examples
     classes
     lib
     ```

4. **Télécharger le Binary pddl4j** :
   - Exécutez la commande suivante pour télécharger le fichier `pddl4j-4.0.0.jar` :
     ```
     Invoke-WebRequest -Uri "http://pddl4j.imag.fr/repository/pddl4j/binaries/pddl4j-4.0.0.jar" -OutFile "lib/pddl4j-4.0.0.jar"
     ```
    - Deplacer le fichier dans le dossier lib avec la commande suivante:
    - ```
      mv pddl4j-4.0.0.jar lib/pddl4j-4.0.0.jar
      ```

5. **Compiler l'Exemple** :
   - Compilez l'exemple avec la commande suivante :
     ```
     javac -d classes -cp lib/pddl4j-4.0.0.jar src/fr/uga/pddl4j/examples/ProblemInstantiationExample.java
     ```

6. **Exécuter l'Exemple** :
   - Exécutez l'exemple avec la commande suivante :
     ```bash
     java -cp "classes;lib/pddl4j-4.0.0.jar" fr.uga.pddl4j.examples.ProblemInstantiationExample "src/test/resources/benchmarks/pddl/ipc2000/logistics/strips-typed/domain.pddl" "src/test/resources/benchmarks/pddl/ipc2000/logistics/strips-typed/p01.pddl"
     ```

7. **Fichiers PDDL** :
   - Les fichiers `domain.pddl` et `p01.pddl` se trouvent dans les benchmarks. Vous pouvez les télécharger depuis [ce lien](https://github.com/pellierd/pddl4j/tree/master/src/test/resources/benchmarks/pddl/ipc2000/logistics/strips-typed).

