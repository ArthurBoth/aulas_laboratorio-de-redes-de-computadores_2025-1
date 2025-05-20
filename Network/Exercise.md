# Configurando Subredes com IPv4 e Roteamento Estático

|Alunos
|-----------------
|[Arthur Antunes de Souza Both](https://github.com/ArthurBoth)
|[Paola Lopes](https://github.com/thepaola)
|[Maria Eduarda Maia](https://github.com/DudaWendelMaia)

## Objetivo

Criar e configurar uma rede local, usando um simulador de rede para exercitar a
configuração do endereçamento IPv4 e do roteamento estático.

## Descrição

1. Usando o simulador crie uma rede local, contendo os seguintes elementos:

   - Pelo menos 5 Roteadores: os roteadores devem estar conectados entre si, por
   enlaces ponto-a-ponto, formando o backbone da rede local.
   - Pelo menos 2 subredes com hosts ao todo: para a criação da subrede
   conecte um switch Ethernet em cada roteador, para ligação de computadores
   e outros dispositivos.

   ![Unlabeled Diagram](images/Unlabeled_Diagram.png)

2. A rede local deve atender os seguintes requisitos quanto ao endereçamento,
roteamento e tradução de endereços:

   - Deve ser utilizado um endereço público para o endereçamento das subredes.
   Utilize as máscaras de subrede que forem mais adequadas para o seu projeto
   de endereçamento.
   - Deve ser configurado o roteamento estático nos 5 roteadores da sua rede
   local, devendo haver conectividade entre todas as subredes.

   ```plaintext
   Escolhemos por ter duas redes, uma com 4 e outra com 2 subredes.
   Esta é uma tabela com os endereços IPs e as máscaras de subrede:
   ```

   | Endereço de Rede | Endereço de Broadcast | Máscara de rede |      Intervalo de endereços
   |:----------------:|:---------------------:|:---------------:|:-------------------------------:
   |  200.151.10.0    |     200.151.10.127    | 255.255.255.128 | 200.151.10.1   - 200.151.10.126
   |  200.151.10.128  |     200.151.10.255    | 255.255.255.128 | 200.151.10.129 - 200.151.10.254
   |  200.251.10.0    |     200.251.10.63     | 255.255.255.192 | 200.251.10.1   - 200.251.10.62
   |  200.251.10.64   |     200.251.10.127    | 255.255.255.192 | 200.251.10.65  - 200.251.10.126
   |  200.251.10.128  |     200.251.10.191    | 255.255.255.192 | 200.251.10.129 - 200.251.10.190
   |  200.251.10.192  |     200.251.10.255    | 255.255.255.192 | 200.251.10.193 - 200.251.10.254

   ![Labeled Diagram](images/Labeled_Diagram.png)

3. Após a criação e configuração da rede local no simulador, gere tráfego com ping a
partir dos hosts e dos roteadores para validar a sua configuração.

   ### Evidências

   #### R1

   ![R1 IP](images/ip_tables/r1_ip.png)

   ![Ping R1-R2](images/pings/r1-r2.png)

   ![Ping R1-R3](images/pings/r1-r3.png)

   ![Ping R1-R4](images/pings/r1-r4.png)

   ![Ping R1-R5](images/pings/r1-r5.png)

   ![Ping R1-PC1](images/pings/r1-pc1.png)

   ![Ping R1-PC2](images/pings/r1-pc2.png)

   ![Ping R1-PC3](images/pings/r1-pc3.png)

   ![Ping R1-PC4](images/pings/r1-pc4.png)

   #### R2

   ![R2 IP](images/ip_tables/r2_ip.png)

   ![Ping R2-R1](images/pings/r2-r1.png)

   ![Ping R2-R3](images/pings/r2-r3.png)

   ![Ping R2-R4](images/pings/r2-r4.png)

   ![Ping R2-R5](images/pings/r2-r5.png)

   ![Ping R2-PC1](images/pings/r2-pc1.png)

   ![Ping R2-PC2](images/pings/r2-pc2.png)

   ![Ping R2-PC3](images/pings/r2-pc3.png)

   ![Ping R2-PC4](images/pings/r2-pc4.png)

   #### R3

   ![R3 IP](images/ip_tables/r3_ip.png)

   ![Ping R3-R1](images/pings/r3-r1.png)

   ![Ping R3-R2](images/pings/r3-r2.png)

   ![Ping R3-R4](images/pings/r3-r4.png)

   ![Ping R3-R5](images/pings/r3-r5.png)

   ![Ping R3-PC1](images/pings/r3-pc1.png)

   ![Ping R3-PC2](images/pings/r3-pc2.png)

   ![Ping R3-PC3](images/pings/r3-pc3.png)

   ![Ping R3-PC4](images/pings/r3-pc4.png)

   #### R4

   ![R4 IP](images/ip_tables/r4_ip.png)

   ![Ping R4-R1](images/pings/r4-r1.png)

   ![Ping R4-R2](images/pings/r4-r2.png)

   ![Ping R4-R3](images/pings/r4-r3.png)

   ![Ping R4-R5](images/pings/r4-r5.png)

   ![Ping R4-PC1](images/pings/r4-pc1.png)

   ![Ping R4-PC2](images/pings/r4-pc2.png)

   ![Ping R4-PC3](images/pings/r4-pc3.png)

   ![Ping R4-PC4](images/pings/r4-pc4.png)

   #### R5

   ![R5 IP](images/ip_tables/r5_ip.png)

   ![Ping R5-R1](images/pings/r5-r1.png)

   ![Ping R5-R2](images/pings/r5-r2.png)

   ![Ping R5-R3](images/pings/r5-r3.png)

   ![Ping R5-R4](images/pings/r5-r4.png)

   ![Ping R5-PC1](images/pings/r5-pc1.png)

   ![Ping R5-PC2](images/pings/r5-pc2.png)

   ![Ping R5-PC3](images/pings/r5-pc3.png)

   ![Ping R5-PC4](images/pings/r5-pc4.png)

   #### PC1

   ![PC1 IP](images/ip_tables/pc1_ip.png)

   ![Ping PC1-R1](images/pings/pc1-r1.png)

   ![Ping PC1-R2](images/pings/pc1-r2.png)

   ![Ping PC1-R3](images/pings/pc1-r3.png)

   ![Ping PC1-R4](images/pings/pc1-r4.png)

   ![Ping PC1-R5](images/pings/pc1-r5.png)

   ![Ping PC1-PC2](images/pings/pc1-pc2.png)

   ![Ping PC1-PC3](images/pings/pc1-pc3.png)

   ![Ping PC1-PC4](images/pings/pc1-pc4.png)

   #### PC2

   ![PC2 IP](images/ip_tables/pc2_ip.png)

   ![Ping PC2-R1](images/pings/pc2-r1.png)

   ![Ping PC2-R2](images/pings/pc2-r2.png)

   ![Ping PC2-R3](images/pings/pc2-r3.png)

   ![Ping PC2-R4](images/pings/pc2-r4.png)

   ![Ping PC2-R5](images/pings/pc2-r5.png)

   ![Ping PC2-PC1](images/pings/pc2-pc1.png)

   ![Ping PC2-PC3](images/pings/pc2-pc3.png)

   ![Ping PC2-PC4](images/pings/pc2-pc4.png)

   #### PC3

   ![PC3 IP](images/ip_tables/pc3_ip.png)

   ![Ping PC3-R1](images/pings/pc3-r1.png)

   ![Ping PC3-R2](images/pings/pc3-r2.png)

   ![Ping PC3-R3](images/pings/pc3-r3.png)

   ![Ping PC3-R4](images/pings/pc3-r4.png)

   ![Ping PC3-R5](images/pings/pc3-r5.png)

   ![Ping PC3-PC1](images/pings/pc3-pc1.png)

   ![Ping PC3-PC2](images/pings/pc3-pc2.png)

   ![Ping PC3-PC4](images/pings/pc3-pc4.png)

   #### PC4

   ![PC4 IP](images/ip_tables/pc4_ip.png)

   ![Ping PC4-R1](images/pings/pc4-r1.png)

   ![Ping PC4-R2](images/pings/pc4-r2.png)

   ![Ping PC4-R3](images/pings/pc4-r3.png)

   ![Ping PC4-R4](images/pings/pc4-r4.png)

   ![Ping PC4-R5](images/pings/pc4-r5.png)

   ![Ping PC4-PC1](images/pings/pc4-pc1.png)

   ![Ping PC4-PC2](images/pings/pc4-pc2.png)

   ![Ping PC4-PC3](images/pings/pc4-pc3.png)
