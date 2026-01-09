DAY Onboarding + Survey (GitHub Pages)

Inside:
- onboarding/index.html  -> router (shows onboarding only the first time)
- onboarding/welcome.html -> intro screen
- onboarding/personalization.html -> topic picker

How to add to your repo:
1) Upload the whole 'onboarding' folder into your repo root (same level as your main index.html).
2) To open onboarding first, link users to:
   your-site/onboarding/index.html
   OR (optional) in your main index.html add:
   window.location.href = "./onboarding/index.html";
3) If your main page is not ../index.html, change it in:
   - welcome.html (2 places)
   - personalization.html (1 place)

Saved data:
- localStorage 'day_preferences_v1' = { topics: [...], savedAt: ... }
- localStorage 'day_onboarded_v1' = "1"

Reset for testing:
localStorage.removeItem('day_onboarded_v1')

✅ ONBOARDING SOLO 1 VEZ
- Se guarda una bandera en el navegador/app: localStorage["day_onboarding_done_v1"] = "1"
- Cuando ya está en "1", /onboarding/index.html manda directo a ../index.html

🔁 Para volver a ver onboarding (solo para pruebas):
- Abre la consola y ejecuta:
  localStorage.removeItem("day_onboarding_done_v1")
