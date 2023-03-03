 Git help
 https://stackoverflow.com/questions/git remote -v32238616/git-push-fatal-origin-does-not-appear-to-be-a-git-repository-fatal-could-n
 
 - Curso de javascrit - Aprendizados

 - Comandos uteis
    document.body.style: acessa propriedades da página, sendo possivel alterar alguns atributos (ex: document.body.style.background = 'black').
    document.querySelector('nome do item'): acessa as propriedades do elemento pelo seu nome (ex: document.querySelector('img.lnXdpd').style.visibility = 'hidden',
                                                                                            document.querySelector('span#title.style-scope.ytd-rich-shelf-renderer').innerText = 'novo texto'))

Site para consulta de métodos internos de strings: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/String
No site acima, ainda é possível encontrar diversas outras informações sobre javascript.

Sintaxe das "fstrings" no javascript: `texto ${variavel} texto`

Requisições utilizando o fetch
Fetch retorna uma promisse, por isso é necessário utilizar funções de uma maneira assincrona, ou ainda utilizar em conjunto com o "then", que só realiza a tarefa após receber uma resposta
   fetch("https://api.giphy.com/v1/gifs/search?api_key=HiFBHYHHnndMDNkSzXRHvtaQAy4O7KRR&q=one+piece&limit=20&rating=g&lang=en")
            .then((response) => {
                return response.json();
            })
            .then((json) => {
                let data = json.data;

                // Criando uma tag <img> dinamicamente atraves do javascript
                data.forEach(image => {
                    let url = image.images.original.url;
                    let img = document.createElement("img");
                    img.src = url;
                    document.body.appendChild(img);
                });
            });

Além de window.alert, temos outras opções:
window.confirm('texto'): mostra uma mensagem com opções de confirmar ou cancelar
window.prompt('texto'): mostra uma mensagem com um input

Conversoes:

Number(n): converte para número
Number.parseInt(): converte para inteiro
parseFloat(): converte para float
String(n): converte para string
n.toString(): converte para string

