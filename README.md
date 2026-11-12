<div align="center">

<img src="docs/media/hero.svg" alt="Money Guard — a personal finance tracker built by a team" width="100%">

<p>
  <a href="https://money-guard-app-eight.vercel.app"><img alt="Live" src="https://img.shields.io/badge/live-open%20Money%20Guard-8b5cf6?style=for-the-badge&labelColor=0b0716"></a>
  <img alt="Redux Toolkit" src="https://img.shields.io/badge/Redux%20Toolkit-persist-ffb627?style=for-the-badge&labelColor=0b0716">
  <img alt="Chart.js" src="https://img.shields.io/badge/Chart.js-statistics-24cca7?style=for-the-badge&labelColor=0b0716">
  <img alt="Team" src="https://img.shields.io/badge/GoIT-team%20project-8b5cf6?style=for-the-badge&labelColor=0b0716">
</p>

<p><em>A fully responsive personal finance app built with React and Redux by a team.<br>
Register, record income and expenses, watch your balance update and read your statistics.</em></p>

<table>
  <tr>
    <td width="60%"><img src="public/GitHubImages/Desktop1.png" alt="Desktop dashboard"></td>
    <td width="20%"><img src="public/GitHubImages/mobile-1.png" alt="Mobile"></td>
    <td width="20%"><img src="public/GitHubImages/mobile-2.png" alt="Mobile statistics"></td>
  </tr>
</table>

</div>

<img src="docs/media/divider.svg" width="100%" alt="">

## Features

| | |
|---|---|
| **Authentication** | Register, log in and log out; the JWT is persisted with redux-persist. |
| **Transactions** | Create, read, update and delete income and expenses, in a table on desktop and cards on mobile. |
| **Quick add** | A floating "+" button and modal add / edit forms with react-hook-form, Yup and a date picker. |
| **Balance** | The total balance stays in sync automatically. |
| **Statistics** | Monthly breakdowns with Chart.js. |
| **Currency** | Exchange rates from the Monobank API. |
| **Feedback** | Toast-based error handling and loaders. |

```mermaid
flowchart LR
  UI[React · mobile first] --> ST[(Redux Toolkit · persisted)]
  ST --> TH[Async thunks · Axios] --> API[Wallet API]
  ST --> CH[Statistics · Chart.js]
  MB[Monobank API] --> CUR[Currency widget]
```

<img src="docs/media/divider.svg" width="100%" alt="">

## Türkçe özet

**Money Guard**, React ve Redux ile ekip olarak geliştirdiğimiz, tamamen duyarlı bir kişisel finans uygulaması. Kullanıcılar kayıt olup gelir ve gider işlemleri ekleyebiliyor, düzenleyip silebiliyor; bakiye anlık güncelleniyor, aylık istatistikler grafikle gösteriliyor ve döviz kurları takip ediliyor. Bu projede işlem ekleme/düzenleme akışından ve modallardan sorumluydum.

<img src="docs/media/divider.svg" width="100%" alt="">

<h2 id="team-members">👥 Team Members & Responsibilities</h2>

<h3>👤 Egemen — Architecture, Auth Core & Global State</h3>
<ul>
  <li>Redux store configuration</li>
  <li>JWT persistence (redux-persist)</li>
  <li>Login & Register operations</li>
  <li>Private/Public routing</li>
  <li>Global loader implementation</li>
</ul>

<h3>👤 Gülnihan — Auth Pages & UI Layout</h3>
<ul>
  <li>Registration & Login pages</li>
  <li>Form validation logic</li>
  <li>Password strength indicator</li>
  <li>Header & Logout flow</li>
</ul>

<h3>👤 Hatice — Dashboard & Transactions List</h3>
<ul>
  <li>Dashboard layout</li>
  <li>Navigation</li>
  <li>TransactionsList rendering</li>
  <li>Desktop & Mobile transaction layout</li>
  <li>Balance component</li>
</ul>

<h3>👤 Kutluhan — Transaction CRUD & Modals</h3>
<ul>
  <li>Floating Add Transaction button</li>
  <li>ModalAddTransaction</li>
  <li>AddTransactionForm (react-hook-form + Yup)</li>
  <li>ModalEditTransaction</li>
  <li>EditTransactionForm</li>
  <li>Delete transaction logic</li>
  <li>Auto balance synchronization</li>
</ul>

<h3>👤 Nur Seda — Statistics & Currency</h3>
<ul>
  <li>Monthly statistics queries</li>
  <li>Chart.js integration</li>
  <li>Statistics filtering (month/year)</li>
  <li>Monobank API integration</li>
  <li>LocalStorage currency cache logic</li>
</ul>

<hr />

<h2>🔗 Team Links</h2>

<ul>
  <li>Egemen Yılmaz — 
    <a href="https://www.linkedin.com/in/egemen-y%C4%B1lmaz/" target="_blank">LinkedIn</a> | 
    <a href="https://github.com/Egemen-Yilmaz" target="_blank">GitHub</a>
  </li>

  <li>Hatice van Daalen — 
    <a href="https://www.linkedin.com/in/haticevand/" target="_blank">LinkedIn</a> | 
    <a href="https://github.com/HaticevanD" target="_blank">GitHub</a>
  </li>

  <li>Kutluhan Gül — 
    <a href="https://www.linkedin.com/in/kutluhangil/" target="_blank">LinkedIn</a> | 
    <a href="https://github.com/kutluhangil" target="_blank">GitHub</a>
  </li>

  <li>Nur Seda Ağgünlü — 
    <a href="https://www.linkedin.com/in/nur-seda-aggunlu/" target="_blank">LinkedIn</a> | 
    <a href="https://github.com/nursedaaggunlu" target="_blank">GitHub</a>
  </li>

  <li>Gülnihan Yazıcı — 
    <a href="https://www.linkedin.com/in/gulnihan-yazici/" target="_blank">LinkedIn</a> | 
    <a href="https://github.com/gnihanyazici" target="_blank">GitHub</a>
  </li>
</ul>

<img src="docs/media/divider.svg" width="100%" alt="">

## Development

```sh
npm install
cp .env.template .env
npm run dev      # http://localhost:5174
npm run build
```

<div align="center">
<br>
<a href="https://github.com/kutluhangil"><img src="docs/media/signature.svg" width="100%" alt="Team project, contribution by kutluhangil"></a>
<sub>Fork of <a href="https://github.com/Egemen-Yilmaz/MoneyGuard">Egemen-Yilmaz/MoneyGuard</a> · a GoIT Full Stack team project.</sub>
</div>
