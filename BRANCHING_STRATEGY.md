# Branching Strategy for Gruppe 14

## Branches

### main
- Brukes kun for å publisere fullførte sprints
- All kode i main skal være testet og klar for produksjon
- Beskyttet mot direkte pushes

### develop
- Integreringsbranch for ferdigutviklede features
- Merges inn i main når en sprint skal publiseres
- Koden skal alltid være stabil

### feature/*
- Opprettes fra develop for hver nye feature
- Navngis etter backlog-item (f.eks. feature/user-authentication)
- Hver utvikler jobber på sin egen feature-branch
- Merges tilbake til develop når featuren er ferdig

## Arbeidsflyt

1. Opprett feature-branch fra develop: `git checkout -b feature/navn develop`
2. Utvikle og commite endringer på feature-branchen
3. Push til remote: `git push -u origin feature/navn`
4. Når feature er klar: opprett pull request fra feature/* til develop
5. Etter code review: merge til develop
6. Når sprint er klar: opprett pull request fra develop til main
7. Etter godkjenning: merge til main og tag release

