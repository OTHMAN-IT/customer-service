Les étapes de création d'un micro service (Customer Service):
------------------------------
Création classe "Customer.java" avec les attributs nécessaires +  les annotations nécessaires JPA(@Entity
@Data @AllArgsConstructor
@NoArgsConstructor @ToString)
------------------------------
Création du Repository "CustomerRepository.java" qui heritera de l'interface JpaRepositroy + l'annotation (@RepositoryRestResource).
@RepositoryRestResource crée le service HATEOAS avec Spring JPA et les opérations seront exposées au format HATEOAS.
------------------------------
Configuration application.properties où on mentionne le port du server + le nom du micro service en cours + la base de donnée ainsi que l'activation du cloud discovery.
------------------------------
L'application est testé par CommandLineRunner est une interface Spring Boot simple avec une méthode run . 
Spring Boot appellera automatiquement la méthode run de tous les beans implémentant cette interface une fois le contexte de l'application chargé.
------------------------------
Les dépendances nécessaires:
-Spring web
-Spring Data JPA
-H2 DataBase
-RestRepositories
-Lombok
-Spring Boot DevTools
-Eureka Discovery Client
-Spring Boot Actuator
