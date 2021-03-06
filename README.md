![](http://f.cl.ly/items/2i3X1i3I2s3i2q2r3u1A/github_image.png)

> Escrever códigos é o que fazemos todos os dias. Porém muitos desses códigos não vão passar apenas por uma única pessoa, mas sim por muitas. Por isso criamos esse guia, para que você possa manter um padrão de convenções e boas práticas para que seu código seja o mais declarativo possível e que ele possa ter um brilho natural.

[Veja o guia completo aqui](http://www.pedronauck.com/frontend-styleguide)

## Faça seu Fork!

Um padrão é algo determinado por uma ou por algumas pessoas. Não existe o melhor ou o pior padrão, existe aquele que você mais se adequar. Definitivamente, o intuito desse guia não é dizer qual é o melhor padrão a seguir. Por isso, caso você não se interesse por este guia de estilo, você pode fazer um fork e criar o seu próprio guia de estilo do jeito que melhor lhe conver.

**Vamos as instruções:**

1 - Primeiramente faça um fork deste projeto.  
2 - Instale as dependências dele com o NPM.

``` bash
# estou assumindo que você já tem o nodejs instalado
$ npm install
```

3 - Precisamos instalar também a gem do [Compass](http://compass-style.org/) que fará o build do nosso css.

```bash
$ sudo gem intall compass
```

4 - Estamos usando o [Assemble.io](http://www.assemble.io), um gerador de sites estáticos para rodar a aplicação. O Assemble usa na sua essência o GruntJS para funcionar, por isso alguns comandos são necessários para você montar seu guia de estilo.

| comando      |      descrição      |
|--------------|-------------|
| grunt server | task que levanta um server na porta :9000 com livereload e watch para você setar e criar seu ambiente de desenvolvimento |
| grunt build  | task para gera os arquivos para build |
| grunt deploy | task para deploy do projeto via `grunt-ftp-deploy` |

**OBS:** As configurações para deploy estão definidas dentro do arquivo `_deploy-config.yml`, altere este arquivo para fazer o deploy da sua aplicação. Para você poder fazer um deploy corretamente via ftp, você precisa criar um arquivo `.ftppass` na raíz do seu projeto com seus dados de username/password. [Veja aqui](https://github.com/zonak/grunt-ftp-deploy#authentication-parameters) como fazer.

5 - Após rodar estes comandos espero que tudo tenha dado certo

## Estrutura do projeto

```
src/
├── assets/
│   ├── fonts/
│   ├── images/
│   ├── javascripts/
│   ├── stylesheets/
├── includes/
│   ├── css/
│   ├── html/
│   ├── js/
├── layouts/
├── pages/
├── partials/
```

- `includes/`: Dentro deste diretório se encontra os arquivos de exemplo de código referente à cada sessão.
- `_config.yml`: Arquivo contendo as metadatas do projetos, como diretório que será feito o build e outras configs.
- `_deploy-config.yml`: Configurações default para as definições da task `ftp-deploy`.
- `config.rb`: Configurações de build do Compass.

## Licença

[MIT License](http://opensource.org/licenses/MIT). Copyright 2014, @pedronauck.

## Agradecimentos

Este guia foi feito com base no [Code Guide do @mdo](https://github.com/mdo/code-guide) para o que se refere à HTML e CSS, juntamente com conceitos do [AirBNB Javascript Style Guide](https://github.com/airbnb/javascript) para as convenções de Javascript.
