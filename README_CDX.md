# Guia das alterações CDX

Todas as partes acrescentadas ao código principal estão identificadas por comentários contendo `CDX`.

## Links do Mercado Livre

- O campo `link_mercado_livre` foi acrescentado aos produtos correspondentes dentro de `produtos.json`.
- JSON não permite comentários. A explicação desse campo está marcada com `CDX` na função `renderizarProdutos` do arquivo `index.html`.
- O botão **Ver no Mercado Livre** é criado somente quando o endereço pertence ao domínio oficial `mercadolivre.com.br`.
- O atributo `target="_blank"` abre o anúncio em outra aba.
- O atributo `rel="noopener noreferrer"` protege a página original ao abrir o endereço externo.

## Sumário por marca e modelo

- O bloco visual do sumário está no início da seção de catálogo.
- O objeto `catalogoVeiculos` reúne as marcas, os modelos e as variações de escrita encontradas nas descrições.
- A função `normalizarVeiculo` remove diferenças de acentuação, pontuação e letras maiúsculas/minúsculas.
- A função `obterAplicacoes` identifica os veículos citados em cada descrição.
- A função `renderizarSumario` mostra apenas marcas e modelos que realmente possuem produtos.
- A função `aplicarFiltros` combina o filtro de marca/modelo com o campo de pesquisa.
- Os números exibidos ao lado dos modelos representam a quantidade de produtos encontrados.
- O sumário começa fechado por meio do atributo `hidden`; o botão `toggle-sumario` abre e fecha o conteúdo e atualiza `aria-expanded`.

## Como encontrar as alterações

Pesquise por `CDX` dentro de `index.html`. Os comentários indicam o início, o fim e a finalidade de cada trecho acrescentado.

