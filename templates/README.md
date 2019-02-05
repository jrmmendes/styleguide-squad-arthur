
# Nome do Projeto
Breve descrição sobre o objetivo do projeto e detalhes da implementação.

## Primeiros passos
Siga estes passos caso queira ter uma cópia do projeto configurada e executando no seu host local para propósitos de desenvolvimento e testes. Veja a seção `Realizando Deploy` para entender como fazer a instalação em um ambiente de produção.

### Prerequisitos
## Ubuntu e derivados
Você precisará ter instalado os seguintes softwares:
- Python 3
- Pip
- Virtualenv
- Pip
- Pipenv

Que podem ser instalados pelo seguinte comando:

```
sudo apt install python python3 python-pip virtualenv && sudo pip install pipenv 
```
## Windows

### Instalação em ambiente de desenvolvimento
Após clonar e acessar a pasta raiz do repositório, crie o ambiente virtual usando o pipenv:

```
pipenv --python 3
```

Após isso, instale as dependências necessárias:

```
pipenv install
```

Para ativar o ambiente virtual, basta fazê-lo também pelo pipenv com o comando `pipenv shell`. Se tudo tiver sido configurado com sucesso, basta aplicar as migrações com 

```
python manage.py migrate
``` 
exportar as seguintes variáveis de ambiente:
- `DJANGO_SECRET_KEY`, que deve receber como valor uma [chave secreta](https://www.miniwebtool.com/django-secret-key-generator/) para o Django;
- `EMAIL_HOST_ACCOUNT`, que deve receber como valor uma conta de email para ser utilizada no [templated_email](https://djangopackages.org/packages/p/django-templated-email/);
- `EMAIL_HOST_PASSWORD`, que deve receber como valor a senha da conta de email.

e iniciar o servidor de desenvolvimento com 

```
python manage.py runserver
``` 


## Realizando Deploy
### Heroku
Para realizar deploy na Heroku, basta criar um novo app, configurar as mesmas variáveis de ambiente na aba `settings`, colocando também a variável `DJANGO_SETTINGS_MODULE` com valor `projeto.settings.production` e associar a este repositório na aba de `deploy`.

## Ferramentas de Build
* [Pipenv](https://github.com/pypa/pipenv) - Python Development Workflow for Humans
* [Django](https://www.djangoproject.com/) - The Web framework for perfectionists with deadlines
* [Heroku](https://www.heroku.com) - Cloud Application Platform

## Autores
* **Júnior Mendes** - *Criação do modelo de README* - [jrmmendes](https://github.com/jrmmendes)
* **Laís Ponciano** - *Mockup*

Made with `markdown` and love by CITi
