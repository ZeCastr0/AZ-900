# laboratorio-dio
Repositório para realizar atividades educacionais da DIO referente a AZ-900

---

📘 AZ-900 – Fundamentos de Cloud (Microsoft Azure)

Este repositório foi criado com o objetivo de registrar estudos e atividades práticas realizadas durante o curso preparatório para a certificação AZ-900 – Microsoft Azure Fundamentals.

Durante o desenvolvimento deste material, foram abordados conceitos fundamentais relacionados à computação em nuvem, incluindo:

---

## 📘 Módulo 1 – Conceitos de Cloud

---

### ☁️ Modelos de Nuvem
- Nuvem Pública  
- Nuvem Privada  
- Nuvem Híbrida  
- Diferenças, vantagens e cenários de utilização de cada modelo  

---

### 💰 Modelos de Custos em Cloud
- Conceito de CAPEX (Capital Expenditure)  
- Conceito de OPEX (Operational Expenditure)  
- Comparação entre custos tradicionais de infraestrutura e custos em computação em nuvem  

---

### ⚙️ Assinaturas e Recursos no Azure
- Processo de criação de assinaturas  
- Organização e gerenciamento de recursos no Azure  
- Estrutura básica de governança na plataforma  

---

### 🚀 Benefícios da Computação em Nuvem

**Alta Disponibilidade**  
Serviços em nuvem oferecem altos níveis de SLA (Service Level Agreement), como 99%, 99,5% e 99,99%, garantindo maior tempo de disponibilidade. Em casos de descumprimento, pode haver compensações financeiras (estornos).

**Exemplo:**  
99% → ~7 horas de indisponibilidade/mês  
99,9% → ~43 minutos/mês  
99,99% → ~4 minutos/mês  

**Escalabilidade**  
Capacidade de aumentar ou reduzir recursos conforme a demanda, permitindo atender crescimento do sistema sem necessidade de investimento antecipado em infraestrutura.

**Elasticidade**  
Permite que os recursos sejam ajustados automaticamente para lidar com picos de uso inesperados, garantindo performance mesmo em situações não previstas.

**Segurança e Governança**  
Aplicação de políticas de acesso, controle de identidade e permissões, garantindo que apenas usuários autorizados tenham acesso aos recursos.

**Confiabilidade**  
Infraestrutura distribuída globalmente, com redundância e tolerância a falhas, garantindo maior estabilidade e continuidade dos serviços.

---

### 🧩 Tipos de Serviços em Cloud

**Infraestrutura como Serviço (IaaS)**  
Fornece recursos básicos de computação, como máquinas virtuais, redes e armazenamento. O usuário tem maior controle sobre o ambiente, sendo responsável por sistemas operacionais e aplicações.

**Plataforma como Serviço (PaaS)**  
Oferece um ambiente completo para desenvolvimento, testes e implantação de aplicações, sem a necessidade de gerenciar a infraestrutura. O provedor cuida do sistema operacional, banco de dados e runtime.

**Software como Serviço (SaaS)**  
Disponibiliza aplicações prontas para uso via internet, sem necessidade de instalação ou gerenciamento técnico por parte do usuário. O provedor é responsável por toda a infraestrutura e manutenção.

![Tipos de Servico](image-1.png)

---

### 🔐 Modelo de Responsabilidade Compartilhada

Na computação em nuvem, a responsabilidade pela segurança e gerenciamento dos recursos é dividida entre o provedor de nuvem e o cliente. Essa divisão varia conforme o tipo de serviço utilizado (IaaS, PaaS e SaaS).

#### 🧱 Infraestrutura como Serviço (IaaS)

**Responsabilidade do Cliente:**
- Sistema operacional  
- Configurações de rede  
- Aplicações instaladas  
- Atualizações e patches  
- Dados  

**Responsabilidade do Provedor:**
- Datacenter físico  
- Hardware  
- Rede física  
- Virtualização  

➡️ Maior controle para o cliente, porém maior responsabilidade  

---

#### ⚙️ Plataforma como Serviço (PaaS)

**Responsabilidade do Cliente:**
- Aplicações desenvolvidas  
- Configuração das aplicações  
- Dados  

**Responsabilidade do Provedor:**
- Sistema operacional  
- Runtime  
- Middleware  
- Infraestrutura (rede, servidores, armazenamento)  

➡️ Equilíbrio entre controle e responsabilidade  

---

#### 💻 Software como Serviço (SaaS)

**Responsabilidade do Cliente:**
- Dados  
- Configuração de uso (acessos, permissões)  

**Responsabilidade do Provedor:**
- Aplicação  
- Sistema operacional  
- Infraestrutura completa  
- Segurança física e lógica da plataforma  

➡️ Menor responsabilidade para o cliente, foco apenas no uso  

![Grafico de Responsabilidade Compartilhada](image.png)

---

## 📘 Módulo 2 – Arquitetura do Azure

---

### 🏗️ Arquitetura do Azure

A arquitetura do Microsoft Azure é baseada em uma estrutura global distribuída, organizada em regiões, zonas de disponibilidade, assinaturas e grupos de recursos, permitindo alta disponibilidade, escalabilidade e governança eficiente.

---

### 🌎 Regiões

As regiões são conjuntos de datacenters localizados em diferentes áreas geográficas ao redor do mundo. Cada região é projetada para oferecer alta disponibilidade e redundância.

**Exemplo:** Brasil Sul, East US, West Europe  
![Regioes](image-2.png)

➡️ Permitem escolher onde os dados e aplicações serão hospedados  

---

🌐 Pares de Regiões (Region Pairs)

O Azure organiza as regiões em pares, chamados de "Region Pairs". Cada região possui uma região secundária associada dentro da mesma geografia.

➡️ Em caso de falha na região principal, a região pareada pode ser utilizada como recuperação  
➡️ Atualizações planejadas são distribuídas entre as regiões do par para evitar indisponibilidade simultânea  
➡️ Auxilia em estratégias de disaster recovery (recuperação de desastre)  

Exemplo:  
Brasil Sul → South Central US (região pareada)

---

### 🏢 Zonas de Disponibilidade

As zonas de disponibilidade são datacenters fisicamente separados dentro de uma mesma região. Cada zona possui energia, rede e refrigeração independentes.

➡️ Garantem alta disponibilidade e tolerância a falhas  
➡️ Se uma zona falhar, outra continua operando  

![Zonas](image-3.png)

---


🛠️ Gerenciamento de Recursos no Azure

O Azure oferece uma estrutura organizada para criação, gerenciamento e controle dos recursos através de diferentes níveis.

➡️ Facilita a organização, controle de acesso e governança dos recursos na nuvem  

**Hierarquia de Gerenciamento:**

Management Groups (Grupos de Gerenciamento)  
➡️ Utilizados para organizar múltiplas assinaturas  
➡️ Permitem aplicar políticas e controle de acesso em larga escala  

Subscriptions (Assinaturas)  
➡️ Unidade de cobrança e controle de acesso  
➡️ Contém grupos de recursos  

Resource Groups (Grupos de Recursos)  
➡️ Container lógico para agrupar recursos relacionados  
➡️ Permite gerenciar recursos como um conjunto  

Resources (Recursos)  
➡️ Elementos individuais, como máquinas virtuais, bancos de dados, storage, etc.  

---

📌 Resumo da Hierarquia

Management Group → Assinatura → Grupo de Recursos → Recursos  

➡️ Cada nível herda permissões e políticas do nível superior  

![Hierarquia](image-4.png)


### 📦 Assinaturas

A assinatura é uma unidade de gerenciamento no Azure que organiza e controla o uso dos recursos.

➡️ Define limites de cobrança (billing)  
➡️ Controla acesso e permissões  
➡️ Permite separar ambientes (ex: dev, teste, produção)  

![Assinaturas](image-5.png)

---

### 📁 Grupos de Recursos

Os grupos de recursos são containers lógicos utilizados para agrupar recursos relacionados de uma aplicação.

➡️ Facilitam o gerenciamento conjunto dos recursos  
➡️ Permitem aplicar permissões e políticas  
➡️ Todos os recursos dentro do grupo podem ser gerenciados como um conjunto  

---

### 📌 Resumo

- Região → Onde os recursos estão hospedados  
- Zona de Disponibilidade → Alta disponibilidade dentro da região  
- Assinatura → Controle de acesso e cobrança  
- Grupo de Recursos → Organização lógica dos recursos  
