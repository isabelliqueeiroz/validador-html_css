**Manual didático** sobre como usar o **validador do W3C (https://validator.w3.org/nu/)**. 

---

# 📘 Manual de Utilização do Validador W3C

## 1. O que é o Validador W3C?
- O **W3C Validator** é uma ferramenta gratuita que verifica se o seu código HTML e CSS está escrito corretamente.
- Ele aponta **erros** (problemas que quebram as regras da linguagem) e **avisos** (boas práticas que podem melhorar seu código).
- Usar o validador ajuda a criar páginas **mais acessíveis, compatíveis e profissionais**.

---

## 2. Como acessar
1. Abra o navegador e vá para: [https://validator.w3.org/nu/](https://validator.w3.org/nu/).
2. Você verá três opções para validar:
   - **By URI**: validar um site já publicado (colocando o link).
   - **By File Upload**: enviar um arquivo HTML do seu computador.
   - **By Direct Input**: colar o código diretamente na caixa de texto.

---

## 3. Passo a passo para validar um arquivo
### Método mais usado em sala de aula: **Upload de arquivo**
1. Clique em **"File Upload"**.
2. Selecione seu arquivo `.html`.
3. Clique em **"Check"**.
4. Aguarde alguns segundos: o validador mostrará os resultados.

---

## 4. Entendendo os resultados
- **Erros (Errors)**: precisam ser corrigidos, pois quebram as regras do HTML.
  - Exemplo: *“O elemento `<a>` com atributo `href` não deve aparecer como descendente do elemento `<button>`”*.
- **Avisos (Warnings)**: não impedem a página de funcionar, mas indicam melhorias.
  - Exemplo: *“A imagem não possui atributo `alt`”*.

---

## 5. Como corrigir os erros
- Leia a mensagem do validador: ela indica **linha e coluna** do problema.
- Vá até o seu código e ajuste.
- Exemplos:
  - **Erro:** `<button><a href="#receitas">...</a></button>`  
    **Correção:** usar apenas `<a>` ou apenas `<button>`.
  - **Erro:** `<img src="foto.jpg">` sem `alt`.  
    **Correção:** `<img src="foto.jpg" alt="Descrição da foto">`.

---

## 6. Boas práticas para usar o validador
- Valide sempre que terminar uma parte do projeto.
- Corrija **primeiro os erros**, depois analise os avisos.
- Use os avisos como oportunidade de aprender boas práticas.
- Lembre-se: o validador não corrige sozinho, ele apenas mostra o que precisa ser ajustado.

---

## 7. Exercício para os alunos
1. Criem um arquivo `index.html` simples com título, parágrafo e imagem.
2. Validem no W3C.
3. Corrijam os erros e avisos até que o validador mostre **“Document checking completed. No errors or warnings to show.”**
4. Compare o código antes e depois da correção.

---

👉 Esse manual pode ser usado como guia em sala de aula. Ele mostra não só como usar a ferramenta, mas também **por que ela é importante** para escrever HTML e CSS de forma correta.

Aqui está um **exemplo de código com erros** para os alunos praticarem no validador do W3C. 
Eles vão validar, observar os erros e depois corrigir.

---

## 🔴 Código com erros (para validar)
```html
<!DOCTYPE html>
<html>
<head>
    <title>Minha Página</title>
</head>
<body>
    <h1>Bem-vindo à minha página</h1>

    <p>Este é um parágrafo sem fechar a tag

    <img src="foto.jpg">

    <button>
        <a href="#receitas"><img src="icone.png"></a>
    </button>

    <ul>
        <li>Item 1
        <li>Item 2
        <li>Item 3
    </ul>
</body>
</html>
```

---

## ⚠️ O que o validador vai apontar
1. **Parágrafo não fechado**: `<p>` aberto mas sem `</p>`.
2. **Imagem sem atributo `alt`**: `<img src="foto.jpg">` e `<img src="icone.png">`.
3. **Uso incorreto de `<a>` dentro de `<button>`**.
4. **Itens da lista sem fechamento de `<li>`**.

---

## ✅ Código corrigido
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Minha Página</title>
</head>
<body>
    <h1>Bem-vindo à minha página</h1>

    <p>Este é um parágrafo corretamente fechado.</p>

    <img src="foto.jpg" alt="Foto ilustrativa">

    <a href="#receitas">
        <img src="icone.png" alt="Ícone de receitas">
    </a>

    <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
    </ul>
</body>
</html>
```

---

## 🎯 Atividade para os alunos
1. Copiem o **código com erros** em um arquivo `exemplo.html`.
2. Validem no [W3C Validator](https://validator.w3.org/nu/).
3. Anotem os erros que aparecerem.
4. Corrijam o código até que o validador não mostre mais erros.
5. Compare com o **código corrigido** para entender as diferenças.

---

Agora um **exemplo de CSS com erros** para os alunos validarem e corrigirem. 

---

# 🔴 Código com erros de CSS (para validar)
```css
body {
    background-color: #fff
    font-family: Arial, sans-serif;
    color: #333
}

h1 {
    font-size: 32px;
    text-align center;
    color: blue;
}

p {
    font-size: 16px
    margin: 10px
    padding: 5px;
    color: red;
}
```

---

## ⚠️ O que o validador vai apontar
1. **Falta de ponto e vírgula (`;`)** em várias propriedades:
   - `background-color: #fff`
   - `color: #333`
   - `font-size: 16px`
   - `margin: 10px`
2. **Erro de sintaxe**: `text-align center;` → falta o `:` depois de `text-align`.
3. **Boas práticas**: sempre fechar corretamente cada declaração com `;`.

---

# ✅ Código corrigido
```css
body {
    background-color: #fff;
    font-family: Arial, sans-serif;
    color: #333;
}

h1 {
    font-size: 32px;
    text-align: center;
    color: blue;
}

p {
    font-size: 16px;
    margin: 10px;
    padding: 5px;
    color: red;
}
```

---

## 🎯 Atividade para os alunos
1. Copiem o **CSS com erros** em um arquivo `style.css`.
2. Validem no W3C CSS Validator [(jigsaw.w3.org)](https://jigsaw.w3.org/css-validator/validator).
3. Observem os erros e avisos que aparecem.
4. Corrijam o código até que o validador não mostre mais erros.
5. Compare com o **código corrigido** para entender as diferenças.

---

👉 Dessa forma, seus alunos vão aprender que o validador não serve apenas para HTML, mas também para CSS, e que ele é uma ferramenta essencial para escrever código limpo e correto.  

Quer que eu prepare um **mini-projeto completo (HTML + CSS com erros)** para eles validarem de uma vez só?