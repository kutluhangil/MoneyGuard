<div align="center">

<img src="docs/media/hero.svg" alt="Money Guard — the add-transaction modal records an expense, the row joins the table and the balance drops" width="100%">

<p>
  <a href="https://money-guard-app-eight.vercel.app"><img alt="Live" src="https://img.shields.io/badge/live-open%20Money%20Guard-8b5cf6?style=for-the-badge&labelColor=2d2556"></a>
  <img alt="Redux Toolkit" src="https://img.shields.io/badge/Redux%20Toolkit-persist-ffb627?style=for-the-badge&labelColor=2d2556">
  <img alt="Chart.js" src="https://img.shields.io/badge/Chart.js-statistics-24cca7?style=for-the-badge&labelColor=2d2556">
  <img alt="Team" src="https://img.shields.io/badge/GoIT-team%20project-8b5cf6?style=for-the-badge&labelColor=2d2556">
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

## The idea

Money Guard is a wallet in the browser: sign up, add every income and expense with a category, a date and a comment, and the app keeps the balance, a monthly breakdown and the day's exchange rates in front of you. It was built by a six-person team in the GoIT programme against the course's wallet API, with each member owning a slice of the app.

> **One source of truth for money.** Every transaction goes through an async thunk to the wallet API; the balance is read back from the server instead of being added up in the browser, so a refresh or a second device always shows the same number.

<img src="docs/media/divider.svg" width="100%" alt="">

## Features

| | |
|---|---|
| **Authentication** | Register, log in and log out; the JWT is persisted with redux-persist and private / public routes guard the pages. |
| **Transactions** | Create, read, update and delete income and expenses, in a table on desktop and cards on mobile. |
| **Quick add** | A floating "+" button and modal add / edit forms with react-hook-form, Yup and a date picker. |
| **Balance** | The total balance stays in sync with the server. |
| **Statistics** | A Chart.js doughnut and a category table for any month and year. |
| **Currency** | USD and EUR buy and sell rates from the Monobank API, cached in localStorage to stay inside its rate limit. |
| **Feedback** | A global loader, toast-based error handling and a password-strength indicator on sign-up. |

<img src="docs/media/divider.svg" width="100%" alt="">

## How it fits together

```mermaid
flowchart LR
  UI[React · mobile first<br/>Home · Statistics · Currency] --> ST[(Redux Toolkit<br/>auth persisted)]
  ST --> TH[Async thunks · Axios] --> API[wallet.b.goit.study/api]
  ST --> CH[Statistics · Chart.js]
  MB[Monobank API] --> CACHE[localStorage cache] --> CUR[Currency table]
```

<img src="docs/media/divider.svg" width="100%" alt="">

## My part

I built the transaction flow: the add and edit modals with their forms and validation, and the create, update and delete actions wired to the wallet API.

<img src="docs/media/divider.svg" width="100%" alt="">

## Türkçe özet

**Money Guard**, React ve Redux ile ekip olarak geliştirdiğimiz, tamamen duyarlı bir kişisel finans uygulaması. Kullanıcılar kayıt olup gelir ve gider işlemleri ekleyebiliyor, düzenleyip silebiliyor; bakiye sunucudan anlık güncelleniyor, aylık istatistikler grafikle gösteriliyor ve Monobank döviz kurları önbellekle takip ediliyor. Bu projede işlem ekleme/düzenleme akışından ve modallardan sorumluydum.

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

```
src/pages/        Home, Statistics, Currency tabs · Login · Register · Dashboard
src/components/   Balance, Chart, Header, Navigation, ModalLayout, StatisticsDashboard, StatisticsTable, transactions
src/features/     auth, global (loader), statistics
src/redux/        store and transactions
src/api/          the Axios instance for the wallet API
```

<div align="center">
<br>
<a href="https://github.com/kutluhangil"><img src="docs/media/signature.svg" width="100%" alt="Team project, contribution by kutluhangil"></a>
<sub>Fork of <a href="https://github.com/Egemen-Yilmaz/money-guard-app">Egemen-Yilmaz/money-guard-app</a> · a GoIT Full Stack team project · amounts in the banner are invented.</sub>
</div>
