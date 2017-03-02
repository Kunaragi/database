# Exemples de requetes

## Afficher l'utilisateur dont l'adresse email est : robert@gmail.com

> SELECT * FROM `users` WHERE email = "robert@gmail.com"

## Afficher l'utilisateur dont le token est : secret1

>SELECT * FROM `users` WHERE token = "secret1"

## Afficher les pokemons appartenant au joueur : Bob

> SELECT * FROM `pokemons`,`users` WHERE users.id = pokemons.user_id
AND  users.name = "bob"

## Afficher les pokemons appartenant au dresseur : Oscar

> SELECT * FROM `pokemons`,`users` WHERE users.id = pokemons.user_id
AND  users.name = "Oscar"

## Afficher toutes les pokemons dont la description commence par : Boo

> SELECT * FROM `pokemons` WHERE description LIKE "boo%"

## Afficher toutes les pokemons dont la puissance est egale a : 98

> SELECT * FROM `pokemons` WHERE power = "98"

## Afficher les pokemons dont le nom commence par "moku" et se termine par "ren"

> SELECT * FROM `pokemons` WHERE name LIKE "moku%" AND name LIKE "%ren"

## Afficher tous les pokemons qui appartiennent à : alice@gmail.com

> SELECT * FROM `pokemons`, `users` WHERE users.id =  pokemons.user_id
AND users.email = "alice@gmail.com"

## Afficher toutes les attaques en provenance de : Boo

> SELECT * FROM `pokemons`, `attacks` WHERE pokemons.name = "boo" AND pokemons.id = attacks.src_pokemon_id

## Afficher toutes les attaques à destination de : mokumokuren

> SELECT * FROM `pokemons`, `attacks` WHERE pokemons.name = "mokumokuren" AND pokemons.id = attacks.dst_pokemon_id
