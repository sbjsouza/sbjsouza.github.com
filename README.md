# **AiBoxLab Website**

### **Por onde começar?**
1. Clone o projeto em sua pasta
2. Abra o Terminal e navegue até a pasta do projeto

### **Ajustando as dependências**
1. utilize o **NVM** para usar a versão *5.x* do **Node**
2. Certifique-se de possuir **Ruby** instalado. Instale se necessário.
3. O tema exige um pacote adicional, o **Jekyll**. Digite o comando abaixo para instalar:
```CURL 
    gem install -n /usr/local/bin jekyll
```

### **Executando**
1. Digite o seguinte comando no **Terminal**:
```CURL
    grunt serve
```
2. Acesse o servidor local. Digite no navegador:
```CURL
    http://127.0.0.1:4000
```

### **Entendendo a página de eventos**

> Esta página possui o objetivo de entregar um resumo para participação e divulgação de eventos promovidos pelo AiBoxLab.

> **Alterações:** durante o desenvolvimento, algumas alterações precisaram ser realizadas no arquivo **doctype-head.html** para inserir dependências necessárias, como fontes e estilos externos. Também foram alterados os arquivos **footer.html** e o **_config.yml** para automação do ano atual do copyright do site.

##### 1. Estrutura 

A página de eventos é dividida em 2 arquivos. O primeiro, **events.html**, é responsável por toda a renderização e localização dos elementos na página. O segundo, **events.css**, é encarregado de atribuir os estilos de cada elemento e classe no primeiro documento.

##### 2. Alterando o conteúdo

Para alterar o conteúdo, será necessário alterar o arquivo **events.html**. Nas primeiras linhas, poderá ser visto o **permaLink**, que redireciona o usuário para o link que consta na mesma linha. Para mudar, será necessário renomear o arquivo atual para o nome desejado, ex: **events.html** --> **pos_graduacao.html** e alterar o permaLink como o exemplo a seguir:

```html
    ---
    layout: default
    permalink: "/events" 
    ---

    alterado para

    ---
    layout: default
    permalink: "/pos_graduacao" 
    ---
```

Para alterar as imagens, basta adicioná-las à pasta **/img** e substituir o nome no local indicado do arquivo **events.html**. O local indicado está demarcado por comentários. 

```html
    <!-- Substitua a foto aqui -->
```

Substitua duas versões de imagem, uma para Web e a segunda para mobile, sem ondas. Dependendo da proporção da imagem, pequenas alterações de distância poderão ser necessárias no arquivo **events.css**.

Assim como as imagens, os outros conteúdos textuais e de imagem estão indicados por comentários, bastando apenas alterar seu conteúdo e redimensionar as distâncias caso necessário.

```html
    <!-- Substitua "nome do conteúdo" aqui -->
```
Ao substituir o botão de **inscrição**, será necessário apenas alterar o link do seu formulário na função 'action(  )', no final do arquivo.

```JavaScript
    function action(){
        window.location.href = 'seu link aqui';
    }
```

> <u>**nota:**</u> caso alguma alteração seja realizada nos estilos, será necessário observar as **media query's**, ao todo são 2 disponíveis (959px e 760px), para adaptar a página a diferentes tamanhos de tela. Portanto, ao alterar o estilo fora das query's, poderá ser necessário a alteração em cada uma delas.

Caso necessite alterar o tempo das animações de surgimento de scroll, basta substituir o tempo de todas as classes.

```JavaScript
    ScrollReveal().reveal('.classe', {duration: tempo em milissegundo});
```



Documentação do tema do site: [Aqui](http://obaez.com/dentistsmile-docs/)