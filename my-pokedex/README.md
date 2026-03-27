## My Pokédex

Aplicativo mobile em React Native com Expo, usado em aulas práticas de desenvolvimento mobile, no formato de uma Pokédex.

Atualmente o projeto contém:

- **Tela de Login** (`src/pages/Login`)
- **Tela de Listagem de Pokémon** (`src/pages/PokemonList`) com dados mockados
- **Tela de Detalhe de Pokémon** (`src/pages/PokemonDetail`) com dados mockados
- **Serviço de API** (`src/services/pokeapi.ts`) já estruturado para consumir a [PokéAPI](https://pokeapi.co)
- **Sistema de temas** (`src/global/themes.tsx`) com paleta inspirada na Pokédex e suporte a modo claro/escuro

> Atenção: neste momento as telas ainda **não estão conectadas entre si** (sem navegação) e os dados mostrados são estáticos. A integração com a API será feita nas aulas.

---

## Pré-requisitos

- **Node.js** (versão LTS recomendada)
- **npm** (vem junto com o Node.js)
- **Expo Go** instalado no celular  
  - Android: disponível na Google Play Store  
  - iOS: disponível na App Store

Opcional (para emuladores):

- Android Studio (emulador Android)
- Xcode (emulador iOS, apenas em macOS)

---

## Como rodar o projeto localmente

1. **Clonar o repositório**

   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd my-pokedex
   ```

2. **Instalar as dependências**

   ```bash
   npm install
   ```

3. **Iniciar o servidor do Expo**

   ```bash
   npx expo start
   ```

   Isso irá abrir a interface do Expo no navegador e/ou no terminal.

4. **Rodar no celular (recomendado)**

   - Conecte o celular e o computador **na mesma rede Wi‑Fi**.
   - Abra o aplicativo **Expo Go** no celular.
   - No navegador/terminal, leia o **QR Code** com o aplicativo Expo Go.
   - Aguarde o bundle carregar e o app será aberto.

5. **Rodar em emulador (opcional)**

   Com o servidor Expo rodando (`npx expo start`):

   - Para Android:

     ```bash
     npx expo start --android
     ```

   - Para iOS (apenas macOS):

     ```bash
     npx expo start --ios
     ```

---

## Estrutura básica do projeto

```text
my-pokedex/
  App.tsx                  # Ponto de entrada, hoje exibindo a tela de Login
  src/
    global/
      themes.tsx           # Definição de temas (claro/escuro) no padrão Pokédex
    pages/
      Login/
        index.tsx          # Página de login
        styles.ts          # Estilos da página de login
      PokemonList/
        index.tsx          # Página de listagem (mock)
        styles.ts          # Estilos da página de listagem
      PokemonDetail/
        index.tsx          # Página de detalhes (mock)
        styles.ts          # Estilos da página de detalhes
    services/
      pokeapi.ts           # Funções para consumir a PokéAPI (ainda não usadas nas páginas)
    @types/
      png.d.ts             # Tipagem para import de imagens PNG
```

---

## Próximos passos (para as aulas)

- Adicionar **navegação** entre as três telas (por exemplo, usando React Navigation).
-.Substituir os dados mockados pela resposta real da **PokéAPI**:
  - Listagem de Pokémon com paginação.
  - Detalhamento de um Pokémon (stats, tipos, altura, peso etc.).
- Evoluir o layout e a experiência de uso.

