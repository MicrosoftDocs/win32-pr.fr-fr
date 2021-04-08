---
description: Les identificateurs InputLocale et keywordlocale aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Arguments de l’identificateur de paramètres régionaux (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862181"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="73eb8-103">Arguments de l’identificateur de paramètres régionaux (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="73eb8-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="73eb8-104">Les `inputlocale` `keywordlocale` identificateurs et aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée.</span><span class="sxs-lookup"><span data-stu-id="73eb8-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="73eb8-105">Ce ne sont pas toujours les mêmes identificateurs de code de langue (LCID), car la recherche Windows est proposée dans plusieurs versions internationales et comprend également des packs MUI pour d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="73eb8-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="73eb8-106">La fonction InputLocale identifie le LCID pour le langage que les utilisateurs saisissent dans la requête de recherche, tandis que le keywordlocale identifie le LCID que le moteur de recherche utilise pour les mots clés.</span><span class="sxs-lookup"><span data-stu-id="73eb8-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="73eb8-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="73eb8-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="73eb8-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="73eb8-108">Example</span></span>](#example)
-   [<span data-ttu-id="73eb8-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73eb8-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="73eb8-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="73eb8-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="73eb8-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="73eb8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73eb8-112">Prise en main avec des arguments Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="73eb8-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="73eb8-113">Argument de navigation</span><span class="sxs-lookup"><span data-stu-id="73eb8-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="73eb8-114">Argument de syntaxe</span><span class="sxs-lookup"><span data-stu-id="73eb8-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="73eb8-115">Argument STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="73eb8-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="73eb8-116">Argument de sous-requête</span><span class="sxs-lookup"><span data-stu-id="73eb8-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



