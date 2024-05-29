### 3.3 Protection contre les Injections SQL

**Mécanisme :**

- Utilisation de requêtes paramétrées et d'ORM pour interagir avec la base de données de manière sécurisée.

**Exemple :**

```jsx
// Exemple en Java avec JDBC
String query = "SELECT * FROM users WHERE username = ?";
PreparedStatement preparedStatement = connection.prepareStatement(query);
preparedStatement.setString(1, username);
ResultSet resultSet = preparedStatement.executeQuery();

```

**Security Considerations (CSP) :**

- Utilisation de Content Security Policy (CSP) pour limiter l'accès aux ressources.