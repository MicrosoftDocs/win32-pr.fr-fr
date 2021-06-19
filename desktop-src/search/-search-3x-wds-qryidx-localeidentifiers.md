---
description: Comprenez les arguments InputLocale et keywordlocale dans Windows Search, qui aide le moteur de recherche à utiliser les analyseurs lexicaux appropriés.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Arguments de l’identificateur de paramètres régionaux (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403752"
---
# <a name="locale-identifier-arguments-windows-search"></a>Arguments de l’identificateur de paramètres régionaux (Windows Search)

Les `inputlocale` `keywordlocale` identificateurs et aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée. Ce ne sont pas toujours les mêmes identificateurs de code de langue (LCID), car la recherche Windows est proposée dans plusieurs versions internationales et comprend également des packs MUI pour d’autres langues. La fonction InputLocale identifie le LCID pour le langage que les utilisateurs saisissent dans la requête de recherche, tandis que le keywordlocale identifie le LCID que le moteur de recherche utilise pour les mots clés.

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

 

 



