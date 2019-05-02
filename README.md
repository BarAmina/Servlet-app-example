# Servlet-app-example
une application java introductif avec servlet
Le projet my-servlet-app contient 2 exemples basiques de servlet avec code facilement à comprendre 
Ce projet permet de comprendre le fonctionnement basique des servlets, les filtres et comment les requêtes et leurs réponses sont utilisées pour échanger les données 

La structure générale du projet :
-	src :
       -main -->java -->com--> hatim--> app-->  AppServlet.java
                                           --> HelloServlet.java
                                           -->SecurityFilter.java
             -->webapp --> WEB-INF -->web.xml

     -test --> java --> com --> hatim --> app -->  AppTest.java
- target
- pom.xml


Points à noter:

-le fichier pom.xml contient la définition de 2 dépendances :la dépendance JUNIT et la dépendance javax-servlet

-la classe Appservlet.java est une servlet qui demande le nom d’utilisateur en utilisant la méthode doGet()
(Quand l’utilisateur entre un url dans un browser ; celui-ci envoie une requête et la méthode doGet() est appelée par le container Tomcat. Cette méthode utilise l’objet PrintWriter qui permet d’envoyer le contenu du document réponse vers le Browser)

-la classe HelloServlet.java représente la 2ème servlet qui affiche le nom de l’utilisateur ajouté comme paramètre.

-la classe SecurityFilter est un filtre comme son nom l’indique ; c’est un composant java utilisé pour qu’il intercepte, si il y a une erreur, les requêtes avant leur envoi vers les servlet et aussi avant que la réponse n’est envoyé vers le client

-le fichier web.xml permet la configuration des 2 servlets en utilisant la balise <servlet> pour définir le nom de la servlet et le nom de la classe de la servlet ,et la balise<web-mapping> pour définir l’url-pattern de la servlet.
