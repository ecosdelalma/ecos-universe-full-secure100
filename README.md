
# Ecos Universe — Full Secure MVP
## Variables de entorno (Vercel)
- NEXT_PUBLIC_SUPABASE_URL
- NEXT_PUBLIC_SUPABASE_ANON_KEY
## Supabase
1) Auth → Providers → Google (opcional: habilitar y Client ID/Secret)
2) Redirects:
   - Local: http://localhost:3000/auth/v1/callback
   - Prod:  https://TU-DOMINIO/auth/v1/callback
3) SQL Editor → ejecutar `supabase/profiles.sql`
## Rutas
- / (home con video + "ecos")
- /login (email/password + Google)
- /signup (DOB opcional con **Omitir**, confirmación, constelación 'origen' por defecto)
- /dashboard (protegida)
- /profile (protegida, edita perfil)
- /constelacion (interactiva)
## Middleware
Protege /dashboard y /profile. Si no hay sesión, redirige a /login.
