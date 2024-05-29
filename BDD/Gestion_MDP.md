### 4.2 Gestion des Mots de Passe

**Mécanisme :**

- Hachage et salage des mots de passe des utilisateurs avec une fonction de hachage sécurisée (par exemple, BCrypt).

**Exemple :**

```jsx
// Exemple en Java avec BCrypt
import org.springframework.security.crypto.bcrypt.BCryptPasswordEncoder;

public class PasswordUtil {
    private static final BCryptPasswordEncoder passwordEncoder = new BCryptPasswordEncoder();

    public static String hashPassword(String plainPassword) {
        return passwordEncoder.encode(plainPassword);
    }

    public static boolean checkPassword(String plainPassword, String hashedPassword) {
        return passwordEncoder.matches(plainPassword, hashedPassword);
    }
}

```

**Security Considerations (SRI) :**

- Utilisation de Subresource Integrity (SRI) pour garantir l'intégrité des ressources externes chargées dans votre application.