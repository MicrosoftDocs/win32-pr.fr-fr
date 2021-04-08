---
title: Chaînes UrlPrefix
description: Dans l’API du serveur HTTP, un UrlPrefix est une chaîne Unicode à caractères larges (UTF-16) avec une forme canonique qui spécifie une section d’espace de noms d’URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- API serveur HTTP des chaînes UrlPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734740"
---
# <a name="urlprefix-strings"></a>Chaînes UrlPrefix

Dans l’API du serveur HTTP, un *URLPrefix* est une chaîne Unicode à caractères larges (UTF-16) avec une forme canonique qui spécifie une section d’espace de noms d’URL. Elle est utilisée pour réserver une section de l’espace de noms d’URL pour un compte d’utilisateur ou pour enregistrer une section d’espace de noms d’URL pour un processus.

## <a name="urlprefix-format"></a>Format UrlPrefix

Un UrlPrefix a la syntaxe suivante :

« schéma://Host : port/relativeURI »

Les éléments de schéma, d’hôte et de port d’un UrlPrefix doivent être présents et non vides, et doivent respecter les règles suivantes :

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>mode
</dt> <dd>

Doit être http ou HTTPS, tout en minuscules.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>HBA
</dt> <dd>

Il doit s’agir d’un nom de domaine complet, d’une chaîne littérale IPv4 ou IPv6 ou d’un caractère générique. Contrairement au schéma, qui doit être en minuscules, la partie hôte ne respecte pas la casse. Selon la façon dont la partie hôte est spécifiée, un UrlPrefix se trouve dans l’une des quatre catégories de routage suivantes, qui sont décrites plus en détail ci-dessous :

<dl> <dd>Caractère générique fort</dd> <dd>Explicite</dd> <dd>Caractère générique faible lié à IP</dd> <dd>Caractère générique faible</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>importer
</dt> <dd>

Chaîne numérique décimale qui ne commence pas par zéro et qui représente un numéro de port TCP valide (1 à 65 535). Cette valeur ne peut pas être un caractère générique.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

L’élément relativeURI est facultatif, mais s’il est présent, il doit toujours être suivi d’une barre oblique ("/"). Il s’agit d’une chaîne de préfixe qui indique une sous-arborescence au sein de l’espace de noms de l’ordinateur, spécifiée par rapport aux valeurs de schéma, d’hôte et de port. Contrairement au schéma, qui doit être en minuscules, la partie relativeURI ne respecte pas la casse.

</dd> </dl>

Voici quelques exemples de UrlPrefixes correctement formés :

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Catégories de Host-Specifier

Pour une flexibilité et une facilité d’utilisation, l’API du serveur HTTP prend en charge quatre façons différentes de spécifier des hôtes. Les quatre catégories Host-specifier sont répertoriées ci-dessous par ordre de priorité :

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Caractère générique fort (signe plus)
</dt> <dd>

Lorsque l’élément hôte d’un UrlPrefix se compose d’un seul signe plus (+), le UrlPrefix correspond à tous les noms d’hôtes possibles dans le contexte de ses éléments Scheme, port et relativeURI et est inclus dans la catégorie caractère générique forte.

Un caractère générique fort est utile lorsqu’une application doit traiter les demandes adressées à un ou plusieurs relativeURIs, quelle que soit la façon dont ces demandes arrivent sur l’ordinateur ou le site qu’elles spécifient dans leurs en-têtes d’hôte. Dans ce cas, l’utilisation d’un caractère générique fort vous évite de devoir spécifier une liste exhaustive des adresses hôte et/ou IP.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicitement
</dt> <dd>

Un nom d’hôte explicite, tel qu’un nom de domaine complet dans l’élément hôte, place un UrlPrefix dans la catégorie explicite. Ce type d’élément hôte est mis en correspondance directement avec les en-têtes d’hôte des requêtes entrantes.

Les spécifications d’hôte explicites sont utiles pour les applications multisites, telles que les serveurs Web qui fournissent des contenus différents en fonction du site vers lequel la demande a été dirigée.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Caractère générique faible lié à IP
</dt> <dd>

Quand une adresse IP apparaît en tant qu’élément hôte, le UrlPrefix se trouve dans la catégorie caractère générique faible liée à IP. Ce type de UrlPrefix correspond à n’importe quel nom d’hôte pour l’interface IP spécifiée avec le schéma, le port et le relativeURI spécifiés, et qui n’a pas déjà été mis en correspondance par un caractère générique fort ou un UrlPrefix explicite. L’adresse IP prend l’une des deux formes suivantes dans l’élément hôte :

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Chaîne littérale IPv4
</dt> <dd>

Un littéral IPv4 se compose de quatre nombres décimaux séparés par des points, chacun dans la plage 0-255, comme 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Chaîne littérale IPv6
</dt> <dd>

Une chaîne littérale IPv6 est placée entre crochets et contient des nombres hexadécimaux séparés par des signes deux-points ; par exemple :: \[ 1 \] ou \[ 3FFE : FFFF :: 6ECB : 0101 \] .

</dd> </dl>

Les spécificateurs d’hôte avec caractère générique faible liés à IP sont destinés aux applications qui font varier le contenu qu’ils servent en fonction de l’itinéraire utilisé par les demandes entrantes. Ne comptez pas sur les spécificateurs d’hôte avec caractère générique faible lié à IP pour appliquer la sécurité.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Caractère générique faible (astérisque)
</dt> <dd>

Lorsqu’un astérisque ( \* ) apparaît en tant qu’élément hôte, le URLPrefix se trouve dans la catégorie caractère générique faible. Ce type de UrlPrefix correspond à n’importe quel nom d’hôte associé au schéma, au port et au relativeURI spécifiés qui n’a pas déjà été mis en correspondance par un UrlPrefix avec caractères génériques forts, explicites ou avec des caractères génériques faibles liés à l’adresse IP.

Cette spécification de l’hôte peut être utilisée comme valeur par défaut de rattrapage dans certaines circonstances, ou peut être utilisée pour spécifier une grande section de l’espace de noms d’URL sans avoir à utiliser de nombreux UrlPrefixes.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Détection de conflit UrlPrefix pendant la réservation et l’inscription

À des fins de réservation et d’enregistrement, les quatre catégories différentes de UrlPrefix sont traitées séparément, sans référence les unes aux autres. Il est possible d’enregistrer les UrlPrefixes en conflit tant qu’ils se trouvent dans des catégories différentes. Une tentative de réservation échoue uniquement dans la même catégorie.

Par exemple, il est possible de réserver à la fois les UrlPrefix explicites `https://www.adatum.com:80/vroot/` et les URLPrefix génériques forts en conflit `https://+:80/vroot/` , car ils appartiennent à des catégories différentes. Toutefois, une tentative ultérieure de réservation https://+:80/vroot/ à un autre utilisateur échoue, car elle serait en conflit avec une réservation existante dans sa propre catégorie.

## <a name="routing-behavior"></a>Comportement de routage

Lors du routage d’une requête HTTP entrante, l’API du serveur HTTP commence par la catégorie de caractères génériques forts et compare l’URL entrante avec les UrlPrefixes inscrits et réservés dans cette catégorie.

Si l’URL entrante correspond à une réservation mais pas à une inscription, l’API du serveur HTTP fait échouer la requête. Cela empêche les inscriptions de faible priorité d’être en mesure de récupérer les demandes qui ne sont pas prévues pour elle. L’État en cas d’échec est 400 (« requête incorrecte ») au lieu de 503 (« service non disponible »), car un retour de 503 est parfois interprété par erreur par les passerelles d’équilibrage de charge, comme indiquant que le serveur a été surchargé.

Si une inscription correspondante est trouvée dans la catégorie, la demande est routée vers la file d’attente de demandes associée à cette inscription. La demande est toujours routée vers la file d’attente associée aux UrlPrefix les plus longues correspondantes dans une catégorie.

Si aucune correspondance n’est trouvée dans la catégorie, l’API du serveur HTTP passe à la catégorie explicite et répète la même procédure. Pour résumer, l’ordre dans lequel les catégories sont examinées est le suivant :

1.  Caractère générique fort
2.  Explicite
3.  Caractère générique IP-Bound faible
4.  Caractère générique faible

Si aucune correspondance n’est trouvée dans l’une des catégories, l’API du serveur HTTP envoie une réponse avec un code d’état de 400 pour indiquer que la demande ne peut pas être routée.

## <a name="longest-match-rule"></a>Règle de correspondance la plus longue

Dans chaque catégorie UrlPrefix, l’API du serveur HTTP achemine une requête vers la file d’attente associée au UrlPrefix correspondant le plus long. Par exemple, supposons que les deux UrlPrefixes suivants sont inscrits dans différentes files d’attente :

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

L’API du serveur HTTP achemine une requête pour `https://www.adatum.com:80/default.htm` à attente queue1 et une demande `https://www.adatum.com:80/dir/sna/snadefault.htm` à Queue2. Il achemine une requête pour `https://www.adatum.com:80/dir/app.htm` à attente queue1, car la correspondance la plus longue est avec `https://www.adatum.com:80/` URLPrefix, et non avec `https://www.adatum.com:80/dir/sna` URLPrefix.

 

 




