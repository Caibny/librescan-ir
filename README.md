<div align="center">

# 📷 LibreScan IR

**Sistema Open Source de Rastreabilidade Óptica, Auditoria Industrial e Inventário**

![Status](https://img.shields.io/badge/Status-MVP_Funcional-28A745?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![OpenCV](https://img.shields.io/badge/Visão_Computacional-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)

</div>

---

### 📌 Sobre o Projeto

O **LibreScan IR** é um terminal de rastreabilidade e auditoria projetado para ambientes industriais, linhas de produção e controle de inventário/EPIs. Desenvolvido para operar **100% localmente** sem dependência de nuvem, o sistema utiliza visão computacional via webcam para leitura de alta velocidade de códigos **1D e 2D (padrão GS1 e QR Code)**, evitando duplicidades e falhas operacionais.

---

### ⚙️ Funcionalidades Principais

* **Leitura Óptica em Alta Velocidade:** Captura e decodificação contínua de códigos de barras 1D (GS1) e QR Codes via webcam, com controle de intervalo (*cooldown*) para bloquear leituras duplicadas.
* **Auditoria & Conformidade:** Validação automática contra o cadastro de SKUs e tratamento dedicado para itens não cadastrados durante a operação.
* **Gestão de Estoque & Movimentação:** Controle de entradas, saídas, separação de materiais/EPIs e contagem automatizada de etiquetas.
* **Dashboard Analítico & Logs:** Painel local com histórico completo de transações e exportação direta de relatórios para **Excel (`.xlsx` / `.csv`)**.

---

### 🏗️ Stack Tecnológica

| Camada | Tecnologia | Função no Sistema |
| :--- | :--- | :--- |
| **Back-end** | Python + Flask | Rotas da aplicação, regras de auditoria e API local |
| **Visão Computacional** | OpenCV / Pyzbar | Captura de vídeo e decodificação óptica 1D/2D |
| **Banco de Dados** | SQLite | Armazenamento local portátil de SKUs e logs |
| **Exportação & BI** | Pandas / OpenPyXL | Geração de planilhas de auditoria para Excel |

---

### 🚀 Como Executar Localmente

```bash
# 1. Clone o repositório
git clone [https://github.com/Caibny/librescan-ir.git](https://github.com/Caibny/librescan-ir.git)
cd librescan-ir

# 2. Instale as dependências
pip install -r requirements.txt

# 3. Inicie o servidor local
python app.py
