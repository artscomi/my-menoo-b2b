# Deploy su Vercel (nuovo progetto)

Questa cartella è una copia del progetto. Per pubblicarla come **nuovo** progetto su Vercel:

## Opzione 1: Deploy da GitHub

1. **Crea un nuovo repository su GitHub**
   - Vai su [github.com/new](https://github.com/new)
   - Nome es. `diet-pwa-app-2` (o come preferisci)
   - Non inizializzare con README (la cartella ha già i file)

2. **Collega questa cartella al nuovo repo**
   ```bash
   cd /Users/cristina.luerti/Desktop/personal-projects/diet-pwa-app-copy
   git init
   git add .
   git commit -m "Initial commit - copia progetto"
   git branch -M main
   git remote add origin https://github.com/TUO_USERNAME/NOME_REPO.git
   git push -u origin main
   ```

3. **Crea il progetto su Vercel**
   - Vai su [vercel.com/new](https://vercel.com/new)
   - Clicca **"Import Git Repository"** e seleziona il nuovo repo
   - Assegna un nome al progetto (es. `diet-pwa-app-2`)
   - Clicca **Deploy**

## Opzione 2: Deploy con Vercel CLI

1. **Installa Vercel CLI** (se non l’hai già)
   ```bash
   npm i -g vercel
   ```

2. **Deploy dalla cartella del progetto duplicato**
   ```bash
   cd /Users/cristina.luerti/Desktop/personal-projects/diet-pwa-app-copy
   vercel
   ```
   - Accedi/registrati se richiesto
   - Scegli **"Create new project"** quando chiede di linkare a un progetto esistente
   - Assegna un nome al progetto

Per deploy successivi dalla stessa cartella: `vercel --prod`

---

**Nota:** Variabili d’ambiente (es. chiavi API OpenAI) vanno configurate nel progetto Vercel:  
Dashboard Vercel → progetto → **Settings** → **Environment Variables**.
