## Base de données intégrées

Une BDD intégrée estu ne base de données qui est intégrée directement dans une application logicielle et fonctionne en mode embarqué. Cela signifie qu'elle est géréee et utilisée par l'application elle-même, sans nécessiter de serveur de base de données externe. Ces BDD sont stockées localement sur le système de l'utilisateur ou dans le répertoire de l'application, et elle sont généralement légères et optimisées pour être rapides et efficaces.

## H2 database

`H2` est l'un des exemples les plus couramment utilisées de BDD intégrées. H2 est une BDD relationnelle écrite en Java qui peut être embarquée dans une application `Spring`. elle prend en charge le mode mémoire (Les données sont stockées en mémoire et sont perdues lorsque l'application est arrêtées) ainsi que le mode fichier (Les données sont stockées dans un fichier sur le système de fichiers de l'ordinateur).

## Optional

`Optional` est une classe générique qui peut contenir soit une valeur non nulle, soit aucune valeur (c'est-à-dire vide) . L'utilisation de `Optional` peut rendre le code plus explicite en indiquant clairement qu'une valeur peut être absente et en forçant les développeurs à traiter ce cas.

## Utilisations courantes de Optional

1. Eviter les `NulPointerException` : 
En utilisant "Optinal" , nous pouvons éviter les erreurs de pointeur nul en vérifiant d'avord si une valeur est présente avant d'essayter d'y accéder. Par exemple:

```java


Optional<String> valeurOptionel = // ... obtenir une valeur, peut-être null

if (valeur Optionel.isPresent()) {
    String valeur = valeurOptionel.get(); // Récupère la valeur présente
    // On fait quelque chose avec la valeur non nulle 
}else {
    //  On fait quelque chose en cas d'absence de valeur 
}


```

2. Chaînage de méthodes:
Nous pouvons chaîner des méthodes pour effetuer des opérations sur la valeru si elle est présente, ou simplement ingorer l'opération si la valeur est absente.

```java

Optional <String> valeur = // ... obtenir une valeur peut - être nulle

valeur.ifPresent(v -> System.out.println("Valeur présent : " + v))

```

3. Traitement des valeurs par défaut:

Nous pouvons spécifier une valeur par défaut à utiliser si la valeur `Optional` est absente, en utilisant la méthode `orElse`

```java

Optional <String> valeur = // ... obtenir une valeur peut - être nulle

valeur.ifPresent(v -> System.out.println("Valeur présent : " + v))
valeur.orElse("Valeur par défaut
")

```