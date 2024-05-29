# 3.2 Gestion des Autorisations (RBAC)

Dans le cadre de notre application, la gestion des autorisations est un élément crucial pour
garantir un accès sécurisé aux fonctionnalités et aux données. Pour cela, nous avons adopté le
modèle de Contrôle d'Accès Basé sur les Rôles (RBAC), qui définit les autorisations en fonction
des rôles des utilisateurs.

**Mécanisme :**

- Mise en œuvre du Contrôle d'Accès Basé sur les Rôles (RBAC) pour contrôler l'accès aux fonctionnalités et aux données.
- Vérification des rôles et des permissions au niveau du back-end.

**Exemple :**

```Java
// Exemple en Java avec Spring Security
@EnableWebSecurity
public class WebSecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
                .antMatchers("/admin/**").hasRole("ADMIN")
                .antMatchers("/client/**").hasRole("CLIENT")
                .antMatchers("/dev/**").hasRole("DEV")
                .anyRequest().authenticated()
            .and()
            .formLogin().permitAll()
            .and()
            .logout().permitAll();
    }
}
````

**Principe du Moindre Privilège :**

- Admin : Accès complet à toutes les fonctionnalités et données.
- Client : Accès limité aux fonctionnalités et données pertinentes à leur rôle.
- Dev : Accès spécialisé aux fonctionnalités et données nécessaires pour le développement.

![Getting Started](/Assets/rbac.png)