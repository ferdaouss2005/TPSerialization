# TPSerialization
# TP Java – Sérialisation et Désérialisation

## Exercice 1 : Sérialisation et Désérialisation avec Serializable


<img width="550" height="148" alt="image" src="https://github.com/user-attachments/assets/a47c6e39-5c55-4e15-91c4-bb4e0057d4d1" />


### Résumé
Cet exercice consiste à sauvegarder et récupérer des objets Java à l'aide de la sérialisation et de la désérialisation. La classe `Employee` implémente l'interface `Serializable` afin de permettre l'enregistrement des objets dans un fichier binaire. La classe `SerializationUtil` utilise `ObjectOutputStream` et `ObjectInputStream` pour écrire et lire une liste d'employés. Le mot-clé `transient` permet d'exclure le mot de passe de la sérialisation, tandis que `serialVersionUID` permet de gérer la version de la classe.

### Classes réalisées
- `Employee.java`
- `SerializationUtil.java`
- `Main.java`

### Résultat
Les trois employés sont correctement sauvegardés puis récupérés depuis le fichier `employees.ser`. Le champ `password` affiche `null` après la désérialisation car il est déclaré `transient`.

---

## Exercice 2 : Sérialisation avancée avec 


<img width="614" height="195" alt="image" src="https://github.com/user-attachments/assets/fe720210-ef1c-4991-af81-70761e1345ee" />


### Résumé
Cet exercice permet de découvrir l'interface `Externalizable`, qui offre un contrôle manuel sur la sérialisation et la désérialisation des objets. La classe `ChatMessage` implémente les méthodes `writeExternal()` et `readExternal()` pour écrire et lire les données dans un ordre précis. Une version du format binaire est également utilisée pour gérer les évolutions. Le champ `length`, déclaré `transient`, est recalculé après la lecture du message.

### Classes réalisées
- `ChatMessage.java`
- `ChatHistory.java`
- `Main.java`

### Résultat
L'historique des messages est sauvegardé dans le fichier `chat.ser`, puis chargé correctement. Les messages sont affichés avec leur date d'envoi et leur longueur.

---

## Conclusion générale

Ces deux exercices m'ont permis de comprendre les différents mécanismes de sérialisation en Java. Le premier exercice utilise `Serializable` pour une sérialisation automatique des objets, tandis que le deuxième utilise `Externalizable` pour contrôler manuellement les données enregistrées et récupérées. J'ai également appris à utiliser les champs `transient`, à gérer les versions de sérialisation et à manipuler les flux d'entrée et de sortie avec Java.
