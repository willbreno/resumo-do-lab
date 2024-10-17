# resumo-do-lab
Este repositório contém o resumo das lições aprendidas durante o desenvolvimento do lab Azure na DIO

# Topicos aprendidos no primeiro LAB: 

No primeiro laboratório do Azure, aprendemos sobre o funcionamento da interface do portal Azure e o acesso às diversas funcionalidades e serviços de cloud da Microsoft. Também exploramos a funcionalidade dos servidores de segurança Bastion, que atuam como uma camada de proteção, evitando a necessidade de IPs públicos nos servidores em cloud. O Bastion elimina a exposição das portas 3389 (RDP) para servidores Windows e 22 (SSH) para servidores Linux, aumentando significativamente a segurança. Assim, o acesso é feito exclusivamente através da interface do portal Azure, restringido a computadores previamente autorizados.

Além disso, recebemos informações sobre o SLA (Service Level Agreement) dos serviços oferecidos pela Microsoft e a importância de monitorar o status dos serviços ao configurar seu ambiente cloud. Isso é essencial para evitar interrupções em ambientes de produção, especialmente quando serviços estão baseados em versões prévias, que podem ser descontinuadas pela Microsoft a qualquer momento, causando paradas inesperadas e possíveis prejuízos para as empresas.

# Quais os benefícios de contratação de serviços baseados em nuvem ?  

1 – Alta disponibilidade ( sistema com acesso 24 por 7 com SLA para correção de erros, com prevenção de desastres )  

SLA 99% de disponibilidade, tem limite para indisponibilidade de 7.2 por mês e  1.68 horas por semana e 3.65 dias por ano caso esse tempo seja ultrapassado será gerado créditos na conta azure com forma de ressarcimento.  
SLA 99.9%  tem tolerância para ficar com sistemas foras de 10,1 minutos por semana, 43,2 minutos por mês e 8.76 horas por ano.  
SLA 99,95 tem tolerância para ficar com sistema fora de 5 minutos por semana, 21,6 minutos por mês e 4,38 horas por ano.  
SLA 99,99 tem tolerância para ficar com sistema fora de 1,01 minutos por semana, 4,32  minutos por mês e 52,56 horas por ano.  
SLA 99,999 tem tolerância para ficar com sistema fora de 6 segundos por semana, 25,9 segundos por mês e 5,26 minutos  por ano.  

 

2  - Escalabilidade ( é a capacidade de  ajustar recursos para atender à demanda)  
A capacidade de escalar induz a possibilidade de aumento de recursos de acordo com a demanda seja para um projeto ou para picos de acesso, assim facilitando o controle de gastos pois uma vez que o serviço for contratado, caso o hardware adicional não fizer mais sentido pode ser devolvido para a Microsoft. 

 

3 – Elasticidade: quando não sabemos a quantidade de crescimento de Hardware temos necessidade como por exemplo o período de ofertas Black Friday onde não sabemos a quantidade de acesso que teremos, com esse benefício podemos atribuir recursos para serem aumentados pelo consumo de processador e memoria atingir certos picos, assim tendo uma maior controle de custo conforme a necessidade de uso.  

 

4 – Confiabilidade: serviços com alta disponibilidade, com SLA de disponibilidade de 99%, 99,9%, 99,5% 

Garantindo serviços online, com poucas horarias de falha, e caso ocorrer falhas ressarcimento de créditos na conta do Azure, servidores redundantes em várias localidades, assim caso de perda de funcionamento na localidade de um data center seu serviço pode estar integro rodando de outra localidade isso é um importante pilar para Microsoft sendo atribuída ao framework, Microsoft Azure Well-Architected Framework 

 

5 – Previsibilidade: Permite avanço com confiança nos serviços oferecido pela Microsoft seja na parte de desempenho de hardware e  ou na garantia de custo pelo serviços utilizados durante o período de cobrança, esse aspecto se basea fortemente no pilar Microsoft Azure Well-Architected Framework. 

 

6 - Segurança: O serviço de segurança dos serviços Clouds não e de responsabilidade do provaider (Microsoft), a Microsoft oferece sim ferramentas para implementação de medidas de segurança, mas é de responsabilidade do contratante realizar a instalação e implementações de recursos de segurança  

 

7 - Governança: Auditoria baseada em nuvem, ajuda a sinalizar qualquer recurso que esteja fora de conformidade dos padrões corporativos e fornece estratégias de mitigação, que está muito ligado a segurança, pois as vez se trata de informações sigilosas que não deve ser acessados por qualquer pessoa da organização. 

 

8 – Gerenciabilidade: uma das principais vantagens dos serviços em nuvem é a patricidade de gerenciamento dos recursos computacionais, atraves do portal azure, linha de comando, power shell, API para gerenciamento.  


Para verificar status de indisponibilidade fora do portal azure pode ser verificado no link abaixo:  

 

https://azure.status.microsoft/pt-br/status 

# Tipos de Serviços em servidores cloud. 

IaaS – Infraestrutura como serviço.  

Recursos onde o cliente tende a ter mais contato com o serviço por exemplo configuração de uma máquina virtual na plataforma azure, onde as responsabilidades de configuração e manutenção(atualização e segurança) e de responsabilidade do contratante.   

Características do IaaS: 

Escalabilidade: As empresas podem ajustar a quantidade de recursos utilizados (como poder de computação e armazenamento) de acordo com suas necessidades. 
Pagamento sob demanda: As organizações pagam apenas pelos recursos que consomem, o que reduz os custos iniciais. 
Responsabilidade do usuário: O provedor cuida da infraestrutura, mas a configuração e manutenção de sistemas operacionais, aplicativos e dados ficam sob responsabilidade do usuário. 

Desafios: 

Gerenciamento de recursos: Os usuários precisam gerenciar e configurar seus próprios ambientes. 
Segurança: Embora os provedores cuidem da infraestrutura, a segurança dos dados e das aplicações é responsabilidade do cliente. 
IaaS é ideal para empresas que precisam de controle sobre seus ambientes de TI sem lidar com os custos e a manutenção de uma infraestrutura física própria. 

 

PaaS – Plataforma como serviço. 

Na Plataforma como Serviço (PaaS), o cliente não precisa se preocupar com a configuração ou gerenciamento da infraestrutura subjacente, como servidores, armazenamento ou recursos de rede. Por exemplo, ao configurar um banco de dados em nuvem, o usuário não precisa lidar com a configuração do hardware ou do sistema operacional. O foco está em desenvolver, gerenciar e implantar aplicativos. A plataforma já oferece o ambiente necessário para isso, permitindo que os desenvolvedores concentrem-se na lógica da aplicação e na sua funcionalidade. 

Características do PaaS: 

Ambiente de desenvolvimento completo: O PaaS oferece ferramentas para o desenvolvimento, teste, e implantação de aplicações, como servidores web, bancos de dados e ambientes de integração contínua (CI/CD). 
Abstração da infraestrutura: O provedor de PaaS gerencia a infraestrutura (servidores, redes, armazenamento), enquanto o usuário se concentra apenas no desenvolvimento e na configuração da aplicação. 
Escalabilidade: A plataforma pode ser facilmente escalada conforme a demanda da aplicação aumenta. 

Desafios: 

Menor controle sobre a infraestrutura: Por abstrair a infraestrutura, o usuário tem menos flexibilidade para customizar configurações avançadas. 
Dependência do provedor: As empresas ficam dependentes do provedor de PaaS para atualizações e gerenciamento de infraestrutura, o que pode representar um risco em casos de interrupção do serviço. 


SaaS – Software como serviço.  

No modelo SaaS, tanto a infraestrutura (hardware) quanto o software (aplicação) já estão completamente configurados e gerenciados pelo provedor. O usuário final só precisa acessar e utilizar o serviço, sem se preocupar com a instalação ou manutenção de servidores ou sistemas. O acesso ao software é baseado em licenças, que podem variar de acordo com as funcionalidades e os níveis de segurança oferecidos. Um exemplo de SaaS é o Microsoft 365, onde os recursos disponíveis para o usuário variam conforme o tipo de licença adquirida e as políticas de segurança definidas. 

Características do SaaS: 

Acesso via internet: Os usuários podem acessar o software de qualquer lugar com conexão à internet, através de um navegador. 
Gerenciamento centralizado: O provedor de SaaS cuida de toda a infraestrutura, atualizações, segurança e backups. 
Licenciamento baseado em assinatura: Os usuários pagam pelo acesso ao software com base em um modelo de assinatura, que pode variar conforme o nível de serviço e funcionalidades. 
Nenhuma instalação local necessária: Não há necessidade de instalar o software nos computadores locais, o que facilita o uso e reduz a necessidade de suporte técnico. 

Desafios do SaaS: 

Dependência da internet: O desempenho do software depende de uma conexão estável e de alta velocidade à internet. 
Segurança de dados: Como os dados ficam armazenados na nuvem do provedor, a segurança e privacidade dependem da infraestrutura do provedor, o que pode gerar preocupações para algumas empresas. 
Personalização limitada: As opções de customização podem ser limitadas em comparação com softwares instalados localmente. 

 
# Componentes de Arquiteturas Azure.

Regiões:  
Atualmente o azure está presente em 60 regiões cobrindo 140 países, tornando um serviço global.  
Uma região e a ligação de 3 data center, onde possuem ligações da própria Microsoft chamados de Back bone(comunicação de baixa latência, da própria Microsoft) para compartilhamento de informações.  
Nem todos os recursos estão disponível para todas as regiões.  

Regiões de Disponibilidade:
Cada região do Azure é subdividida em várias Zonas de Disponibilidade (Availability Zones), que consistem em um ou mais data centers equipados com alimentação, rede e refrigeração independentes. Essas zonas são criadas para proteger os aplicativos e os dados contra falhas no nível do data center. 

Benefícios de escolher a região correta: 
Menor latência: Hospedar suas aplicações e dados em uma região próxima dos seus clientes ou usuários finais ajuda a melhorar o desempenho. 
Cumprimento de requisitos de conformidade: Escolher uma região que atenda às regulamentações locais, como o GDPR na Europa, é fundamental para algumas empresas. 
Recuperação de desastres: Ter uma estratégia de backup em regiões geograficamente distribuídas pode ajudar a garantir a continuidade dos negócios em caso de falhas em data centers. 
 
Como escolher a Região do Azure: 
Proximidade: Escolha uma região próxima ao seu público-alvo para garantir baixa latência. 
Serviços disponíveis: Algumas regiões podem não oferecer todos os serviços, por isso é importante verificar se a região escolhida oferece os recursos que você precisa. 
Preços: Os custos dos serviços do Azure podem variar entre regiões, então considerar o orçamento é importante. 
Resiliência e compliance: Dependendo dos requisitos de negócios e regulamentações, pode ser necessário escolher uma região específica para manter a conformidade ou garantir a recuperação de desastres. 

Regiões Pares (Azure Region Pairs): 
As Regiões Pares são um recurso do Azure projetado para aumentar a resiliência e a disponibilidade dos serviços. Cada região do Azure é emparelhada com outra dentro da mesma geografia (por exemplo, East US é emparelhada com West US). Isso significa que, em caso de falha ou indisponibilidade em uma região, a sua região par pode assumir o processamento e os dados, mitigando o impacto de eventuais interrupções.  

Além disso, as regiões pares garantem: 
Replicação automática dos dados entre regiões em cenários de recuperação de desastres. 
Manutenção coordenada, onde atualizações de infraestrutura são feitas de forma a evitar que ambas as regiões sejam afetadas simultaneamente. 
Distância geográfica suficiente entre as regiões para reduzir a probabilidade de desastres naturais impactarem ambas ao mesmo tempo, mas ainda assim garantindo proximidade suficiente para oferecer replicação eficiente. 
Essa estratégia de emparelhamento entre regiões ajuda a garantir alta disponibilidade e continuidade dos serviços, essencial para empresas que dependem de uma infraestrutura sempre ativa.

Regiões Soberanas do Azure: 
As Regiões Soberanas do Azure são regiões especiais onde o acesso e a disponibilidade dos recursos são restritos a um conjunto limitado de organizações ou indivíduos, geralmente por razões de segurança ou requisitos regulatórios específicos. Nesses locais, os dados e serviços são isolados do restante da infraestrutura global do Azure, garantindo que os dados permaneçam dentro de jurisdições e sob regras de governança específicas. 
Essas regiões têm um controle muito mais rigoroso sobre o acesso aos servidores e à infraestrutura. Um exemplo de uma Região Soberana é a Região Governamental dos Estados Unidos ("Azure Government"), que é dedicada a agências governamentais e militares dos EUA. Ela é projetada para atender às exigências legais e regulatórias de segurança, sendo acessível apenas por entidades que atendam aos critérios específicos. 

Em resumo, as Regiões Soberanas oferecem: 
Isolamento total de dados, garantindo que eles não sejam armazenados ou processados fora das fronteiras especificadas. 
Conformidade com regulamentos rigorosos de segurança e privacidade. 
Acesso controlado e restrito a um público-alvo definido, como entidades governamentais ou militares. 
Essas regiões são essenciais para organizações que lidam com dados sensíveis ou que estão sujeitas a normas regulatórias estritas, como é o caso do setor militar ou governamental. 
Temos também a região soberana da China seguindo os mesmo critérios e sendo operado pela uma empresa separada da Microsoft chama 21VIANET 

Grupos de Recursos (Azure Resource Groups): 
Organização de recursos: Os grupos de recursos são utilizados para organizar e gerenciar os recursos do Azure (como VMs, redes, bancos de dados) de forma lógica, facilitando o gerenciamento, controle e aplicação de políticas. 
Imutabilidade do nome: Uma vez criado, o nome de um grupo de recursos não pode ser alterado. Se houver necessidade de um novo nome, é necessário criar um novo grupo de recursos e mover os recursos para ele. 
Movimentação de recursos: É possível mover recursos de um grupo para outro, seja dentro da mesma assinatura ou entre assinaturas diferentes, sem perder a integridade dos dados ou configuração. 
Aplicação de regras e políticas: É possível aplicar políticas e tags nos grupos de recursos para gerenciar a governança, segurança, e conformidade de forma centralizada. 
Existência de recursos: Um recurso só pode pertencer a um único grupo de recursos por vez, mas ele pode ser movido para outro grupo de recursos quando necessário. 
Recursos em regiões diferentes: Embora os recursos estejam vinculados a um grupo de recursos, os próprios recursos podem estar em diferentes regiões. Ou seja, um grupo de recursos pode conter ativos de várias regiões do Azure. 

 Assinaturas do Azure: 
É possível ter mais de uma assinatura por conta no Azure. Isso é útil, por exemplo, para dividir e organizar os serviços e recursos de maneira eficiente. Um cenário comum é ter uma assinatura para Homologação (testes), outra para Produção e, se necessário, até outras assinaturas para diferentes ambientes ou projetos. Isso facilita o gerenciamento, pois separa os recursos e permite uma administração mais clara de cada ambiente. 
As contas de faturamento e os gastos também podem ser divididos por assinatura, o que proporciona um controle financeiro mais preciso, permitindo que os custos sejam segregados por setores ou projetos, evitando confusões na alocação de recursos. 
Isso também nos permite segregar também a questões de acesso aos sistemas, por exemplo uma determinada pessoa só pode ter acesso ao recurso de homologação e não pode ter acesso ao de produção.  
É importante notar que uma assinatura não pode ser vinculada a mais de uma conta. Cada assinatura está associada a uma única conta, o que ajuda a manter uma gestão centralizada e segura dos recursos. 
OBS: um grupo de gerenciamento pode aplicar suas configurações para várias assinaturas.  

Dados data center Microsoft:  
https://datacenters.microsoft.com/globe/explore?info=region_brazilsouth 

#Computação e Redes 

Conjuntos de Disponibilidade de VMs: 
No Azure, é possível criar políticas de disponibilidade para ambientes, permitindo configurar nossas estruturas em diferentes racks, o que garante alta disponibilidade. 

Domínio de Falha 
O domínio de falha refere-se ao rack que abriga os servidores físicos. É ideal que sejam configurados pelo menos três domínios de falha para garantir que, se um rack falhar, os serviços ainda permaneçam disponíveis em outros racks. 

Domínio de Atualização 
O domínio de atualização diz respeito à forma como as atualizações são aplicadas aos servidores. O Azure garante que as atualizações sejam distribuídas entre os diferentes domínios de atualização, evitando que todos os servidores sejam atualizados simultaneamente. Isso minimiza o risco de interrupções nos serviços durante o processo de atualização. 

Área de trabalho virtual do Azure:  
No azure e possível criar ambiente de trabalho remoto para colaboradores, assim ao invés de custo com aquisição de equipamentos físicos, e gasto com envio e tempo de espera até que a mercadoria chegue ao colaborador com área de trabalho virtual e possível realizar de forma rápida, além de reduzir risco de recursos deixados para trás ( equipamentos que não são devolvido com o desligamento do colaborador:   

Contêineres do Azure: 
Os contêineres do Azure oferecem um ambiente leve e virtualizado que elimina a necessidade de gerenciamento do sistema operacional, permitindo uma resposta rápida a alterações sob demanda. Essa abordagem facilita a implementação de aplicativos de forma ágil e escalável. 
Um exemplo popular dessa tecnologia é o Docker, que permite a criação, o gerenciamento e a implementação de contêineres. O Azure integra-se bem ao Docker, possibilitando o uso de serviços como o Azure Container Instances e o Azure Kubernetes Service, que oferecem orquestração e gerenciamento de contêineres em larga escala. 
Além disso, os contêineres garantem consistência entre ambientes de desenvolvimento e produção, reduzindo problemas de compatibilidade e melhorando a eficiência do ciclo de vida do desenvolvimento de software. 
Azure Functions e Serviços de aplicação do Azure:  
Azure Functions é uma oferta de serviço PaaS que dá suporte a operações de computação sem servidor.  
Executa ações dependendo das especificações configuradas para elas serem iniciadas.  

Serviços de aplicativo do Azure:  
Plataforma totalmente gerenciada para a criação, implementação e dimensionamento de APIs ou aplicativos WEB, esta oferta de serviço consiste em uma plataforma PaaS.  
Aceitando as seguintes linguagens:  
.NET, .NET CORE, Node.js, Java, Python PHP.  

Serviços de rede do Azure: 
A rede virtual do Azure(VNet) permite que os recursos do Azure se comuniquem uns com os outros, com a internet e redes locais. 
Pontos de extremidades públicos: acessíveis de  qualquer lugar na internet.  
Pontos de extremidades privados: acessíveis somente de dentro da sua rede.  
As sub-redes virtuais segmentam sua rede para atender ás suas necessidades. 
Gateway de VPN é usado para encaminhar trafego criptografado entre a rede Azure e a rede publica  
ExpressRoute estende as redes locais para rede Azure por meio de uma configuração direta  
DNS do Azure utiliza uma rede global de servidores de nome. 

# Armazenamento 

Contas de armazenamento:  
Deve ter um nome globalmente exclusivo.  
Disponibilizar acesso à internet em todo mundo.  
Deve se definir um serviço de armazenamento e opções de redundancia.  

Redundância de Armazenamento:  
LRS (armazenamento com redundância local) -> Datacenter individual na região primária durabilidade 11 noves  
ZRS (armazenamento com redundância de zona) -> Três zonas de disponibilidade na região primária durabilidade 12 noves 
GRS (armazenamento com redundância geografica) -> Datacenter único no primário e região secundaria durabilidade 16 noves 
GZRS (armazenamento com redundância de zona geogrâfica) -> Três zonas de disponibilidade na região primária e um único datacenter na região secundaria durabilidade de 16 noves 

Blob do Azure:  
Otimizado  para armazenamento de  quantidades massivas de dados não estruturados, como texto ou dados binarios (arquivos como foto, videos, texto entre outros) 

Disco de Azure:  
Fornece discos para máquinas virtuais, aplicativos e outros serviços ( durante a implementação de um novo disco não é necessário a para dos sistemas)  

Fila do Azure:  
Serviço de dico utilizado para armazenamento de mensagens (podendo até armazenar arquivos de mensagem de 64 KB 

Arquivos do Azure:  
Configura um compartilhamento de arquivos de rede altamente disponível  similar ao compartilhamento local de arquivos utilizados em servidores FILE SERVE on premisse.  

Tabelas do Azure:  
Fornece uma opção de chave/atributos para o armazenamento de dados estruturados não relacionais com um  design sem esquemas.  

Camadas de acesso de armazenamento do Azure:  
Frequente: Otimizada para armazenamento de dados acessados com frequencia.  
Esporádico:  
Otimizada para armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 30 dias.  
Frio:  
Otimizado para o armazenamento de dados acessados com pouca frequência e armazenados por pelo menos 90 dias.  

Arquivo Morto:  
Otimizada para o armazenamento de dados acessados raramente e armazenados por pelo menos 180 dias com requisitos de latência flexíveis.  
Migração para o Azure 

Azure Data Box:  
Serviço utilizado para realizar a migração de dados de servidores on premiss para o servidor da microsoft  
Realizando a transferência de até 80 TB de dados.  
Protegendo os dados em caixa robusta durante ao transito para os servidores da Microsoft. 
O Azure DATA BOX e indicados para os cenários onde existe conectividade limitada ou não existe conectividade, migração de dados de locais remotos , complices da empressa contratante ou regulatórias.   

Az Copy: 
Utilitário de linha de comando.  
Copiar blobs ou arquivos de ou para sua conta de armazenamento.  
A sincronização é realizada somente em uma direção.  

Gerenciador de Arquivos do Azure: 
Interface gráfica do usuário ( de modo semelhante ao Windows Explorer) 
Compatível com windows,macos e linux  
Obs: utiliza por trás da interface gráfica comando do Az copy, indica para pessoas que prefira não utilizar linha de comando para realizar essas tarefas de migração.  

Gerenciamento de arquivos:  
Sincroniza os arquivos do Azure e locais de forma bidirecional.  
A camada de nuvem mantém os arquivos acessado com frequência no local enquanto libera espaço.  
