# Segurança do Firebase — Tania Parfum

Este repositório usa o Realtime Database do Firebase no projeto `taniaparfum233`.

## Arquivo de regras

As regras seguras estão no arquivo:

```text
firebase-database.rules.json
```

## Como aplicar no Firebase Console

1. Acesse o Firebase Console.
2. Entre no projeto `taniaparfum233`.
3. Vá em **Realtime Database**.
4. Abra a aba **Rules**.
5. Copie o conteúdo de `firebase-database.rules.json`.
6. Cole nas regras do Realtime Database.
7. Clique em **Publish**.

## O que estas regras fazem

- O catálogo público pode ler produtos, preços, esgotados, carrossel e configurações públicas.
- Apenas usuários logados no Firebase Auth podem alterar produtos, preços, esgotados, carrossel e configurações.
- Backups e dados de vendas ficam privados para usuários autenticados.
- A raiz do banco fica bloqueada por padrão.

## Caminhos públicos somente leitura

- `produtos_estaticos`
- `produtos_custom`
- `precos`
- `esgotados`
- `carrossel`
- `config`

## Caminhos privados

- `backup`

## Importante

Estas regras protegem o banco, mas precisam ser publicadas manualmente no Firebase Console para terem efeito. Apenas commitar o arquivo no GitHub não altera as regras do Firebase automaticamente.
