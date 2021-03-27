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
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="23205-103">Arguments de l’identificateur de paramètres régionaux (shell Windows)</span><span class="sxs-lookup"><span data-stu-id="23205-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="23205-104">Les `inputlocale` `keywordlocale` identificateurs et aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée.</span><span class="sxs-lookup"><span data-stu-id="23205-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="23205-105">Ce ne sont pas toujours les mêmes identificateurs de code de langue (LCID), car la recherche Windows est proposée dans plusieurs versions internationales et comprend également des packs d’interface utilisateur multilingue (MUI) pour d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="23205-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="23205-106">`inputlocale`Identifie le LCID pour les utilisateurs du langage entrant leur requête de recherche dans, tandis que le `keywordlocale` identifie le LCID que le moteur de recherche utilise pour les mots clés.</span><span class="sxs-lookup"><span data-stu-id="23205-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="23205-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="23205-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="23205-108">Informations sur les arguments</span><span class="sxs-lookup"><span data-stu-id="23205-108">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="23205-109">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="23205-109">Minimum Operating System</span></span> | <span data-ttu-id="23205-110">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="23205-110">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



