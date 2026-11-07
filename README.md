# Proteção da Natureza (prona) — versão 2.0.0

Código revisto em novembro de 2026. Verificado com `dart analyze`: **0 erros, 0 avisos**.

## Conteúdo
- `lib/` — todo o código da app (194 ficheiros).
- `pubspec.yaml` — dependências atualizadas.
- `analysis_options.yaml` — regras de análise.
- `PERMISSOES.md` — permissões de câmara e localização (Android e iOS).

## Não incluído (fica no projeto original)
- `android/`, `ios/` (ou gerar com `flutter create .`, ver abaixo);
- `images/` e `pdf/` (assets).

## Como montar
1. Fazer cópia de segurança do projeto atual.
2. Copiar `lib/`, `pubspec.yaml` e `analysis_options.yaml` para o projeto,
   substituindo os existentes. Apagar do projeto os ficheiros antigos que já
   não existem em `lib/` (por exemplo `lib/Home/`, `lib/main_1.dart`, os
   `*home.dart`, `Rotas/Pesca/conc/`, `Rotas/Pesca/zpl/`, `Rotas/id/Singular/`
   e `Rotas/id/Coletiva/`). A forma mais simples é apagar a pasta `lib/`
   antiga e pôr esta no lugar.
3. Se faltarem as pastas `android/` ou `ios/`, correr na raiz do projeto:
   `flutter create --project-name prona --org pt.desenhodados .`
   (não altera `lib/` nem o `pubspec.yaml`).
4. Acrescentar as permissões indicadas em `PERMISSOES.md`.
5. `flutter pub get` e depois `flutter analyze`.
6. Confirmar que os logótipos dos sites de interesse estão em `images/`.
