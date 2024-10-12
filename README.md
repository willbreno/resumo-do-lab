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

 
