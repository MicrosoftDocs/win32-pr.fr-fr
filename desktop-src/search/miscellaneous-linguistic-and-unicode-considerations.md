---
description: Cette rubrique décrit les éléments à prendre en compte pour les langages agglutinantes et les paires de substitution Unicode, et pour l’utilisation de paires de substitution pour étendre le jeu de caractères Unicode en fonction de jeux de caractères différents.
ms.assetid: 7104b2da-2ece-46ce-b4ca-6c24dc4d6677
title: Considérations linguistiques et Unicode diverses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433fb212917f29acbc2347c3324668a77533dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033874"
---
# <a name="miscellaneous-linguistic-and-unicode-considerations"></a>Considérations linguistiques et Unicode diverses

Cette rubrique décrit les éléments à prendre en compte pour les langages agglutinantes et les paires de substitution Unicode, et pour l’utilisation de paires de substitution pour étendre le jeu de caractères Unicode en fonction de jeux de caractères différents. Cette rubrique décrit également comment les analyseurs lexicaux identifient les expressions dans le texte et gèrent les espaces insécables, et comment les analyseurs lexicaux et les générateurs de formes dérivées gèrent les nombres et les dates, les mots composés, les expressions composées, les mots et les caractères spéciaux, les acronymes et les abréviations, ainsi que la mise en majuscules.

Cette rubrique est organisée comme suit :

-   [Identification de l’expression](#phrase-identification)
-   [Langues agglutinantes](#agglutinative-languages)
-   [Nombres, heures et dates](#numbers-times-and-dates)
-   [Mots composés](#compound-words)
-   [Expressions composées](#compound-phrases)
-   [Caractères spéciaux et mots](#special-characters-and-words)
-   [Acronymes et abréviations](#acronyms-and-abbreviations)
-   [Mise en majuscules](#capitalization)
-   [Espaces insécables](#nonbreaking-spaces)
-   [Paires de substitution](#surrogate-pairs)

## <a name="phrase-identification"></a>Identification de l’expression

Les expressions sont un mot ou un groupe de mots qui sont modifiés par un ou plusieurs autres. Les expressions sont difficiles à identifier de manière cohérente, car le même modificateur peut être utilisé dans plusieurs expressions avec le même nom. Par exemple, « nouvelle maison », « maison du Parlement », « nouveau bâtiment du Parlement ».

Windows Search utilise les expressions le plus souvent au moment de la requête. Les expressions contenues dans le texte de la requête reçoivent un poids supérieur à celui des mots individuels. Dans l’exemple précédent, un document contenant « House of Parlement » est classé plus haut qu’un document contenant « House » et « Parlement » à des points différents dans le document. Nous recommandons que les analyseurs lexicaux génèrent une expression au moment de la requête si l’expression est susceptible de correspondre à au moins un document.

## <a name="agglutinative-languages"></a>Langues agglutinantes

Les langages agglutinantes font la combinaison de plus petits morphèmes pour exprimer des idées composées. Chacun de ces morphèmes a généralement une signification ou une fonction et conserve sa forme d’origine et sa signification pendant le processus de combinaison. Pour les langues qui ont une morphologie agglutinantes, comme le turc, le finnois, le hongrois ou le coréen, il est possible de produire des milliers de formulaires pour un mot racine donné.

Le tableau suivant présente une liste de formes fléchies pour le mot « Talo » en finnois (« House »).



| Word      | Traduction   |
|-----------|---------------|
| Talo      | Placés         |
| Taloni    | Ma maison      |
| Talossa   | Dans la maison  |
| Talossani | Dans ma maison   |
| Taloja    | Accueille        |
| Taloissa  | Dans les maisons |



 

Les langues fléchies, telles que l’anglais, le français et le latin, comportent un très petit nombre de formes Word possibles pour un mot racine. Dans les langages fléchis, morphèmes influencent l’un l’autre lors de la liaison. La plupart des modifications apportées à l’inflexion sont présentes dans la tige ou le mot se terminant. Contrairement aux langages agglutinantes, les langages fléchis ont tendance à avoir des fonctions différentes pour un seul morpheme. Par exemple, un morpheme peut déterminer le nombre et la casse.

Les générateurs de formes dérivées pour les langages agglutinantes doivent peser le compromis entre performances et précision pour générer uniquement un sous-ensemble du nombre de formulaires Word possibles.

## <a name="numbers-times-and-dates"></a>Nombres, heures et dates

Les analyseurs lexicaux doivent utiliser un format commun pour représenter des nombres, des heures et des dates pour faciliter les requêtes cohérentes.

Lorsque vous créez un analyseur lexical, nous vous recommandons d’utiliser l’analyseur lexical pour normaliser les nombres dans une représentation canonique à l’aide du modèle « NN *DD* D *CC*», où nn est la séquence littérale « NN », *DD* est la partie entière du nombre, d est le littéral « d », et *CC* est la partie fractionnaire du nombre. Les analyseurs lexicaux ne limitent pas le nombre de chiffres pour l’entier ou la partie fractionnaire du nombre. Nous recommandons que les analyseurs lexicaux reconnaissent les modèles numériques délimités par les points (.) et les virgules (,). Par exemple, Windows Search représente à la fois « 1 000,2 » et « 1.000, 2 » en tant que « NN1000D2 ».

Choisissez un format pour les analyseurs lexicaux et les générateurs de formes dérivées. Les chiffres arabes sur un octet sont normalisés de telle sorte qu’une requête contenant l’une de ces formes corresponde à des documents avec les autres formulaires.

Lorsque vous créez un analyseur lexical, nous vous recommandons d’utiliser l’analyseur lexical toutes les occurrences sous la forme d’une représentation de 24 heures à l’aide du modèle « TT *HHMMSS*», où TT est le préfixe LITTÉRAL « TT », *hh* est heures, *mm* est le nombre de minutes et *SS* est le nombre de secondes. Windows Search ne correspond pas aux unités de temps supplémentaires, telles que les millisecondes. Analyse du matin et P.M Patterns est facultatif.

Lorsque vous créez un analyseur lexical, nous recommandons que l’analyseur lexical génère des dates au format canonique « JJ *AAAAMMJJ*», où JJ est le LITTÉRAL « JJ », *yyyy* les années, *mm* les mois et *JJ* les jours. Nous recommandons également que les analyseurs lexicaux stockent des années à deux chiffres dans les formats du vingtième siècle et du vingt-et-un-siècle. Par exemple, les analyseurs lexicaux représentent « 2.2.99 » en tant que « DD19990202 » et « DD20990202 ». Au moment de la requête, Windows Search dérive la date en utilisant les interfaces de programmation d’applications (API) de Windows pour déterminer la date de découpe du serveur afin d’afficher le format correct, 19 *XX* ou 20 *XX*.

## <a name="compound-words"></a>Mots composés

Dans certains langages, tels que l’allemand, les noms sont composés de noms plus simples. Ces noms composés sont trop spécifiques en ce sens pour un rappel de requête raisonnable. Par exemple, sans décomposition, une requête pour « Versicherung » (« Insurance ») ne correspond pas à « Lebensversicherungsgesellschaft » (« Life-Insurance Sales »). Dans ce cas, nous recommandons que les analyseurs lexicaux décomposent ces mots composés en composants de base pendant la création de l’index et la durée de la requête. L’analyseur lexical allemand divise « Lebensversicherungsgesellschaft » en mots de composants « Leben », « Versicherung » et « Gesellschaft ». Elle applique la même décomposition au moment de la requête, ainsi qu’une recherche de radical facultative pour chacun des termes résultants.

## <a name="compound-phrases"></a>Expressions composées

Certains langages, tels que le coréen, contiennent des expressions complexes qui peuvent être décomposées de plusieurs façons. Une expression coréenne est constituée de *mots de contenu*, tels que des noms, des pronoms, des verbes et des adjectifs, suivis de *mots fonctionnels*. Les mots fonctionnels se trouvent dans après les positions et les fins. Les positions postérieures indiquent le rôle fonctionnel du substantif ou du pronom dans une phrase ; les fins indiquent le rôle fonctionnel du verbe ou de l’adjectif.

Une expression peut avoir plusieurs analyses, et chaque analyse peut comporter plusieurs mots de contenu. L’analyseur lexical doit utiliser des heuristiques spécifiques à la langue pour déterminer, du contexte, le poids à attribuer à différentes analyses. L’analyseur lexical peut déterminer quelle décomposition utiliser en fonction du nombre de mots de composants résultants. Certains analyseurs lexicaux peuvent privilégier les courtes séquences de termes plus longs, tandis que les autres analyseurs lexicaux peuvent préférer de longues séquences de mots plus petits.

Un autre point à prendre en compte est que, en coréen, les noms et les pronoms peuvent être stockés dans l’index sans les mots fonctionnels correspondants. Le coréen est un langage agglutinantes qui combine de nombreuses fins de mot avec des verbes et des adjectifs pour former des formes fléchies sans nombre. Les verbes et les adjectifs identifiés dans les expressions sont enregistrés avec leurs terminaisons dans l’index, mais l’analyseur lexical ne génère pas de nouveaux formulaires.

## <a name="special-characters-and-words"></a>Caractères spéciaux et mots

Les caractères spéciaux sont des caractères tels que « », «© » et « ™ ». Ces caractères sont rarement utilisés dans les requêtes. Les analyseurs lexicaux doivent supprimer les caractères spéciaux lors de la création de l’index et au moment de la requête.

Nous recommandons que les analyseurs lexicaux reconnaissent les mots spéciaux, tels que « C++ », « C », « \# .net », « qualités » et « notation musicale ». Les analyseurs lexicaux peuvent utiliser une heuristique de langage pour identifier un motif pour des mots spéciaux. Les analyseurs lexicaux peuvent également utiliser un dictionnaire personnalisé qui contient des mots spéciaux reconnus.

## <a name="acronyms-and-abbreviations"></a>Acronymes et abréviations

Les acronymes et les abréviations doivent être pris en compte lors de l’implémentation d’un analyseur lexical. Dans de nombreux langages, les lettres d’acronymes individuelles sont séparées par des points. Parfois, les mots qui ne sont pas des acronymes ou des abréviations reconnus sont abrégés. Par exemple, « États-Unis de l’Amérique » peut être abrégé en « USA » ou « États-Unis » Les analyseurs lexicaux inclus avec Windows Search identifient généralement les mots à lettres uniques comme des mots parasites et traitent ces mots comme des espaces réservés au moment de la requête. Pendant la durée de la requête, un analyseur lexical qui ne tient pas compte des acronymes courants ou qui ne reconnaît pas les abréviations, convertit l’abréviation « U.S.A. ». en « U », « S » et « A ». Cette décomposition ne fournit pas suffisamment d’informations pour faire correspondre les mots de l’index de recherche en texte intégral, car tous les termes de la requête sont des mots parasites. Lorsque vous créez un analyseur lexical, nous recommandons que l’analyseur lexical supprime les points qui séparent les lettres d’acronymes. Dans l’exemple, « États-Unis » est stocké sous la forme « USA » et un terme de requête contenant « États-Unis » Interrogez en fait les « USA ». Si un analyseur lexical traite une abréviation, le point de cette abréviation n’est pas traité comme une rupture EOS. Pour cette raison, un analyseur lexical peut ne pas identifier correctement une rupture EOS si l’abréviation se trouve à la fin de la phrase.

## <a name="capitalization"></a>Mise en majuscules

Windows Search ne préserve pas actuellement la casse lorsqu’il enregistre des mots dans l’index de recherche en texte intégral. Les analyseurs lexicaux et les générateurs de formes dérivées ne doivent pas modifier la casse des mots.

## <a name="nonbreaking-spaces"></a>Espaces insécables

Lorsque vous créez un analyseur lexical, nous vous recommandons de vous assurer que l’analyseur lexical traite les espaces insécables comme des séparateurs de mots. Il est également recommandé que l’analyseur lexical génère d’autres formes du mot, avec et sans espaces insécables. Certains caractères, tels que les traits de soulignement, sont des caractères spéciaux qui sont traités comme des caractères insécables en raison des sources du texte dans lequel elles se trouvent. Par exemple, le code source ou les noms de fichiers peuvent inclure des traits de soulignement comme des caractères insécables.

## <a name="surrogate-pairs"></a>Paires de substitution

Les paires de substitution sont des représentations de caractères dans le code source qui représentent un caractère unique qui se compose d’une séquence de deux valeurs Unicode. Dans une paire codée, la première valeur est un substitut étendu et la seconde est un caractère de substitution faible. Un substitut étendu est un caractère compris entre U + D800 et U + DBFF. Un substitut faible est un caractère de la plage U + DC00 et à U + DFFF. Les paires de substitution étendent le jeu de caractères au-delà du caractère Unicode. Il est recommandé qu’un analyseur lexical utilise les règles suivantes lors de la gestion des paires de substitution :

-   Un substitut étendu doit précéder un caractère de substitution faible.
-   Un substitut faible doit suivre un caractère de substitution étendu.
-   Un substitut haute ou faible sans valeur correspondante pour l’autre moitié n’a aucune signification.

Les analyseurs lexicaux doivent prendre en compte toutes les paires et générer les paires comme tel dans l’index. Pour plus d’informations, consultez [substituts et caractères supplémentaires](/windows/desktop/Intl/surrogates-and-supplementary-characters).

 

 
