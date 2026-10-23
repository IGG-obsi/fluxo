# Fluxo — app financeiro pessoal

App de fluxo de caixa com saldo projetado dia a dia, no método da Escola do Breno.
Funciona offline no celular (Android) e no PC, e sincroniza os dois pelo GitHub.

## 1. Colocar o app online (uma vez só, ~5 min, grátis)

O app precisa de um endereço https para ser instalável e funcionar offline. O jeito mais simples é o GitHub Pages:

1. Crie uma conta em github.com (se ainda não tiver).
2. Clique em **New repository** → nome `fluxo` → marque **Public** → **Create repository**.
3. Na página do repositório: **Add file → Upload files** → arraste **todo o conteúdo** desta pasta
   (`index.html`, `manifest.webmanifest`, `sw.js` e a pasta `icons`) → **Commit changes**.
4. Vá em **Settings → Pages** → em *Branch* escolha `main` e `/ (root)` → **Save**.
5. Depois de 1–2 minutos, o app fica em `https://SEU-USUARIO.github.io/fluxo/`.

> O código fica público, mas **seus dados não**: eles ficam só nos seus aparelhos (e no seu gist secreto, se ligar a sincronização).

## 2. Instalar

- **Android (Chrome):** abra o endereço → menu ⋮ → **Instalar app** (ou "Adicionar à tela inicial").
- **PC (Chrome ou Edge):** abra o endereço → ícone de instalar na barra de endereço (ou menu → "Instalar Fluxo").

Depois de aberto uma vez, funciona sem internet.

## 3. Sincronizar celular ↔ PC (opcional, recomendado)

1. github.com → foto do perfil → **Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token (classic)**.
   Marque **somente `gist`**, validade "No expiration" (ou a que preferir) → gere e copie o token.
2. No **primeiro aparelho**: Fluxo → menu → *sincronizar celular ↔ PC* → cole o token → **criar gist**. Copie o ID que aparece.
3. No **outro aparelho**: mesmo lugar → cole o token **e** o ID → **conectar / sincronizar agora**.

Daí em diante ele sincroniza sozinho sempre que houver internet. Lançou algo offline? Fica guardado e sobe quando a conexão voltar.
Se editar nos dois aparelhos, as alterações são juntadas (vale a mais recente de cada lançamento).

## 4. Atualizar o app no futuro

Suba o novo `index.html` no repositório e troque `fluxo-v1` por `fluxo-v2` no `sw.js`. Os aparelhos pegam a versão nova na próxima abertura (às vezes precisa abrir duas vezes).

## Atalhos

- tocar no **número do dia** = check-in ✓
- tocar no **valor/saldo** = ver e editar o dia
- **segurar** a célula (ou botão direito no PC) = lançar
- **arrastar** a lista para os lados = trocar o filtro
- ícone de **grade** = horizonte de 12 meses
- **calendário** = voltar para hoje
