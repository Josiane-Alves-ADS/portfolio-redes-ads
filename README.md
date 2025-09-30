# 🌐 Portfólio: Projeto de Rede Corporativa com VLANs

Este projeto simula a configuração de uma **rede corporativa** para a empresa fictícia **SuperTech**, utilizando o simulador **Cisco Packet Tracer**. O principal objetivo foi aplicar conceitos de segmentação de rede, VLANs, roteamento e distribuição de endereçamento IP.

---

## 🛠️ Detalhes da Topologia e Equipamentos

### Topologia
* **Topologia:** Estrela Parcialmente Encadeada, adaptada devido às limitações do simulador (Roteador IR829).
* **Segmentação:** A rede é dividida em quatro setores principais: **Engenharia, Compras, TI Interno e Infraestrutura**.

### Equipamentos Utilizados
* **Roteador:** 1 x Roteador Cisco IR829.
* **Switches:** 5 x Switches Cisco 2950T-24 (Um para cada setor e um central para interconexão).
* **Dispositivos Finais:** Total de 80 PCs, 8 Servidores e 8 Impressoras (20 PCs, 2 Servidores e 2 Impressoras por setor).

---

## ⚙️ Configurações Principais

### Endereçamento IP e Segmentação
* **Faixa Base:** O endereçamento IP base utilizado é `192.168.1.x` com máscara `/27` para cada sub-rede.
* **VLANs:** A rede está organizada globalmente em duas VLANs por setor:
    * **VLAN 10:** Para 10 computadores, 1 servidor e 1 impressora.
    * **VLAN 20:** Para 10 computadores, 1 servidor e 1 impressora.
* **Roteamento:** Foi configurado o **Router-on-a-Stick** (Roteamento entre VLANs) utilizando subinterfaces no roteador.

### Distribuição de Serviços
* **DHCP:** Utilizado nos setores de **Compras** e **Infraestrutura** para PCs e Impressoras.
* **IP Estático:** Utilizado nos setores de **Engenharia** e **TI Interno** para todos os dispositivos, e nos Servidores de todos os setores.

---

## 📝 Documentação e Como Acessar

Para visualizar o projeto e as configurações, você precisará ter o **Cisco Packet Tracer** instalado.

1.  **Baixe:** Faça o download do arquivo `.pkt` (o arquivo do projeto) deste repositório.
2.  **Abra:** Abra o arquivo diretamente no Cisco Packet Tracer.
3.  **Análise:** Você pode inspecionar as configurações de *interfaces*, *VLANs*, e *DHCP* em cada dispositivo.

### Arquivos Adicionais
* **`Portifolio Redes de Computadores - Josiane Alves da Silva (2025).pdf`:** Relatório completo do portfólio, detalhando a INTRODUÇÃO, ENDEREÇAMENTO IP, AJUSTES E CONCLUSÃO do projeto.

---

## ✅ Resultados e Conclusão

O projeto foi implementado com sucesso, validando a **comunicação satisfatória** em testes de ping entre dispositivos na mesma VLAN, em VLANs diferentes (validando o roteamento) e entre os setores. A adaptação da topologia para contornar a limitação do simulador demonstrou flexibilidade na resolução de problemas.
