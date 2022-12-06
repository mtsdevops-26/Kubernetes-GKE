# Kubernetes-GKE

O Google Kubernetes Engine (GKE) é um serviço Kubernetes totalmente gerenciado para implantação, gerenciamento e dimensionamento de aplicativos em contêineres no Google Cloud.

Neste repositorio, nos iremos implantar um cluster GKE de pool de nós gerenciado separadamente de 3 nós usando o Terraform. Este cluster do GKE será distribuído em várias zonas para alta disponibilidade. Em seguida, você configurará kubectlusando a saída do Terraform para implantar um painel do Kubernetes no cluster.

# Por que implantar com o Terraform?  

Embora você possa usar os processos integrados de provisionamento do GCP (IU, SDK/CLI) para clusters do GKE, o Terraform oferece vários benefícios:

***Fluxo de trabalho unificado*** - se você já estiver implantando infraestrutura no Google Cloud com o Terraform, seu cluster do GKE pode se encaixar nesse fluxo de trabalho. Você também pode implantar aplicativos em seu cluster do GKE usando o Terraform.

***Gerenciamento completo do ciclo de vida*** - O Terraform não apenas cria recursos, mas também atualiza e exclui recursos rastreados sem exigir que você inspecione a API para identificar esses recursos.

***Gráfico de Relacionamentos*** - O Terraform entende os relacionamentos de dependência entre os recursos. Por exemplo, se você precisar de um pool de nós gerenciado separadamente, o Terraform não tentará criar o pool de nós se houver falha na criação do cluster do GKE.
