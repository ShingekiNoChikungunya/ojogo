# O JOGO

```
sudo pacman -Syu stack
stack install
stack build
stack run
```

* Como editar o .cabal: [Manual](https://www.haskell.org/cabal/release/cabal-1.10.1.0/doc/users-guide/#package-descriptions)
* Documentação de bot no Telegram: [API](https://core.telegram.org/bots/api)
* Exemplo de requests com JSON em Haskell: [Exemplo](https://github.com/PedroHLC/haskell-openstack-req/tree/master/src)

## Descrição

`${SOMEONE}` está sendo julgado numa corte.
Seu bot deve assumir o papel de advogado da defesa ou do ataque.
Seres Humanos são testemunhas. O administrador é o JUIZ.
Seu bot pode usar OBJEÇÕES.

## Protocolo

```
JUIZ: Libera quem pode falar quando
ATAQUE: Acusa X
DEFESA: Defende X



Inicio de mediação:
Acusacao: argumento
Acusado: quem esta sendo acusado
Promotor: quem acusa
Argumento: Argumento em texto
Permissao: ataque/defesa (quem pode falar)
Palavras chave no argumento: [lista de palavras chave do argumento]
Quantidade Chave no Argumento: [Números chaves utilizados na argumentação]
Terceiros: [lista de terceiros envolvidos, pode ser adicionado um terceiro a qualquer momento]
ObjecaoQuantidade: Número de objeções
CondicaoVitoria: Quantas vitórias para ganhar o caso

Mensagem de ataque:
Argumento: Argumento em texto
Palavras chave no argumento: [lista de palavras chave do argumento]
Quantidade Chave no Argumento: [Números chaves utilizados na argumentação]
Terceiros: [lista de terceiros envolvidos, pode ser adicionado um terceiro a qualquer momento]

Mensagem de defesa:
Argumento: Argumento em texto
Palavras chave no argumento: [lista de palavras chave do argumento]
Quantidade Chave no Argumento: [Números chaves utilizados na argumentação]
Terceiros: [lista de terceiros envolvidos, pode ser adicionado um terceiro a qualquer momento]

Recebimento de mediação:
Argumento: Argumento em texto
Palavras chave no argumento: [lista de palavras chave do argumento]
Quantidade Chave no Argumento: [Números chaves utilizados na argumentação]
Terceiros: [lista de terceiros envolvidos, pode ser adicionado um terceiro a qualquer momento]
Permissao: ataque/defesa (quem pode falar)
Ganho: 180s para discussão e apoio de algum lado. Humanos lêem os argumentos e votam em qual gostaram mais


Objeção (sempre recebida pela mediação):
Argumento: Argumento em texto
Palavras chave no argumento: [lista de palavras chave do argumento]
Quantidade Chave no Argumento: [Números chaves utilizados na argumentação]
Terceiros: [lista de terceiros envolvidos, pode ser adicionado um terceiro a qualquer momento]
Quantidade: Numero de objeções restantes

```

## Premiação

(350x250x3mm)[https://www.aliexpress.com/item/1005002491798093.html]

