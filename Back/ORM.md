### 3.5 Utilisation d'un ORM (Object-Relational Mapping)

**Mécanisme :**

- Utilisation d'un ORM tel que Hibernate pour gérer la persistance des données. Les ORM mappent les objets Java aux tables de la base de données et gèrent automatiquement la création de requêtes SQL sécurisées, réduisant ainsi les risques d'injections SQL.

**Exemple :**

```jsx
// Exemple en Hibernate (JPQL)
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String username;
    private String password;
    // getters and setters
}

public class UserRepository {
    @PersistenceContext
    private EntityManager entityManager;

    public User findByUsername(String username) {
        String jpql = "SELECT u FROM User u WHERE u.username = :username";
        return entityManager.createQuery(jpql, User.class)
                            .setParameter("username", username)
                            .getSingleResult();
    }
}

```