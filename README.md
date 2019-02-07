# Styleguide
<p align="left">
  <a href="https://github.com/jrmmendes/styleguide-squad-arthur/issues">
    <img src="https://img.shields.io/github/issues/jrmmendes/styleguide-squad-arthur.svg?&colorB=D35F5F&style=flat-square" alt="Open Issues">
  </a>
  <a href="https://github.com/jrmmendes/styleguide-squad-arthur/pulls">
    <img src="https://img.shields.io/github/issues-pr/jrmmendes/styleguide-squad-arthur.svg?style=flat-square" alt="Open Pull Requests">
  </a>
  <a href="https://github.com/jrmmendes/styleguide-squad-arthur/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/jrmmendes/styleguide-squad-arthur.svg?style=flat-square" alt="Contributors">
  </a>
</p>

Todo projeto open source, por sua dimensão, segue um guia de estilos: um conjunto de conveções sobre como escrever código. Isso permite que, a longo prazo, seja possível manter a consistência e a qualidade do que é feito.

Esse repositório contem diversos insights pra que nossos projetos possam usufruir dessas característica, em se tornarem mais consistentes :)

# Branchs
Seguimos os Gitflow, então existem os seguintes tipos de branchs:
- `master`: branch com a versão de estável mais atual do sistema (não commitar diretamente);
- `develop`: branch para desenvolvimento do projeto, contendo a última versão instável
- `feature/new-feature`: branch para desenvolvimento de uma funcionalidade específica
- `hotfix/catch-the-bug`: branch para resolução de erros encontrados na master

O seguinte workflow deve existir:

1 - Crie a branch da sua feature a partir da branch `develop`

2 - Ao terminar a funcionalidade, crie um pull request para a branch `develop` e marque um ou mais revisores (e se alguem te marcar, revise o quanto antes o PR pra não prender o projeto)

Quando um conjunto de funcionalidades razoável tiver sido desenvolvido, um dos membros do squad abre um PR da `develop` para a `master`. Caso um bug seja encontrado após o merge, crie uma branch `hotfix` e solucione-o, abrindo depois um PR para a branch `master` e outro para a branch `develop`.

# Deploy
O código da branch `develop` será usado para o deploy em `staging`. Já o da branch `master` será usado para o deploy que será apresentado ao cliente.
