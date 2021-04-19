---
description: Le concept d’une adresse est essentiel pour la plupart des opérations de communication.
ms.assetid: 32fbd06b-f6f2-4024-b8d5-3d6eef16bca2
title: Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6ad8f03b725a58d564c63f4c5c0d0165eed99a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533978"
---
# <a name="address"></a>Adresse

Le concept d’une adresse est essentiel pour la plupart des opérations de communication. Une adresse représente un emplacement sur un réseau. L’attribution locale d’une adresse à une ligne ou à un canal a généralement lieu lors de l’installation du fournisseur de services, mais peut être modifiée ultérieurement. Vous trouverez plus d’informations sur les procédures impliquées dans le kit de ressources du système d’exploitation pour les fournisseurs de services fournis par Microsoft et dans la documentation du fournisseur de services pour les produits non-Microsoft.

Une seule adresse peut être partagée par plusieurs périphériques de ligne. Différents fournisseurs de commutateurs ont des noms différents pour ce concept, tels que le pontage d’adresses, le numéro de répertoire à plusieurs apparences (MADN) ou l’apparence de pont. Un appel entrant sur une adresse partagée est proposé sur toutes les lignes associées à l’adresse. Pour obtenir une description des configurations reconnues par TAPI, consultez [ \_ constantes LINEADDRESSSHARING](./lineaddresssharing--constants.md) .

L’adresse elle-même est une chaîne qui identifie un emplacement sur un réseau. Dans le cas d’un réseau téléphonique, l’adresse est un numéro de téléphone complet avec des codes nationaux ou internationaux. Si le réseau est basé sur IP, l’adresse peut être une adresse IP. Consultez [LINEADDRESSTYPE \_ constantes](lineaddresstype--constants.md) pour les types d’adresses définis par TAPI. Un fournisseur de services peut définir des types d’adresses supplémentaires.

## <a name="address-related-capabilities-and-messages"></a>Address-Related les fonctionnalités et les messages

Les différentes adresses possèdent des fonctionnalités, des fonctionnalités et des États différents. Les fournisseurs de services sont la source de ces informations. La fonctionnalité de requête d’appareil et les mécanismes d’État et de rapport d’événements de l’interface TAPI fournissent aux applications des informations pour gérer les adresses.

Les applications acquièrent ces informations en traitant les événements à partir de l’interface TAPI ou à l’aide d’opérations de requête. Cela permet à une application de prendre en compte des facteurs tels que le fait qu’une adresse donnée prenne en charge une fonctionnalité spécifique, telle que [Park](park-ovr.md).

**TAPI 2. x :** Les applications appellent la fonction [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) pour déterminer les fonctionnalités de téléphonie de chaque adresse, puis elles reçoivent ces informations dans une structure de données [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) . De la même façon, une application peut appeler [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) pour un périphérique de ligne pour déterminer le nombre d’adresses affectées à la ligne, ainsi que d’autres informations.

**TAPI 3. x :** Les applications utilisent les [interfaces d’objet Address](address-object-interfaces.md) pour obtenir des informations sur les fonctionnalités d’adresse et les événements.

## <a name="storing-phone-numbers-in-electronic-address-books"></a>Stockage des numéros de téléphone dans les carnets d’adresses électroniques

De nombreux utilisateurs choisissent de composer des personnes, des télécopieurs, des forums et d’autres entités en sélectionnant leurs noms dans un carnet d’adresses. Le nombre réel composé dépend de l’emplacement géographique de l’utilisateur et de la façon dont le périphérique de ligne à utiliser est connecté. Par exemple, un ordinateur de bureau peut avoir accès à deux lignes, une connectée à un PBX, l’autre au bureau central de l’entreprise. Lors d’un appel au même tiers, il peut être nécessaire d’utiliser des numéros différents. (Pour effectuer un appel via le PBX, par exemple, il se peut que l’ordinateur doive composer un préfixe « 9 » pour obtenir une ligne extérieure, ou un préfixe différent peut être nécessaire pour un appel effectué par le Bureau central.) Ou bien, un utilisateur peut effectuer des appels à partir d’un ordinateur portable et souhaiter utiliser un seul carnet d’adresses statique, même en cas d’appel à partir de différents emplacements ou environnements de téléphonie. Les fonctionnalités de traduction d’adresses de TAPI permettent à l’utilisateur d’informer l’ordinateur de l’emplacement actuel et de l’appareil de ligne souhaité pour l’appel. L’interface TAPI gère ensuite les différences de numérotation, en ne nécessitant aucune modification du carnet d’adresses de l’utilisateur. Une application utilise la [traduction d’adresses](initiate-a-session-ovr.md) pour convertir une adresse du format d' [adresse canonique](#canonical-addresses) au format d' [adresse de numérotation](#dialable-addresses) .

Une rubrique connexe est la gestion de la surveillance internationale des appels, qui est le processus d’écoute de tonalités audibles telles que la tonalité, les tonalités d’information spéciales, les signaux occupés et les tonalités de rappel pour déterminer l' *État* d’un appel (sa progression via le réseau). Étant donné que les cadences et les fréquences des tons de progression des appels varient d’un pays ou d’une région à l’état d’un pays ou d’une région, le fournisseur de services doit connaître la progression de l’appel à suivre lors de l’appel international sortant. Par conséquent, les applications spécifient le pays ou le code de région de destination lors du placement des appels sortants.

## <a name="canonical-addresses"></a>Adresses canoniques

Le format d’adresse canonique est destiné à être un numéro de répertoire universellement constant. Pour cette raison, les nombres figurant dans les carnets d’adresses sont mieux stockés à l’aide du format canonique.

Les détails suivants concernent ce qui est considéré comme canonique pour une adresse de téléphone.

Une adresse de téléphone canonique est une chaîne de texte avec la structure suivante :

\+*CountryCode* Espace \[ **(**_indicatif_*_)_* espace SubscriberNumber nom de la sous- \]  \| *adresse*  ^   CRLF...

Les composants de cette structure sont décrits dans le tableau suivant.



Composant

Signification

\+

Équivalent à hex 2B. Indique que le nombre qui suit utilise le format canonique.

*CountryCode*

Chaîne de taille variable contenant un ou plusieurs des chiffres « 0 » à « 9 » (nombre hexadécimal de 30 à 39 inclus). Le *CountryCode* est délimité par l’espace suivant. Il identifie le pays ou la région où se trouve l’adresse.

Espace

Exactement un caractère d’espace (20 Hex). Il est utilisé pour délimiter la fin de la partie *CountryCode* d’une adresse.

*Indicatif*

Chaîne de taille variable contenant zéro, un ou plusieurs des chiffres « 0 » à « 9 » (nombre hexadécimal de 30 à 39 inclus). L' *indicatif* régional est la partie indicatif de l’adresse et est facultatif. Si le code de zone est présent, il doit être précédé d’un caractère de parenthèse ouvrante (28) exactement et être suivi par exactement un caractère de parenthèse droite (29) et un espace (20).

*SubscriberNumber*

Chaîne de taille variable contenant un ou plusieurs des chiffres « 0 » à « 9 » (nombre hexadécimal de 30 à 39 inclus). Il peut également inclure d’autres caractères de mise en forme, y compris les caractères de contrôle de numérotation décrits dans le format d’adresse de numérotation :

 

Caractère

Encodage hexadécimal

 

! \#<br/> $<br/> \*<br/> ,<br/> ?<br/> @<br/> ABCD<br/> P<br/> T<br/> W<br/> abcd<br/> p<br/> t<br/> w<br/>

21 23<br/> 24<br/> 2A<br/> 2C<br/> 3F<br/> 40<br/> 41-44<br/> 50<br/> 54<br/> 77<br/> 61-64<br/> 70<br/> 74<br/> 79<br/>

 

Le numéro de l’abonné ne doit pas contenir la parenthèse ouvrante ou la parenthèse fermante (qui sont uniquement utilisés pour délimiter le code de zone), ni contenir les \| caractères "", "^" ou CRLF (qui sont utilisés pour commencer les champs suivants). Le plus souvent, les caractères non numériques du numéro d’abonné incluent uniquement les espaces, les points (« . ») et les tirets (« - »). Tous les caractères non numériques autorisés qui apparaissent dans le numéro de l’abonné sont omis de la *DialableString* retournée par la fonction [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) , mais sont conservés dans le *DisplayableString*.

\|

Hex (7C). Si ce caractère facultatif est présent, les informations qui le suivent jusqu’au suivant + \| ^ CRLF, ou la fin de la chaîne d’adresse canonique, sont traitées comme des informations de sous-adresse, comme pour une sous-adresse RNIS.

*Sous-adresse*

Chaîne de taille variable contenant une sous-adresse. La chaîne est délimitée par + \| ^ CRLF ou la fin de la chaîne d’adresse. Lors de la numérotation, les informations de sous-adresse sont transmises au tiers distant. Il peut s’agir d’une sous-adresse RNIS ou d’une adresse de messagerie.

^

Hex (5E). Si ce caractère facultatif est présent, les informations qui le suivent jusqu’au CRLF suivant ou la fin de la chaîne d’adresse canonique sont traitées comme un nom RNIS.

*Nom*

Chaîne de taille variable traitée comme des informations de nom. Name est délimité par CRLF ou la fin de la chaîne d’adresse canonique et peut contenir d’autres délimiteurs. Pendant la numérotation, les informations de nom sont transmises au tiers distant.

CRLF

Hex (0D) suivi de Hex (0A) et est facultatif. S’il est présent, il indique qu’un autre nombre canonique suit celui-ci. Il est utilisé pour séparer plusieurs adresses canoniques dans le cadre d’une seule chaîne d’adresse (multiplexage inverse). Par exemple, la représentation canonique du numéro de téléphone principal de Microsoft Corporation serait la suivante :<br/> + 1 (425) 882-8080<br/>



 

## <a name="dialable-addresses"></a>Adresses numérotables

Le format d’adresse de numérotation est le formulaire dans lequel une adresse est transmise à un fournisseur de services qui gère les numéros de téléphone. Les informations suivantes concernent les adresses numérotables sur un réseau téléphonique.

Le format du numéro de téléphone à distance permet de fournir plusieurs adresses de destination à la fois. Cette possibilité peut être utile si le fournisseur de services offre une forme de multiplexage inverse en configurant des appels à chacune des destinations spécifiées et en gérant ensuite le flux d’informations en tant que flux de données multimédia à bande passante unique. L’application perçoit ce groupe d’appels comme un appel unique, car elle reçoit uniquement un seul descripteur d’appel représentant l’agrégat des appels téléphoniques individuels.

Il est également possible de prendre en charge le multiplexage inverse au niveau de l’application. Pour ce faire, l’application configure une série d’appels individuels et synchronise leurs flux multimédias.

La sous- *adressage* est une fonctionnalité fournie sur les lignes RNIS qui permet d’obtenir plus d’informations qu’un simple numéro de téléphone à utiliser lors de la numérotation. Ces informations supplémentaires peuvent spécifier une extension téléphonique individuelle pour sonner ou, dans un environnement informatique, une application particulière à alerter. D’autres paramètres peuvent décrire les aspects requis d’une connexion demandée, tels que le taux et le minutage.

Si la sous-adresse est prise en charge par un fournisseur de services, l’application l’intègre à l’adresse passée à toute opération qui en requiert une.

Une adresse de téléphone numérotable contient des informations sur l’adressage des parties et fait partie de la navigation par nature. Toute chaîne d’entrée qui ne commence pas par un caractère « + » est supposée ne pas être au format canonique et, par conséquent, être dans un format d’adresse de numérotation, et est retournée à l’application comme étant inchangée. Une adresse de numérotation est une chaîne de texte avec la structure suivante :

*DialableNumber* \| Sous- *adresse*  ^  *Nom* CRLF...

Les composants de cette structure sont indiqués dans le tableau suivant.



| Composant        | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *DialableNumber* | Chiffres et modificateurs 0-9 A-D \* \# , ! W w P t t @ $ ? ; délimité par \| ^ CRLF ou la fin de la chaîne d’adresse de numérotation. Le signe plus (+) est un caractère valide dans les chaînes de numérotation. Elle indique que le numéro de téléphone est un numéro international complet. Dans le *DialableNumber*, notez les définitions suivantes :<br/> 0-9 A-D \*\#<br/> Caractères correspondant aux chiffres DTMF et/ou Pulse.<br/> |
| !                | Hex (21). Indique qu’un hookflash (une demi-seconde OnHook, suivi d’une demi-seconde offhook avant de continuer) doit être inséré dans la chaîne de numérotation.                                                                                                                                                                                                                                                                                   |
| P p              | Hex (50) ou Hex (70). Indique que la numérotation par impulsions doit être utilisée pour les chiffres qui la suivent.                                                                                                                                                                                                                                                                                                                                                |
| T t              | Hex (54) ou Hex (74). Indique que la numérotation tonale (DTMF) doit être utilisée pour les chiffres qui la suivent.                                                                                                                                                                                                                                                                                                                                          |
| ,                | Hex (27). Indique que la numérotation doit être suspendue. La durée d’une pause est spécifique à l’appareil et peut être récupérée à partir des fonctionnalités de l’appareil de la ligne. Plusieurs virgules peuvent être utilisées pour fournir des pauses plus longues.                                                                                                                                                                                                                                 |
| W w              | Hex (57) ou Hex (77). Un W majuscule ou minuscule indique que la numérotation doit se poursuivre uniquement après la détection d’une tonalité.                                                                                                                                                                                                                                                                                                            |
| @                | Hex (40). Indique que la numérotation consiste à « attendre une réponse calme » avant de composer le reste de l’adresse de numérotation. Cela signifie qu’il faut attendre au moins une tonalité de rappel, suivie de plusieurs secondes de silence.                                                                                                                                                                                                                               |
| $                | Hex (24). Indique que la numérotation des informations de facturation consiste à attendre un « signal de facturation » (par exemple, une tonalité de carte de crédit).                                                                                                                                                                                                                                                                                                              |
| ?                | Hex (3F). Indique que l’utilisateur doit être invité à confirmer la numérotation. Le fournisseur ne fait pas réellement l’invite, mais la présence de «  ? » oblige le fournisseur à rejeter la chaîne comme étant non valide, en avertissant l’application de la nécessité de la scinder en plusieurs parties et de demander à l’utilisateur de le décomposer.                                                                                                                           |
| ;                | Hex (3B). Si elle est placée à la fin d’une chaîne d’adresse numérotable partiellement spécifiée, elle indique que les informations de numéro de numérotation sont incomplètes et que d’autres informations d’adresse seront fournies ultérieurement. Le composant ";" est uniquement autorisé dans la partie *DialableNumber* d’une adresse.                                                                                                                                                       |
| \|               | Hex (7C) et est facultatif. S’il est présent, les informations qui le suivent jusqu’au prochain + \| ^ CRLF, ou la fin de la chaîne d’adresse de numérotation, sont traitées comme des informations de sous-adresse (comme pour une sous-adresse RNIS).                                                                                                                                                                                                                                  |
| *Sous-adresse*     | Chaîne de taille variable contenant une sous-adresse. La chaîne est délimitée par le suivant + \| ^ CRLF ou la fin de la chaîne d’adresse. Lors de la numérotation, les informations de sous-adresse sont transmises au tiers distant. Il peut s’agir d’une sous-adresse RNIS, d’une adresse de messagerie, etc.                                                                                                                                                                       |
| ^                | Hex (5E) et est facultatif. S’il est présent, les informations qui le suivent jusqu’au CRLF suivant ou la fin de la chaîne d’adresse à distance sont traitées comme un nom RNIS.                                                                                                                                                                                                                                                                                |
| *Nom*           | Chaîne de taille variable traitée comme des informations de nom. Le nom est délimité par CRLF ou la fin de la chaîne d’adresse de numérotation. Lors de la numérotation, les informations de nom sont transmises au tiers distant.                                                                                                                                                                                                                                                      |
| CRLF             | Hex (0D) suivi de Hex (0A). S’il est présent, ce caractère facultatif indique qu’un autre numéro de numérotation est à la suite de celui-ci. Il est utilisé pour séparer plusieurs adresses à numéroter dans le cadre d’une seule chaîne d’adresse (pour le multiplexage inverse).                                                                                                                                                                                           |



 

La traduction d’adresses peut être utilisée pour convertir une adresse de format canonique en format de numérotation.

 

