---
description: 'Windows Les fonctions d’API qui manipulent des caractères sont généralement implémentées dans l’un des trois formats suivants :'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode dans l'API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c36e1e292eddd786d4c4bf336f980486f66870deb809587f9c51334f269ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764809"
---
# <a name="unicode-in-the-windows-api"></a>Unicode dans l'API Windows

Windows Les fonctions d’API qui manipulent des caractères sont généralement implémentées dans l’un des trois formats suivants :

-   une version générique qui peut être compilée pour Windows pages de codes ou Unicode
-   une [Windows](code-pages.md) version de page de codes avec la lettre « A » utilisée pour indiquer « ANSI »
-   Une version [Unicode](unicode.md) avec la lettre « W » utilisée pour indiquer « grande »

Certaines fonctions plus récentes prennent uniquement en charge les versions Unicode. Pour plus d’informations, consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).

Les rubriques suivantes traitent des types de données Unicode et de la façon dont ils sont utilisés dans les fonctions et les messages ; l’utilisation des ressources, des noms de fichiers et des arguments de ligne de commande ; et méthodes de conversion entre différents types de chaînes.

-   [Traduction automatique des messages](automatic-message-translation.md)
-   [Jeux de caractères utilisés dans les noms de fichiers](character-sets-used-in-file-names.md)
-   [Arguments de ligne de commande](command-line-arguments.md)
-   [Conventions pour les prototypes de fonctions](conventions-for-function-prototypes.md)
-   [Fonctions C standard](standard-c-functions.md)
-   [Différences de fonction de chaîne](string-function-differences.md)
-   [Conversion entre types chaîne](translation-between-string-types.md)
-   [Types de données Windows pour les chaînes](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos d’Unicode et des jeux de caractères](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



