---
description: Un &\# 0034 ; jeu de caractères&\# 0034 ; est un mappage de caractères avec leurs valeurs de code d’identification.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Character Sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240426"
---
# <a name="character-sets"></a>Character Sets

Un « jeu de caractères » est un mappage de caractères avec leurs valeurs de code d’identification. Le jeu de caractères le plus couramment utilisé dans les ordinateurs actuels est [Unicode](unicode.md), une norme globale pour l’encodage des caractères. en interne, les applications Windows utilisent l’implémentation UTF-16 d’Unicode. En UTF-16, la plupart des caractères sont identifiés par des codes à deux octets. Les caractères supplémentaires les moins communément utilisés sont représentés par une paire de substitution, qui est une paire de codes à deux octets. Pour plus d’informations, consultez [substituts et caractères supplémentaires](surrogates-and-supplementary-characters.md).

certaines applications Windows doivent fonctionner avec les jeux de caractères plus anciens qui sont natifs pour Windows Me/98/95. [Windows pages de codes](code-pages.md) permettent à votre application de travailler avec ces jeux de caractères. Ces jeux de caractères peuvent être divisés en :

-   [Jeux de caractères codés sur un octet](single-byte-character-sets.md) (SBCS). Dans un SBCS, chaque caractère est identifié par une valeur d’un octet en largeur.
-   Jeux de caractères multioctets, en particulier les [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS). Les jeux de caractères multioctets offrent un moyen de représenter le grand nombre de caractères dans de nombreuses langues asiatiques.

Pour plus d'informations, voir les rubriques suivantes :

-   [Pages de codes](code-pages.md)
-   [Jeux de caractères codés sur deux octets](double-byte-character-sets.md)
-   [Jeux de caractères codés sur un octet](single-byte-character-sets.md)
-   [Substituts et caractères supplémentaires](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos d’Unicode et des jeux de caractères](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



