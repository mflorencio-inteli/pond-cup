# Estudo Cypress:

## O que é o Cypress e para que serve?

Cypress é uma ferramenta de teste de software para web front-end. Essa plataforma permite que os desenvolvedores escrevam e executem testes automatizados com eficiência e precisão, focando principalmente na interface do usuário. Com o Cypress, é possível realizar tanto testes de integração, que verificam a coesão e o funcionamento conjunto de várias partes da aplicação, quanto testes End-to-End (E2E), que simulam o comportamento do usuário na aplicação de maneira completa, desde a interação inicial até a conclusão de uma tarefa.

## Vantagens e desvantagens do Cypress em relação a outras ferramentas de teste.

O Cypress se destaca no cenário de ferramentas de automação de testes pelas várias que oferece, diferenciando-se de outras opções disponíveis no mercado. Uma das principais vantagens do Cypress é sua capacidade de fornecer execuções de testes rápidas, consistentes e confiáveis. Graças ao seu design arquitetônico único, ele consegue evitar muitos dos problemas que comumente afetam outras ferramentas de automação, especialmente em relação a inconsistências nos resultados de teste.

Outro diferencial significativo do Cypress é sua resistência a flaky tests, ou seja, testes que apresentam resultados inconsistentes sem qualquer modificação no código. Isso é alcançado por meio da habilidade do Cypress em esperar automaticamente por comandos e asserções antes de prosseguir, eliminando a necessidade de adicionar esperas explícitas ou timeouts, um desafio comum em testes assíncronos.

A depuração é outra área onde o Cypress se destaca. Ele captura instantâneos à medida que os testes são executados, permitindo aos desenvolvedores e testadores ver exatamente o que aconteceu em cada passo do teste. Essa capacidade é reforçada pelo Log de Comandos, que permite a inspeção detalhada dos passos do teste, facilitando a identificação e correção de problemas.

No entanto, apesar dessas vantagens, o Cypress não é isento de desvantagens. Por exemplo, sua abordagem baseada em JavaScript e a execução dentro do navegador podem limitar sua aplicabilidade em alguns contextos, especialmente quando é necessário testar aplicações em uma variedade de navegadores ou realizar testes que envolvam múltiplas origens. Além disso, embora ofereça extensas funcionalidades para aplicações web modernas, pode não ser a ferramenta ideal para todos os tipos de aplicações ou testes, especialmente aqueles que exigem uma interação mais complexa com o sistema operacional ou dispositivos externos.

## Arquitetura do Cypress.

A arquitetura do Cypress funciona diretamente no navegador. Isso elimina a necessidade de um servidor intermediário ou proxy, permitindo um controle mais direto e eficiente sobre a execução dos testes. Essa abordagem direta facilita a depuração, permite a interceptação de chamadas de rede e a simulação de respostas de servidores, além de executar os testes rapidamente .

## Seletores de elementos no Cypress.

O seletor de elementos é uma maneira de identificar elementos específicos da DOM (Documento de Objetos Modelo) de uma página web para interação ou teste. Ele facilita a interação com a UI, usando seletores CSS para manipular elementos. No Cypress, esses seletores funcionam ao permitir que os desenvolvedores especifiquem de maneira precisa quais elementos da interface do usuário (UI) eles desejam manipular ou verificar durante os testes. . Os seletores CSS são amplamente usados devido à sua flexibilidade e capacidade de apontar para elementos de maneira precisa, trazendo o benefício de tornar os testes mais robustos e menos suscetíveis a erros por selecionarem exatamente o elemento desejado, mesmo em uma UI complexa e dinâmica. Esta precisão e facilidade de uso melhoram significativamente a eficácia da automação de testes.

## Comandos e asserções no Cypress.

No Cypress, **comandos** são usados para realizar ações na aplicação, como obter elementos DOM com **`cy.get()`, clicar em elementos, digitar texto, navegar entre páginas etc**. Eles facilitam a interação com a página, permitindo a execução de testes dinâmicos. Esses comandos seguem uma sintaxe encadeada e podem ser combinados com asserções para verificar o estado da aplicação. Eles são fundamentais para simular a interação do usuário e validar a funcionalidade da aplicação web de maneira automatizada.

Já as a**sserções** são verificações que confirmam se um elemento ou situação específica atende a uma expectativa, como **`expect`** ou **`should`**, assegurando que a aplicação se comporta como esperado. Ambos são cruciais para criar testes automatizados robustos e confiáveis no Cypress.

## Descrição das etapas de preparação de um testes de interface, execução e verificação no Cypress.

1. **Preparação**: Instalar o Cypress e configurar o ambiente de testes. Criar arquivos de teste dentro do diretório Cypress e definir cenários de teste específicos, focando nas funcionalidades que se deseja testar.
2. **Execução**: Utilizar os comandos do Cypress para simular ações do usuário, como navegação pela página, cliques, digitação em campos de texto e seleção de elementos. Esses comandos permitem que os testes “interajam” com a aplicação como se fosse um usuário real.
3. **Verificação**: Após a execução de cada ação, verificar o estado da aplicação e garantir que ela está funcionando conforme o esperado. As asserções podem incluir a verificação de textos, estados de elementos, ou qualquer outra condição que reflita o comportamento esperado da aplicação.

## Como estruturar testes de forma eficiente no Cypress?

Para estruturar testes no Cypress de forma eficiente, é fundamental organizar os testes de maneira lógica, separando-os por funcionalidade ou área da aplicação. Utilize a função describe para agrupar testes relacionados e it ou test para cada caso de teste específico. Aproveite recursos como hooks (beforeEach, afterEach) para configurar e limpar o ambiente de teste, minimizando a repetição de código. Adote padrões de nomenclatura claros para facilitar a manutenção e a compreensão dos testes. Implemente a reutilização de código para ações comuns usando funções customizadas ou comandos personalizados do Cypress.
