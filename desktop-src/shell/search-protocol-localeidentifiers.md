---
description: Les identificateurs InputLocale et keywordlocale aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée.
title: Arguments de l’identificateur de paramètres régionaux (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210309"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a>Arguments de l’identificateur de paramètres régionaux (shell Windows)

Les `inputlocale` `keywordlocale` identificateurs et aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée. Ce ne sont pas toujours les mêmes identificateurs de code de langue (LCID), car la recherche Windows est proposée dans plusieurs versions internationales et comprend également des packs d’interface utilisateur multilingue (MUI) pour d’autres langues. `inputlocale`Identifie le LCID pour les utilisateurs du langage entrant leur requête de recherche dans, tandis que le `keywordlocale` identifie le LCID que le moteur de recherche utilise pour les mots clés.

## <a name="example"></a>Exemple


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a>Informations sur les arguments



|                          |                                         |
|--------------------------|-----------------------------------------|
| Système d’exploitation minimal | Windows Vista Service Pack 1 (SP1) |



 

 

 



