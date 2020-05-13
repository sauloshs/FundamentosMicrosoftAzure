# *Fundamentos Microsoft Azure*


## *O que é computação em Nuvem*

É o fornecimento de serviços de computação, incluindo servidores, armazenamento, bancos de dados, rede, software, análise e inteligência, pela Internet (“a nuvem”) para oferecer inovações mais rápidas, recursos flexíveis e economias de escala. Você normalmente paga apenas pelos serviços de nuvem que usa, ajudando a reduzir os custos operacionais, a executar sua infraestrutura com mais eficiência e a escalonar conforme as necessidades da sua empresa mudam.

## *CapEx  vs OpEx*

- Capita Expenditure (CapEx)
  - Gastar em infra-estrutura física antecipadamente.
  - Deduzir a despesa de sua conta de impostos.
  - Alto custo inicial, valor do investimento reduz ao longo do tempo.
- Operational Expenditure (OpEx)
  - Gastar em serviços ou produtos conforme necessário.
  - Seja cobrado imediatamente.
  - Deduzir a despesa de sua conta de impostos no mesmo ano.
  - Sem custo inicial, pague como você usa.

### *Modelo baseado em consumo*

- Sem custos iniciais.
- Não há necessidade de comprar e gerenciar infra-estrutura cara.
- Capacidade de pagar por recursos adicionais como eles são necessários.
- capacidade de pagar por recursos que não são mais necessários.

##  [*Termos de computação em Nuvem*](Termos.md)

## *Tipos de Nuvem*

### *Nuvem Pública*

As nuvens públicas são a maneira mais comum de implantar a computação em nuvem. Os recursos de nuvem (como servidores e armazenamento) pertencem a um provedor de serviço de nuvem terceirizado, são operados por ele e entregues pela Internet. O Microsoft Azure é um exemplo de nuvem pública. Com uma nuvem pública, todo o hardware, software e outras infraestruturas de suporte são de propriedade e gerenciadas pelo provedor de nuvem. Em uma nuvem pública, você compartilha os mesmos dispositivos de hardware, de armazenamento e de rede com outras organizações ou “locatários” da nuvem. Você acessa serviços e gerencia sua conta usando um navegador da Web. As implantações de nuvem pública geralmente são usadas para fornecer email baseado na Web, aplicativos de escritório online, armazenamento e ambientes de desenvolvimento e teste.

### *Nuvem Privada*

Uma nuvem privada consiste em recursos de computação usados exclusivamente por uma única empresa ou organização. A nuvem privada pode estar localizada fisicamente no datacenter local da sua organização ou pode ser hospedada por um provedor de serviços terceirizado. Mas em uma nuvem privada, os serviços e a infraestrutura são sempre mantidos na rede privada e o hardware e o software são dedicados unicamente à sua organização. Dessa forma, com a nuvem privada é mais fácil para que a organização personalize seus recursos a fim de atender a requisitos de TI específicos. As nuvens privadas geralmente são usadas por órgãos governamentais, instituições financeiras e outras organizações de grande porte com operações críticas para os negócios, que buscam melhorar o controle sobre seu ambiente.

### *Nuvem Híbrida*

Geralmente chamadas de “o melhor dos dois mundos”, as nuvens híbridas combinam a infraestrutura local, ou seja, as nuvens privadas, com as nuvens públicas, permitindo que as organizações aproveitem as vantagens de ambas as opções. Em uma nuvem híbrida, dados e aplicativos podem ser movidos entre as nuvens públicas e privadas, o que oferece maior flexibilidade e mais opções de implantação. Por exemplo, você pode usar a nuvem pública para necessidades de volume grande e segurança mais baixa, como email baseado na Web, e a nuvem privada (ou outra infraestrutura local) para operações confidenciais críticas, como relatórios financeiros. Em uma nuvem híbrida, o “cloud bursting” também é uma opção. “Cloud bursting” ocorre quando um aplicativo ou recurso é executado na nuvem privada até que haja um pico de demanda (por exemplo, um evento sazonal como compras online ou envio de impostos) e, nesse ponto, a organização pode “estourar” para a nuvem pública para fazer uso de recursos de computação adicionais.

## **Regiões**

- Uma região representa uma coleção de data centers.
- Proporciona flexibilidade e escala.
- Preserva a residência de dados.
- Seleciona regiões próximas aos seus usuários.
- Esteja ciente da disponibilidade de implantação da região.
- Existem serviços globais que são independentes da região. 

## **Pares de região**

- cada região do Azure é emparelhada com outra região.
- Azure prefere pelo menos 300 milhas de separação entre data centers em um par regional.
- Alguns serviços fornecem replicação automática para a região emparelhada.
- Em uma paralisação, a recuperação de uma região é priorizada de cada par.
- As atualizações do sistema Azure são distribuídas para regiões emparelhadas sequencialmente (não ao mesmo tempo).
- Regiões pareadas são membros da mesma geografia - exceto o Brasil.

## **Zona geográfica**

- Mercados discretos que preservam os limites de residência e conformidade de dados.
- Normalmente contêm duas ou mais regiões.
- Permitir que clientes com residência de dados e conformidade específicas mantenham seus dados e aplicativos próximos.
- Categorizandos como ***Américas, Europa, Ásia-Pacífico, Oriente Médio e África***

## **Availability sets**

Mantenha os aplicativos online durante a manutenção ou falha de hardware.

- **Update domains (UD)** - As atualizações programadas de manutenção, desempenho ou segurança são sequenciadas através de domínios de atualização.
- **Fault domains (FD)** - Forneça uma separação física de cargas de trabalho em diferentes hardwares em um data center.

## **Availability zones**

- Locais fisicamente separados dentro de uma região Azure.
- Leva os conjuntos de disponibilidade para o próximo nível.
- Inclui um ou mais data centers, equipados com energia independentes, resfriamento e rede.
- Atua como um limite de isolamento.
- Se uma zona de disponibilidade cair a outra continua funcionando.

## **Resource groups**

- Contêineres para múltiplos recursos que compartilham o mesmo ciclo de vida.
- Agrega recursos em uma única unidade gerenciável.
- cada recurso do Azure deve existir em um (e apenas um) grupo de recursos.
- Seguro no nível de grupo de recursos (ou recurso) - usando o **RBAC** (Role- Based Access Control, controle de acesso baseado em função).

## **Azure Resource Manager**

- Fornece uma camada de gerenciamento que permite criar, atualizar e excluir recursos em sua assinatura.
- Criar, configurar, gerenciar e excluir recursos e grupos.
- Organizar recursos.
- Controle de acesso e recursos.
- Automatiza usando diferentes ferramentas e SDKs.

## **Azure Compute Services**

VM (Máquinas Virtuais) do Azure é um dos vários tipos de [recursos de computação sob demanda escalonáveis](https://docs.microsoft.com/pt-br/azure/architecture/guide/technology-choices/compute-decision-tree) oferecidos pelo Azure. Normalmente, você escolhe uma VM quando precisar de mais controle sobre o ambiente de computação do que as outras opções oferecem. Este artigo fornece informações sobre o que você deve considerar antes de criar uma VM, como criá-la e como gerenciá-la.

- **Azure VMs** - Usa infraestrutura como serviço (IaaS) para fornecer poder de computação na nuvem.
- **VM scale sets** - São projetados para dimensionamento automático de VMs idênticos.
- **App services** - É uma plataforma como um serviço (PaaS) que oferece para construir, implantar e dimensionar aplicativos web, mobile e API de nível corporativo.
- **Functios** - Realizar ações de computação com base em um evento.

## **Scale Sets**

Os conjuntos de dimensionamento de máquinas virtuais do Azure lhe permitem criar e gerenciar um grupo de VMs idênticas e com balanceamento de carga. O número de instâncias de VM pode aumentar ou diminuir automaticamente em resposta à demanda ou a um agendamento definido. Os conjuntos de dimensionamento fornecem alta disponibilidade para seus aplicativos e permitem que você gerencie, configure e atualize um grande número de máquinas virtuais de forma centralizada. Com conjuntos de dimensionamento de máquinas virtuais, você pode criar serviços em grande escala para áreas como computação, big data e cargas de trabalho de contêiner.

## **Container services.**

Containers é um ambiente de virtualização. No entanto, ao contrário das máquinas viruasi, você não gerencia um sistema operacional. Os contêineres são feitos para serem leves, e foram projetados para serem ccriados, dimensionados e parados dinamicamente. 

- **Azure Container Instances** - Uma oferta PaaS que permite que você carregue seus contêineres, que estão serão executados para você.
- **Azure Kubernetes Service** - Um serviço de orquestração de contêineres para gerenciar um grande número de contêineres. 