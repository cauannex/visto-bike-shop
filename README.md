# Visto Bike Shop

**Landing page conceitual para uma bicicletaria da Vila Mariana, em São Paulo.**

Projeto de Front-End desenvolvido para apresentar bicicletas, serviços de oficina e conversão elétrica em uma experiência visual que conecta a descoberta da loja ao contato com a equipe.

A proposta combina direção visual esportiva, navegação simples e animações de rolagem. O foco é permitir que o visitante conheça os serviços, explore categorias de bicicletas e encontre os canais de atendimento sem precisar de cadastro.

> **Status:** protótipo independente para apresentação e portfólio. Não é o site oficial da Visto Bike Shop. Identidade visual, imagens e conteúdo estão sujeitos à aprovação da empresa.

## Experiência e funcionalidades

- Página de abertura com fotografia, chamadas para ação e navegação por seções.
- Faixa de texto com animação contínua em formato de esteira.
- Vitrine horizontal de bicicletas com filtros por categoria e controles de navegação.
- Cena vetorial de ciclismo com deslocamento vinculado à rolagem da página.
- Apresentação de revisão, ajustes, personalização e conversão elétrica.
- Links para WhatsApp com texto pré-preenchido, Instagram e telefone.
- Acesso à localização por uma pesquisa de rota no Google Maps.
- Preenchimento verde gradual nos botões transparentes ao passar o mouse ou receber foco pelo teclado.
- Layout responsivo para diferentes tamanhos de tela.

As bicicletas da vitrine são ilustrações conceituais de categorias. O projeto não consulta estoque, processa pedidos ou realiza pagamentos. Os links de WhatsApp preenchem uma mensagem; o envio é realizado pelo visitante.

## Tecnologias

| Tecnologia | Aplicação |
| --- | --- |
| HTML5 | Estrutura da página e conteúdo |
| CSS3 | Layout, responsividade, transições e animações |
| JavaScript | Filtros, navegação do carrossel e efeitos de rolagem |
| SVG | Ilustrações de bicicletas e da cena de ciclismo |
| Intersection Observer API | Exibição progressiva de seções |
| `requestAnimationFrame` | Atualização visual dos efeitos de rolagem |

O projeto não utiliza frameworks, dependências externas de JavaScript, banco de dados ou etapa de compilação. CSS e JavaScript estão incorporados ao `index.html`.

## Estrutura do repositório

- `index.html` — página principal, estilos, scripts e ilustrações SVG.
- `assets/bike.jpg` — fotografia ilustrativa utilizada na abertura.
- `README.md` — documentação do projeto.

## Executar localmente

Clone o repositório, entre na pasta criada e abra o arquivo `index.html` em um navegador atualizado. Mantenha a pasta `assets` no mesmo diretório do HTML para carregar a fotografia corretamente.

Se preferir acessar por um servidor local e tiver Python instalado, execute na raiz do projeto:

```bash
python -m http.server 8000
```

Depois, acesse [http://localhost:8000](http://localhost:8000).

## Personalização

Os principais pontos de edição estão no `index.html`:

- **Paleta:** variáveis CSS em `:root`, incluindo `--green`, `--black` e `--muted`.
- **Vitrine:** lista `products` no JavaScript, responsável pelas categorias e pelos textos dos cartões.
- **Contato:** atributos `data-chat` e número utilizado para construir os links `wa.me`.
- **Localização e redes sociais:** links na seção de visita à loja.
- **Fotografia de abertura:** arquivo `assets/bike.jpg` e referência em `.hero:before`.
- **Velocidade da esteira:** duração da animação `visto-ticker`.

## Acessibilidade e movimento

A implementação inclui indicação visual de foco, identificação de controles, estado dos filtros com `aria-pressed` e suporte à preferência `prefers-reduced-motion`. Quando essa preferência está ativa, a esteira é interrompida e os efeitos de movimento são reduzidos.

Esses recursos fazem parte da implementação, mas não representam certificação de conformidade nem substituem uma auditoria de acessibilidade.

## Publicação

O site pode ser servido por uma plataforma de hospedagem estática, preservando `index.html` na raiz e a pasta `assets` ao lado dele.

Para a Vercel, a configuração prevista é:

| Configuração | Valor |
| --- | --- |
| Framework Preset | `Other` |
| Root Directory | Raiz do projeto |
| Build Command | Sem comando de build |
| Output Directory | `.` |

Antes de publicar para uma empresa, confirme as condições e os limites do plano escolhido. O plano Hobby da Vercel é destinado a projetos pessoais e não comerciais. Um domínio próprio requer registro e configuração de DNS separados da implementação do site.

## Contexto do projeto

Este trabalho explora como um site institucional pode organizar informações de um comércio local e facilitar o contato de potenciais clientes. O desenvolvimento prioriza hierarquia visual, adaptação a dispositivos móveis e interações que reforçam a identidade esportiva da proposta.

A implementação atual é uma demonstração. Não há métricas de conversão, resultados comerciais comprovados ou integração de estoque.

## Créditos e uso de marca

Desenvolvimento e proposta: **Cauan Matos Moura Silva**.

O nome Visto Bike Shop é utilizado para contextualizar a proposta independente. Não implica vínculo, contratação ou aprovação da empresa. A fotografia de abertura é ilustrativa, obtida do Unsplash; as ilustrações de bicicletas estão definidas em SVG no código.

Antes de uma publicação oficial, devem ser confirmados os direitos de uso dos materiais, o logotipo, a paleta, os contatos, os serviços e as imagens aprovadas pela loja. A presença desses materiais neste repositório não concede direitos sobre marcas ou imagens de terceiros.
