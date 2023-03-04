# DevOpsDays Goiânia - 2023

Talk : Simplificando o DevSecOps <br>
Demonstrando como aplicar ferramentas de segurança Open Source em um pipeline <br>

* GitHub Actions (para montar o workflow de demonstração)
* [Trivy](https://github.com/aquasecurity/trivy) (Para realizar analise da imgem Docker)
  * Para quebra automatica do pipeline, utilizar a opção "exit-code: '1'" no arquivo [main.yml](https://github.com/crypto-br/DevOpsDays_Goiania/blob/main/.github/workflows/main.yml) do actions
  * ```sh
    exit-code: '1'
    ```
* [HoruSec](https://horusec.io/site/) (para análise SAST)
  * Para quebra automatica do pipeline, utilizar a opção  -e="true" na linha de comando do horusec no arquivo [main.yml](https://github.com/crypto-br/DevOpsDays_Goiania/blob/main/.github/workflows/main.yml) do actions:
  * ```sh
    $ horusec start -p="./" -e="true"
    ```
* [OWASP ZAP](https://github.com/zaproxy/zaproxy/) (para análise DAST)

## Resultado da pipeline de demonstração

![Resultado da pipeline do LAB](https://github.com/crypto-br/DevOpsDays_Goiania/blob/main/assets/resultpipeline.jpg)

* [Apresentação em PDF]()

## Links úteis
* [Configurando o Github dependabot](https://docs.github.com/pt/code-security/dependabot/dependabot-alerts/configuring-dependabot-alerts)
* [Lista de ferramentas de segurança da OWASP para DevSecOps e AppSec](https://owasp.org/www-community/Free_for_Open_Source_Application_Security_Tools)
* [Link do TFSEC para configuração](https://aquasecurity.github.io/tfsec/v0.63.1/getting-started/installation/)
* [Link do checkov para configuração](https://www.checkov.io/2.Basics/Installing%20Checkov.html) 
