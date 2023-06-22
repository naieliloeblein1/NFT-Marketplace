# OpenD

Projeto realizado no curso The Complete 2023 Web Development Bootcamp, que possui como objetivo ser um Marketplace de NFT, onde as pessoas possam cunhar, listar e vender suas NFTS.

## Tecnologias Utilizadas

- ReactJS
- Motoko

## Instruções de instalação e execução do projeto

1. Clone este repositório: `git clone https://github.com/seu-usuario/NFT-Marketplace.git`

2. Navegue até o diretório do projeto: `cd NFT-Marketplace`

3. Para iniciar localmente o dfx: `dfx start --clean`

4. Instale as dependências: `npm install`

5. Inicie o servidor de desenvolvimento: `npm start`

6. Faça deploy dos canisters:`dfx deploy --argument='("CryptoDunks #123", principal "z2vzc-7cqcg-zzz23-rltbv-tukax-rxopr-4mw6b-kwdyg-cc3oy-sncs4-zqe", (vec {137; 80; 78; 71; 13; 10; 26; 10; 0; 0; 0; 13; 73; 72; 68; 82; 0; 0; 0; 10; 0; 0; 0; 10; 8; 6; 0; 0; 0; 141; 50; 207; 189; 0; 0; 0; 1; 115; 82; 71; 66; 0; 174; 206; 28; 233; 0; 0; 0; 68; 101; 88; 73; 102; 77; 77; 0; 42; 0; 0; 0; 8; 0; 1; 135; 105; 0; 4; 0; 0; 0; 1; 0; 0; 0; 26; 0; 0; 0; 0; 0; 3; 160; 1; 0; 3; 0; 0; 0; 1; 0; 1; 0; 0; 160; 2; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 160; 3; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 0; 0; 0; 0; 59; 120; 184; 245; 0; 0; 0; 113; 73; 68; 65; 84; 24; 25; 133; 143; 203; 13; 128; 48; 12; 67; 147; 94; 97; 30; 24; 0; 198; 134; 1; 96; 30; 56; 151; 56; 212; 85; 68; 17; 88; 106; 243; 241; 235; 39; 42; 183; 114; 137; 12; 106; 73; 236; 105; 98; 227; 152; 6; 193; 42; 114; 40; 214; 126; 50; 52; 8; 74; 183; 108; 158; 159; 243; 40; 253; 186; 75; 122; 131; 64; 0; 160; 192; 168; 109; 241; 47; 244; 154; 152; 112; 237; 159; 252; 105; 64; 95; 48; 61; 12; 3; 61; 167; 244; 38; 33; 43; 148; 96; 3; 71; 8; 102; 4; 43; 140; 164; 168; 250; 23; 219; 242; 38; 84; 91; 18; 112; 63; 0; 0; 0; 0; 73; 69; 78; 68; 174; 66; 96; 130;}))'`

7. Acesse o localhost:`http://localhost:8080/`

## Criando NFT para teste

1. Crie um NFT na linha de comando para obter NFT em mapOfNFTs:`dfx canister call opend mint '(vec {137; 80; 78; 71; 13; 10; 26; 10; 0; 0; 0; 13; 73; 72; 68; 82; 0; 0; 0; 10; 0; 0; 0; 10; 8; 6; 0; 0; 0; 141; 50; 207; 189; 0; 0; 0; 1; 115; 82; 71; 66; 0; 174; 206; 28; 233; 0; 0; 0; 68; 101; 88; 73; 102; 77; 77; 0; 42; 0; 0; 0; 8; 0; 1; 135; 105; 0; 4; 0; 0; 0; 1; 0; 0; 0; 26; 0; 0; 0; 0; 0; 3; 160; 1; 0; 3; 0; 0; 0; 1; 0; 1; 0; 0; 160; 2; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 160; 3; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 0; 0; 0; 0; 59; 120; 184; 245; 0; 0; 0; 113; 73; 68; 65; 84; 24; 25; 133; 143; 203; 13; 128; 48; 12; 67; 147; 94; 97; 30; 24; 0; 198; 134; 1; 96; 30; 56; 151; 56; 212; 85; 68; 17; 88; 106; 243; 241; 235; 39; 42; 183; 114; 137; 12; 106; 73; 236; 105; 98; 227; 152; 6; 193; 42; 114; 40; 214; 126; 50; 52; 8; 74; 183; 108; 158; 159; 243; 40; 253; 186; 75; 122; 131; 64; 0; 160; 192; 168; 109; 241; 47; 244; 154; 152; 112; 237; 159; 252; 105; 64; 95; 48; 61; 12; 3; 61; 167; 244; 38; 33; 43; 148; 96; 3; 71; 8; 102; 4; 43; 140; 164; 168; 250; 23; 219; 242; 38; 84; 91; 18; 112; 63; 0; 0; 0; 0; 73; 69; 78; 68; 174; 66; 96; 130;}, "CryptoDunks #123")'`

2. Liste o item em mapOfListings:`dfx canister call opend listItem '(principal "<REPLACE WITH NFT CANISTER ID>", 2)'`

3. Obtenha o ID da caixa OpenD:`dfx canister id opend`

4. Transfira NFT para OpenD:`dfx canister call <REPLACE WITH NFT CANISTER ID> transferOwnership '(principal "ryjl3-tyaaa-aaaaa-aaaba-cai", true)'`

## Conectando-se ao Token Canister

1. Defina o ID da caixa do token em <SUBSTITUA PELO TOKEN CANISTER ID>:`const dangPrincipal = Principal.fromText("<SUBSTITUA PELO TOKEN CANISTER ID>");`

## Estrutura do Projeto

NFT-Marketplace/
├── src/
│ ├── NFT/ # Diretório contendo o back-end do NFT em Motoko
│ ├── opend/ # Diretório contendo o back-end do opend em Motoko
│ ├── opend_assets/  
│ ├── src/ # Diretório principal do código ReactJS.
│ ├── components/ # Diretório contendo os componentes reutilizáveis da aplicação.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request :)

## Liçenca

Copyright 2022 London App Brewery LTD (www.appbrewery.com)

The code in this tutorial project is licended under the Apache License, Version 2.0 (the "License");
you may not use this project except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Here is the TL;DR version of the above licence:
https://tldrlegal.com/license/apache-license-2.0-(apache-2.0)
