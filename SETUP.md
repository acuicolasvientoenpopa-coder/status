# AcuiCal Status — Configuración

## Requisitos
- Cuenta en GitHub
- Repositorio para el status page

## Pasos

1. **Crear repositorio desde template**
   - Ir a https://github.com/upptime/upptime
   - Click "Use this template"
   - Nombre: `status`
   - Visibilidad: público

2. **Configurar monitoreo**
   - Clonar el repo
   - Reemplazar `.upptimerc.yml` con el archivo de este directorio
   - Commit y push

3. **Agregar dominio custom (opcional)**
   - En el repo, Settings → Pages
   - Custom domain: `status.acuical.com`
   - En Cloudflare, agregar CNAME: `status` → `acuicolasvientoenpopa.github.io`

4. **Notificaciones**
   - Repo → Settings → Secrets → Actions
   - Agregar `GH_PAT` con token de GitHub con scopes `repo` y `workflow`
   - Opcional: configurar Telegram, Slack o correo en el workflow

## URLs monitoreadas

| Servicio | URL |
|---|---|
| App AcuiCal | https://app.acuical.com |
| Landing | https://acuical.com |
| Master Panel | https://master.acuical.com |
| API Health | https://smvjffbeshxcfltjoolm.supabase.co/functions/v1/health |
| Acuarismo | https://acuarismo.acuical.com |
| AcuiGen NFC | https://acuigen.acuical.com |

## Costo
$0 — GitHub Actions free tier tiene 2000 min/mes, Upptime consume ~50 min/mes.
