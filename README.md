# 📦 InSu Web Resource Builder

Strumento dedicato alla creazione, gestione e strutturazione di risorse per il progetto InSu Web.  
Permette di generare oggetti TypeScript coerenti e pronti all’integrazione nel frontend.

## 🚀 Panoramica

**InSu Web Resource Builder** è un tool progettato per semplificare la creazione di dataset strutturati utilizzati nel progetto InSu Web.

L'obiettivo è:
- Standardizzare la creazione delle risorse
- Ridurre errori manuali
- Velocizzare il popolamento dei contenuti
- Garantire coerenza con i modelli TypeScript

## 🧱 Struttura delle Risorse

### 📌 `Resource`

```ts
export class Resource {
    id: number
    resourceName: string
    brief: string
    description: string
    type: ResourceType
    lastUpdate: Date
    banner: string
    files: FileReference[]
}
```

### 📎 `FileReference`

```ts
export class FileReference {
    name: string;
    url: string;
    type: FileType;
}
```

### 🏷️ `ResourceType`

```ts
export enum ResourceType {
    IDEA,
    IN_DEVELOPMENT_PROJECT,
    SCHOOL_BANK,
}
```

## ✨ Funzionalità

- 🧾 Generazione guidata di risorse
- 📂 Gestione file allegati (FileReference)
- 🏷️ Classificazione tramite enum
- 📅 Gestione automatica delle date
- 🧠 Output pronto per TypeScript
- ⚡ Integrazione diretta con frontend NextJS

## 🛠️ Tecnologie

- TypeScript
- Next.js
- TailwindCSS
- React

## 📦 Installazione

```bash
git clone https://github.com/LoRy24/InSu-Web-ResourceBuilder.git
cd InSu-Web-ResourceBuilder
npm install
npm run dev
```

## 🧪 Utilizzo

1. Avvia l’applicazione
2. Compila il form per creare una nuova `Resource`
3. Aggiungi eventuali `FileReference`
4. Ottieni l’output TypeScript pronto all’uso

## 📁 Output

Esempio:

```ts
const resource = new Resource(
  1,
  "Titolo",
  "Breve descrizione",
  "Descrizione completa",
  ResourceType.IDEA,
  new Date(),
  "/images/banner.png",
  [
    new FileReference("Documento", "/files/doc.pdf", FileType.PDF)
  ]
);
```

## 🎯 Obiettivi del Progetto

- Migliorare la produttività nello sviluppo contenuti
- Centralizzare la gestione delle risorse
- Ridurre la duplicazione e inconsistenza dei dati
- Facilitare l’integrazione con il frontend

## 🤝 Contributi

1. Fork del progetto
2. Crea un branch (`feature/nome-feature`)
3. Commit delle modifiche
4. Push
5. Apri una Pull Request

## 📄 Licenza
MIT License
