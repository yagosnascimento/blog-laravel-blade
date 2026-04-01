## 1. O que é o PHP e como ele funciona?

Diferente do JavaScript que roda no navegador do seu cliente, o PHP roda no **servidor**. Ele processa as informações e entrega apenas o HTML pronto para o navegador.



### Preparando o terreno
Para começar, você precisa de três coisas no seu PC:
1.  **PHP:** O interpretador da linguagem.
2.  **Composer:** O gerenciador de pacotes (como o NuGet do C# ou o pip do Python).
3.  **VS Code:** (Ou qualquer editor que você curta).

> **Dica:** Se não quiser configurar um por um agora, você pode baixar o **XAMPP** ou o **Laragon**, que já instalam tudo (PHP, Servidor, Banco de Dados) de uma vez.

---

## 2. Sintaxe Básica (Onde tudo começa)

Todo arquivo PHP precisa começar com a tag `<?php`. Você não precisa fechar essa tag se o arquivo só contiver código PHP.

### Variáveis e Tipos
No PHP, toda variável começa com um cifrão `$`. O PHP é fracamente tipado (embora esteja ficando cada vez mais rigoroso).

```php
<?php

$titulo = "Meu Primeiro Blog"; // String
$postagens = 10;               // Integer
$estaAtivo = true;             // Boolean

// Para exibir algo na tela, usamos o 'echo'
echo "Bem-vindo ao " . $titulo; 
```
*Note que usamos o **ponto (.)** para concatenar strings, e não o sinal de mais (+).*

---

## 3. Arrays (A alma do PHP)

No PHP, os arrays são extremamente poderosos. Eles podem ser listas simples ou "mapas" (chave => valor), que chamamos de Arrays Associativos.

```php
<?php

// Array simples
$categorias = ["Tecnologia", "Games", "3D Printing"];

// Array associativo (muito comum para dados de banco)
$post = [
    "titulo" => "Aprendendo PHP em 2026",
    "descricao" => "Um guia para iniciantes",
    "imagem" => "banner.jpg"
];

echo $post["titulo"]; // Saída: Aprendendo PHP em 2026
```

---

## 4. Estruturas de Controle

Como você já tem noção de lógica, aqui é bem parecido com o que você já conhece:

### Condicionais
```php
if ($postagens > 0) {
    echo "Temos conteúdo!";
} else {
    echo "Blog vazio.";
}
```

### Loops (Essencial para o Blog)
O `foreach` é o seu melhor amigo para listar as postagens na tela.

```php
$posts = ["Post 1", "Post 2", "Post 3"];

foreach ($posts as $item) {
    echo "<li>" . $item . "</li>";
}
```

---

## 5. O Próximo Passo: Funções

Para o seu projeto de blog, você vai precisar organizar o código em funções. Uma função simples em PHP:

```php
function formatarData($data) {
    return date('d/m/Y', strtotime($data));
}
```

---
