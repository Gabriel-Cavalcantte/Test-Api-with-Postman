<h1 style="color: orange; font-size: 20px;">Automação de API com Postman e Newman</h1>

<p>Este projeto tem como objetivo demonstrar exemplos práticos de automação de testes de API utilizando Postman em conjunto com Newman para execução em pipelines CI/CD.</p>
<p>A integração com GitHub Actions permite a execução automatizada dos testes em diferentes ambientes, com geração de relatórios detalhados para análise dos resultados.</p>

<h1 style="color: orange; font-size: 20px;">Tecnologias Utilizadas</h1>

<ul>
  <li><strong>Postman:</strong> <a href="https://www.postman.com/" style="color: orange;">Postman</a></li>
  <li><strong>Newman:</strong> <a href="https://learning.postman.com/docs/running-collections/using-newman-cli/command-line-integration-with-newman/" style="color: orange;">Newman CLI</a></li>
  <li><strong>Node.js:</strong> <a href="https://nodejs.org/" style="color: orange;">Node.js</a></li>
  <li><strong>GitHub Actions:</strong> <a href="https://github.com/features/actions" style="color: orange;">GitHub Actions</a></li>
</ul>

<h1 style="color: orange; font-size: 20px;">Dependências</h1>

<p>Para instalar as dependências necessárias para a execução do projeto, utilize o seguinte comando:</p>
<p><code style="color: red;">npm install -g newman newman-reporter-html</code></p>
<p>Esse comando irá instalar o Newman (executor de coleções Postman) e o reporter HTML para geração de relatórios detalhados.</p>

<h1 style="color: orange; font-size: 20px;">Execução de Testes</h1>

<h2 style="color: orange; font-size: 16px;">Localmente</h2>

<p>Para executar os testes localmente, utilize o seguinte comando:</p>

<pre><code>newman run test\collections\api-tests.json</code></pre>

<h2 style="color: orange; font-size: 16px;">Via GitHub Actions</h2>

<p>Os testes são executados automaticamente no pipeline CI/CD quando:</p>
<ul>
  <li>Há um push para a branch <code>main</code></li>
  <li>Há um pull request para a branch <code>main</code></li>
</ul>

<p>O relatório HTML é gerado automaticamente e disponibilizado como artefato para download.</p>

<h1 style="color: orange; font-size: 20px;">Estrutura do Projeto</h1>

<ul>
  <li><strong>collections/</strong> - Armazena a coleção Postman com os testes de API (<code>api-tests.json</code>)</li>
  <li><strong>environment/</strong> - Contém os arquivos de configuração de ambiente (<code>dev.environment.json</code>)</li>
  <li><strong>reports/newman/</strong> - Diretório onde são gerados os relatórios de execução (<code>report.html</code>)</li>
  <li><strong>.github/workflows/</strong> - Configuração do pipeline CI/CD (<code>postman-tests.yml</code>)</li>
</ul>

<h1 style="color: orange; font-size: 20px;">Configuração de Ambientes</h1>

<p>O projeto suporta múltiplos ambientes através de arquivos específicos:</p>
<ul>
  <li><strong>dev.environment.json</strong> - Configurações para ambiente de desenvolvimento</li>
  <li>(Futuras implementações podem incluir ambientes de staging e produção)</li>
</ul>