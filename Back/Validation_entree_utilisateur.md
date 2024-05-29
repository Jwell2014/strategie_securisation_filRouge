### 3.4 Validation des Entrées Utilisateur

**Mécanisme :**

- Validation et filtrage des entrées côté serveur pour empêcher les injections de code et les attaques XSS.

**Exemple :**

```jsx
// Exemple en Java avec Spring
@Controller
public class UserController {

    @PostMapping("/submit")
    public String submit(@RequestParam("input") String input, Model model) {
        String sanitizedInput = input.replaceAll("[<>]", "");
        model.addAttribute("input", sanitizedInput);
        return "result";
    }
}

```