# App Ride - Documentação

## Visão Geral

O **App Ride** é um aplicativo web para registrar, visualizar e gerenciar trajetos utilizando geolocalização. Ele permite iniciar e parar gravações de rotas, visualizar detalhes de cada trajeto, ver estatísticas como velocidade máxima, distância e duração, além de exibir mapas com o percurso realizado.

---

## Funcionalidades

### 1. Registro de Trajetos

- **Iniciar Trajeto:**  
  Na página `speedometer.html`, ao clicar em **Start**, o app começa a gravar a localização do usuário em tempo real, salvando cada ponto no `localStorage`.

- **Parar Trajeto:**  
  Ao clicar em **Stop**, a gravação é finalizada e o trajeto é salvo.

---

### 2. Listagem de Trajetos

- **Página Inicial (`index.html`):**  
  Exibe todos os trajetos gravados, mostrando:

  - Localização inicial (cidade/país)
  - Velocidade máxima
  - Distância total
  - Duração
  - Data/hora de início
  - Mini-mapa do ponto inicial

- **Clique em um trajeto:**  
  Redireciona para a página de detalhes do trajeto.

---

### 3. Detalhes do Trajeto

- **Página de Detalhes (`detail.html`):**  
  Mostra:
  - Mapa com o percurso completo
  - Estatísticas detalhadas
  - Botão para deletar o trajeto

---

## Explicação dos Arquivos Principais

- **storage.js:**  
  Funções para criar, salvar, deletar e recuperar trajetos do `localStorage`.  
  Cada trajeto é identificado por um ID baseado no timestamp.

- **dataManager.js:**  
  Funções utilitárias:

  - `getLocationData`: Busca informações de cidade/país via API.
  - `getMaxSpeed`: Calcula a velocidade máxima do trajeto.
  - `getDistance`: Calcula a distância total percorrida.
  - `getDuration`: Calcula a duração do trajeto.
  - `getStartDate`: Formata a data/hora de início.

- **index.js:**  
  Carrega todos os trajetos e monta a lista na tela inicial.  
  Cria mini-mapas para cada trajeto usando Leaflet.

- **speedometer.js:**  
  Controla o início/fim da gravação de trajetos.  
  Atualiza a velocidade em tempo real na interface.

- **detail.js:**  
  Exibe detalhes do trajeto selecionado.  
  Mostra o percurso no mapa e estatísticas.  
  Permite deletar o trajeto.

---

## Tecnologias Utilizadas

- HTML5, CSS3, JavaScript
- Bootstrap (estilização)
- Leaflet.js (mapas)
- localStorage (armazenamento local)
- API BigDataCloud (reverse geocoding)

---

## Como Rodar

1. Abra a pasta no VS Code.
2. Use o Live Server (porta 5501) para rodar o projeto.
3. Acesse `index.html` para visualizar e interagir
