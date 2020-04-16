# Trabalho de DevOps
# Autores
Esse trabalho foi desenvolvido em conjunto com Tiago Rockenbach e Nadine Anderle.
# Descrição do trabalho
Para que se mantenham competitivas no mercado as empresas de TI necessitam utilizar ferramentas e estratégias que assegurem qualidade e rapidez nas entregas de seus produtos, e devido isso se torna imprescindível a adoção de uma Governança de TI  eficiente com métodos que a fundamentem. Frente a esse cenário o DevOps, é a metodologia que permite e fundamenta essas entregas. O DevOps, é bem mais do que um conjunto de software e ferramentas que permitem a execução de entregas rápidas e com qualidade, mas se trata de uma cultura que deve ser adotada por todas as áreas das empresas que desejam aplicar o DevOps em seu cotidiano. 

Com o objetivo de fixar os conhecimentos explanados na disciplina de DevOps, foi realizada a construção de um pipeline de CI/CD  utilizando  o GitLab SaaS.

URL do projeto criado para consulta: [https://gitlab.com/tiagorockenbach/teste].

As vantagens identificadas no GitLab em relação ao Jenkins são, não é necessário executar a instalação de plugins adicionais, além disso, o mesmo oferece um Container Registry interno para o Docker e por ser um serviço não necessita nenhum instalação local, tendo escala sob demanda. O GitLab também possibilita realizar o deploy automático através do GitLab Runner, permitindo a execução em ambiente local com configurações simplificadas, ou até mesmo em clusters Kubernetes.

Para a construção do Pipeline, foram utilizadas algumas tecnologias, tais como NodeJS e Express para a construção da API, a biblioteca Chai para construção dos testes automatizados. No que se refere a conteinerização foi utilizado o Docker e também como imagem base o Docker In Docker.

O Pipeline criado, possui quatro etapas, build onde é realizada a construção do aplicativo, test onde é executado a etapa de testes unitários para verificar a operabilidade da API construída, publish onde a aplicação é copiada para um container Docker, criada uma imagem e a mesma é enviada ao Container Registry do GitLab, e por fim, o deploy que é executado a partir da imagem criada no passo anterior e copiada para execução  na máquina local através do GitLab Runner.
