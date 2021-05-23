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

## Exemplo de Round
```
Inicio de mediação:
Acusacao: Ronaldinho Gaúcho foi encontrado com cigarro no paraguai
Acusado: Ronaldinho Gaúcho
Promotor: Hebe Camargo
Argumento: Ronaldinho foi encontrado dentro de um monza 1984 com 1000 cigarros atravessando a fronteira
Permissao: ataque
Palavras chave no argumento: [Ronaldinho, Cigarro, Paraguai, Monza, 1984]
Quantidade Chave no Argumento: [1000, 1984]
Terceiros: [Polícia Federal]
ObjecaoQuantidade: 3
CondicaoVitoria: 3 rounds

Mensagem de ataque (parseia as mensagens anteriores e adiciona mais coisas):
Argumento: O safado do ronaldinho foi encontrado com cigarro, monza e muitos homens pelados na fronteira do Paraguai.
Palavras chave no argumento: [Cigarro, Monza, Homens Pelados, Paraguai, Safado]
Quantidade Chave no Argumento: []
Terceiros: [Homens pelados]

Mensagem de defesa (parseia as mensagens anteriores e adiciona mais coisas, sempre acumulativo vendo todas as mensagens anteriores):
Argumento: Não existiam Homens pelados, o cigarro era mentira, o Paraguai não existe. O ataque quer tirar dinheiro do Safado. Hebe Camargo fugiu para o Paraguai
Palavras chave no argumento: [Mentiras]
Quantidade Chave no Argumento: [0]
Terceiros: [Habe Camargo]

Recebimento de mediação:
Argumento: Vamo ver, o bixo está pegando!!!
Palavras chave no argumento: [todos as palavras chaves anteriores sem repetição]
Quantidade Chave no Argumento: [todos os números anteriores sem repetição]
Terceiros: [todos os terceiros envolvidos]
Ganho: 180s para discussão e apoio de algum lado. Humanos lêem os argumentos e votam em qual gostaram mais

PESSOAS VÃO VOTAR COM: Ataque/Defesa, voto único, vale o último.

Resultado de mediação:
Argumento: Lado ataque ganhou
Permissao: Defesa
```

## Premiação

(350x250x3mm)[https://www.aliexpress.com/item/1005002491798093.html]

