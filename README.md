# Python CI Pipeline
Repositório criado para aula de ECD11 - Entrega Contínua e DevOps

Este repositório simples implementa um pipeline de Integração Contínua (CI) utilizando **GitHub Actions**. O pipeline é configurado para realizar as seguintes etapas automaticamente:

## Estrutura do Pipeline

1. **Build Automatizado**:
   - Verifica a integridade do código e instala as dependências listadas no `requirements.txt`.
   - É executado em cada commit ou pull request nas branches `main` e `develop`.

2. **Testes Automatizados**:
   - Utiliza o framework `pytest` para rodar testes automatizados localizados na pasta `tests/`.

3. **Análise de Qualidade de Código**:
   - Utiliza a ferramenta `flake8` para verificar a conformidade com o PEP 8 e outras boas práticas de código.
   - Rodado após a etapa de testes, ignorando apenas:
      - E203: Whitespace before ':'
      - E266: Too many leading '#' for block comment
      - E501: Line too long e
      - W503: Line break occurred before a binary operator

4. **Deploy Automatizado (Simulado, pois não tinha base real)**:
   - Simula o processo de deploy após o build e os testes serem bem-sucedidos.

## Como Executar o Pipeline

1. **Commit ou Pull Request**: Sempre que um commit é feito ou um pull request é criado, o pipeline é automaticamente disparado.
2. **Visualizar os Resultados**: Vá para a aba "Actions" no repositório do GitHub para visualizar o progresso e os resultados de cada execução do pipeline.

## Dependências

- **pytest**: Framework de testes.
- **pytest-cov**: Ferramenta de cobertura de código.
- **flake8**: Ferramenta de análise de qualidade de código.

## Diagrama do Pipeline

O diagrama a seguir ilustra as etapas do pipeline de CI:
<img width="1880" alt="Desenho" src="https://github.com/user-attachments/assets/b7fc6ce2-1e09-4e8d-8e09-58e8e4b52acb">

