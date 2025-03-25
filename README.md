### Rótulo Nutricional 


---

### Estilização do corpo da página
Inicie criando um seletor para o elemento `body`. Defina a propriedade `font-family` para "Open Sans" e adicione um fallback `sans-serif`. O uso de fallback garante que, caso a fonte principal não esteja disponível, uma alternativa similar será utilizada. Importante: fontes com nomes compostos devem ser envolvidas entre aspas no CSS.

---

### Organização e separação do conteúdo
Para facilitar a leitura e organização do rótulo, insira um elemento `<div>` abaixo do título `<h1>` e aplique a classe `divider`. Linhas divisórias ajudam a separar e estruturar informações importantes, especialmente em espaços restritos.

---

### Entendendo Margin e Padding
- **Margin (margem)** Define o espaço externo ao redor do elemento. É a distância entre o elemento e os outros elementos ou a borda da página. Margins nunca afetam o conteúdo ou o tamanho visual do elemento em si, apenas o espaçamento ao seu redor.
 Imagine que o quadro está pendurado na parede. O margin é o espaço vazio entre o quadro e qualquer outro objeto na parede, como outro quadro ou uma janela. Esse espaço é externo ao quadro e não afeta o tamanho ou o conteúdo dentro do quadro.

 
- **Padding (preenchimento)**: Define o espaço interno dentro do elemento. É a distância entre o conteúdo do elemento (como texto ou imagens) e a borda do elemento. Padding aumenta o tamanho visual do elemento, sem mudar o seu conteúdo.
 Agora pense na área dentro do quadro, entre a borda e a pintura em si. O padding é o espaço vazio que mantém a pintura afastada das bordas internas do quadro. Ele afeta apenas o interior do quadro e aumenta o espaço disponível dentro dele sem alterar o espaço externo.

---

### Ajuste fino no texto
Use a propriedade `letter-spacing` para ajustar o espaçamento entre os caracteres, criando uma aparência mais refinada e legível.

---

### Negrito eficiente no rótulo
Se o texto em negrito é usado com frequência em elementos como tabelas nutricionais ou outras partes do layout, faz sentido criar uma classe CSS dedicada para aplicar o estilo em vários elementos. Isso melhora a manutenção, porque, caso o estilo precise ser ajustado no futuro (como mudar a fonte ou o peso do negrito), você só precisa editar a classe, e todas as partes que a utilizam serão atualizadas automaticamente.Você pode aplicar essa classe em qualquer lugar necessário.
ex:
     .bold-label {
       font-weight: bold;
     }

---

### Estilização com `<span>`
O elemento `<span>` é ideal para estilizar partes específicas de um texto inline. Ele permite aplicar cor, peso ou estilo de forma granular, sem alterar a estrutura geral do conteúdo.

---

### Flexbox para alinhamento perfeito
`display: flex`: Transforma o elemento em um contêiner flexível, permitindo que seus filhos (neste caso, os textos dos parágrafos) sejam organizados de forma automática e flexível

 `justify-content: space-between`* `: Distribui os elementos filhos ao longo do eixo principal (horizontal por padrão), com espaços iguais entre eles. Isso cria um layout equilibrado onde os itens ficam distribuídos de ponta a ponta do contêiner.

`align-items: flex-end`: Alinha os itens ao longo do eixo cruzado (vertical por padrão) na parte inferior do contêiner flexível

---

### Unidade rem para escalabilidade
A unidade `rem` é baseada no tamanho da fonte do elemento raiz (`<html>`). Por exemplo, ao definir `font-size: 0.85rem`, a fonte terá 85% do tamanho padrão do `<html>` (geralmente 16px), resultando em aproximadamente 13.6px.

---

### Pseudoseletores inteligentes
Com o pseudo-seletor `:not`, é possível aplicar estilos a elementos enquanto exclui aqueles que atendem a condições específicas. Isso melhora a flexibilidade e personalização do design.

---

### Texto em itálico
Use a tag `<i>` para adicionar ênfase ou estilo especial a partes do texto, como no exemplo "Trans Fat".

---

### Criação de divisores e classes específicas
Divisores ajudam a criar uma hierarquia visual e organização no rótulo. Combine classes como `divider`, `indent` ou `no-divider` para ajustar separações ou recuos. Adicione novas classes para personalizar elementos, como `.note`, para textos adicionais ou observações.
A regra não será aplicada aos parágrafos com essa classe.
ex:
   .daily-value p:not(.no-divider) {
  border-bottom: 1px solid #888989;
}


---

### Espaçamento e alinhamento em rótulos
Utilize uma classe como `.calories-info`, configurando `display: flex` para layouts alinhados. O uso de `justify-content: space-between` permite espaçamento uniforme, e `align-items: flex-end` garante que os elementos fiquem alinhados verticalmente ao final.
