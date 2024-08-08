
## Teleoperator [Contribution](http://contribution.teleoperator.app) [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/MENU.md)



## Rozwiązanie [teleoperator.app](http://www.teleoperator.app)

+ [cameramonit.com](http://www.cameramonit.com)
+ [dokumentacja](http://docs.cameramonit.com)
+ [logo](http://logo.cameramonit.com)
+ [roadmap](http://roadmap.cameramonit.com)
+ [identyfikator](http://identity.cameramonit.com)
+ [współpraca](http://współpraca.softreck.dev)


## [WSPÓŁPRACA](http://contribution.teleoperator.app) zawsze jest mile widziana:

+ Znalazłeś [problem lub błąd](https://github.com/cameramonit/docs/issues/new)?
+ Czy chcesz [poprawić artykuł](https://github.com/cameramonit/docs/edit/main/README.md)?
+ Czy interesuje Cię współpraca przy innych [projektach git](https://github.com/cameramonit/)?
+ Czy masz co dołożyć lub rozmawiać? [Otwórz pull request](https://github.com/cameramonit/docs/pulls) lub [opisz problem](https://github.com/cameramonit/docs/issues).

 [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/STRUCTURE.md)

### Inicjalizacja projektu React.js

1. **Zainstaluj Node.js i npm**: Najpierw upewnij się, że masz zainstalowany Node.js i npm.
2. **Utworzenie nowego projektu React**:
   ```sh
   git clone 
   cd www
   npx create-react-app .   
   npm start
   ```


### Struktura Folderów

Upewnij się, że Twoje katalogi mają poniższą strukturę:

```
teleoperator-app/
├── backend/
│   ├── Dockerfile
│   ├── package.json
│   ├── package-lock.json
│   ├── server.js
│   └── ...inne_pliki_backendu...
├── src/
│   ├── components/
│   │   ├── Header.js
│   │   ├── Footer.js
│   │   ├── InstallerList.js
│   │   ├── Marketplace.js
│   │   ├── Dashboard.js
│   │   └── ...
│   ├── App.js
│   ├── App.css
│   └── index.js
├── Dockerfile
├── docker-compose.yml
├── package.json
├── package-lock.json
├── public/
└── ...inne_pliki_frontendu...
```

## Node Install [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/NODE.md)



Po zapisaniu pliku `package.json`, uruchom następującą komendę w terminalu, aby zainstalować wszystkie zależności:

```sh
cd src
```

```sh
npm install
```

To upgrade all the dependencies in your `package.json` to their latest versions, you can follow these steps:

### Using npm (version 5.2 or higher)

1. **Install `npm-check-updates`:**
   First, you need to install the `npm-check-updates` tool globally. This tool helps you to easily upgrade the dependencies in your `package.json` to the latest versions.

   ```sh
   sudo npm install -g npm-check-updates
   ```

   ```sh
   sudo npm install -g npm@10.8.1
   ```
2. **Update `package.json` Dependencies:**
   Once `npm-check-updates` is installed, run the following command to upgrade your `package.json` dependencies:

   ```sh
   ncu -u
   ```

   The `ncu -u` command checks your `package.json` file for any outdated dependencies and updates them to the latest versions.

3. **Install Updated Dependencies:**
   After updating the `package.json` file, install the updated packages using:

   ```sh
   npm install
   ```

### Using yarn

If you prefer to use `yarn`, you can update all dependencies to their latest versions as follows:

1. **Upgrade Dependencies:**
   Run the following command to upgrade all the dependencies listed in your `package.json` file:

   ```sh
   yarn upgrade --latest
   ```

### Manual Method

Alternatively, you could manually update the `package.json` file and then install the dependencies:

1. **Update Versions in `package.json`:**
   Manually change the version numbers of the dependencies in your `package.json` file to the latest versions. You can look up the latest versions on npm's website or by running:

   ```sh
   npm show <package-nameversion
   ```

2. **Install Dependencies:**
   After updating the `package.json` file, run the following command to install the updated packages:

   ```sh
   npm install
   ```

### After Upgrading

After upgrading your dependencies, it's a good practice to:

1. **Check for breaking changes:**
   Review the changelogs of the dependencies to be aware of any breaking changes that might require code modifications.

2. **Test your application:**
   Thoroughly test your application to ensure everything works correctly with the updated dependencies.

3. **Lockfile Update:**
   If you use a lockfile (`package-lock.json` or `yarn.lock`), make sure it is updated by the package manager.

Following these steps should help you successfully upgrade all the packages in your `package.json` to their newest versions.



[Deployment | Create React App](https://create-react-app.dev/docs/deployment/)

Static Server

For environments using [Node](https://nodejs.org/), the easiest way to handle this would be to install [serve](https://github.com/vercel/serve) and let it handle the rest:
```bash
npm install -g serveserve -s build
```

The last command shown above will serve your static site on the port **3000**. Like many of [serve](https://github.com/vercel/serve)’s internal settings, the port can be adjusted using the `-l` or `--listen` flags:
```bash
serve -s build -l 4000
```

Run this command to get a full list of the options available:
```bash
serve -h
```

## Python Install [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/PYTHON.md)

Zainstaluj biblioteki Pythona, jeśli jeszcze tego nie zrobiłeś. Możesz to zrobić używając `pip`:

```bash
py -m pip install --upgrade pip
py -m pip install --upgrade setuptools
py -m pip install --upgrade wheel
py -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

```bash
py -m pip install -r requirements.txt
```

## Uruchamianie kontenerów [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/DOCKER.md)

Pliki `Dockerfile` i `docker-compose.yml` umożliwiaj konteneryzację aplikacji React.js (src) i backendu Express, co sprawia, że aplikacja staje się bardziej przenośna i łatwa do wdrożenia. 
Dzięki Docker i Docker Compose możesz uruchomić złożone środowiska wielokontenerowe jedną komendą, co znacznie upraszcza zarządzanie i skalowanie aplikacji.



```sh
cd backend
docker build -t .
```


```sh
cd ..
```

```sh
cd src
docker build .
```

### Zbuduj i uruchom kontenery za pomocą Docker Compose:

```sh
docker compose up --build
```

### Debugowanie
Jeśli wystąpią problemy, sprawdź logi za pomocą:

```sh
docker compose logs
```

### Zatrzymywanie kontenerów

```sh
docker compose down
```


If you need your build to connect to services running on the host, you can use the special host-gateway value for --add-host. In the following example, build containers resolve host.docker.internal to the host's gateway IP.
```sh
docker build --add-host host.docker.internal=host-gateway .
```

## TODO [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/TODO.md)

Na tym etapie stworzyliśmy podstawową makietę aplikacji webowej z wykorzystaniem technologii React.js, która jest łatwa do modyfikacji.
Od inicjalizacji projektu, przez utworzenie podstawowej struktury komponentów, aż po integrację z symulowanym API (MSW).



### Podsumowanie i Następne Kroki

[ ] **Skalowanie**: W miarę potrzeb dodawaj więcej komponentów, takich jak formularze rejestracyjne, kalendarze dostępności, panele administracyjne itd.
[ ] **Backend**: Rozważ implementację rzeczywistego backendu z REST API lub GraphQL.
[ ] **Autoryzacja**: Zaimplementuj system autoryzacji, np. OAuth2.
[ ] **Testowanie**: Dodaj testy jednostkowe i integracyjne, korzystając np. z Jest i React Testing Library.
[ ] **Responsywność**: Dopracuj stylizację, aby aplikacja działała dobrze na różnych urządzeniach.



Poniżej przedstawiam plan rozwoju projektu.

### 1. Skalowanie i Nowe Funkcjonalności

Dodanie bardziej kompleksowych komponentów takich jak:
- **Formularze Rejestracyjne**: Komponenty z walidacją np. z wykorzystaniem `formik` do łatwego zarządzania formularzami w React.js.
- **Kalendarze Dostępności**: Implementacja bardziej zaawansowanych kalendarzy z możliwością zarządzania wolnym czasem instalatorów, np. z użyciem bibliotek takich jak `react-big-calendar`.
- **Panele Administracyjne**: Widoki i funkcje dla administratorów, tj. zarządzanie użytkownikami, zamówieniami i produktami.

### 2. Backend Integration

Ciężar logiki biznesowej i przechowywania danych przenieś na backend:
- **API REST**: Zaimplementuj prawdziwe API, preferencyjnie w Node.js z Express, Django, czy innej technologii, z której korzystasz.
- **GraphQL**: Alternatywnie użyj GraphQL do bardziej elastycznego zarządzania danymi.
- **Serwery**: Hostuj backend na platformach takich jak AWS, Google Cloud, Heroku.

### 3. Uwierzytelnianie i Autoryzacja

Zaimplementuj bezpieczne logowanie i autoryzowanie użytkowników:
- **OAuth2**: Integracja z popularnymi providerami tożsamości (Google, Facebook).
- **JWT**: Użyj JSON Web Tokens do bezpiecznego przekazywania informacji o autoryzacji.

### 4. Testowanie i Utrzymanie Jakości

Wprowadź narzędzia do testowania kodu, jego analizy i ciągłej integracji:
- **Jest i React Testing Library**: Testuj komponenty oraz interakcje.
- **ESLint i Prettier**: Zapewniaj spójność kodu i szybkie wyłapywanie błędów.
- **Ciągła Integracja (CI)**: Ustaw np. w GitHub Actions, CircleCI, TravisCI.

### 5. Ulepszanie Stylizacji i Responsywności

Dostosuj aplikację do różnych urządzeń i ulepsz jej wygląd:
- **CSS-in-JS**: Rozważ użycie bibliotek takich jak `styled-components` lub `emotion`.
- **Responsywność**: Zapewnij, aby Twoje komponenty dobrze wyglądały zarówno na urządzeniach mobilnych, jak i desktopowych z pomocą `flexbox`, `grid` oraz media queries.

### 6. Monitorowanie i Optymalizacja

Monitoruj działanie aplikacji i poprawiaj jej wydajność:
- **Google Analytics**: Śledź ruch i zachowania użytkowników.
- **Logi i Monitoring**: Zaimplementuj systemy logowania błędów i monitorowania wydajności (np. Sentry, New Relic).
- **Optymalizacja Wydajności**: Przeprowadź optymalizację komponentów React używając technik takich jak lazy loading, memoization.

### 7. DevOps i Automatyzacja

Automatyzacja procesów wdrożeniowych zapewni częste i pewne wdrożenia:
- **Docker i Kubernetes**: Zautomatyzuj wdrożenia aplikacji przy użyciu konteneryzacji.
- **CI/CD**: Implementacja potoków CI/CD do automatyzacji buildów, testów i wdrożeń.

 [<span style='font-size:20px;'>&#x270D;</span>](git@github.com:teleoperator-app/contribution/edit/main/DOCS/FOOT.md)
---
[info about privacy](../docs/PRIVACY.md)


+ [edit](https://github.com/cameramonit/www/edit/main/README.md)


<script type="module">    
  import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10/dist/mermaid.esm.min.mjs';
  //import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@10.8.0/dist/mermaid.min.js';
  mermaid.initialize({
    startOnReady:true,
    theme: 'forest',
    flowchart:{
            useMaxWidth:false,
            htmlLabels:true
        }
  });
  mermaid.init(undefined, '.language-mermaid');
</script>

---
+ Modular Documentation made possible by the [FlatEdit](http://www.flatedit.com) project.
