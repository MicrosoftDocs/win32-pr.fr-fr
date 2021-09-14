---
description: comprenez les arguments inputlocale et keywordlocale dans Windows recherche, qui aide le moteur de recherche à utiliser les analyseurs lexicaux appropriés.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Arguments de l’identificateur de paramètres régionaux (recherche Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231270"
---
# <a name="locale-identifier-arguments-windows-search"></a>Arguments de l’identificateur de paramètres régionaux (recherche Windows)

Les `inputlocale` `keywordlocale` identificateurs et aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée. il ne s’agit pas toujours des mêmes identificateurs de code de langue (lcid), car la recherche Windows est proposée dans plusieurs versions internationales et comprend également des packs MUI pour d’autres langues. La fonction InputLocale identifie le LCID pour le langage que les utilisateurs saisissent dans la requête de recherche, tandis que le keywordlocale identifie le LCID que le moteur de recherche utilise pour les mots clés.

Cette rubrique est organisée comme suit :

-   [Exemple](#example)
-   [Rubriques connexes](#related-topics)

## <a name="example"></a>Exemple


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec des arguments Parameter-Value](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Argument de navigation](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Argument de syntaxe](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Argument STACKEDBY](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[Argument de sous-requête](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



