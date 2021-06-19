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
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="436df-103">Arguments de l’identificateur de paramètres régionaux (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="436df-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="436df-104">Les `inputlocale` `keywordlocale` identificateurs et aident le moteur de recherche à utiliser les analyseurs lexicaux appropriés en identifiant la langue des requêtes entrées par l’utilisateur et la langue des mots clés de syntaxe de requête avancée.</span><span class="sxs-lookup"><span data-stu-id="436df-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="436df-105">Ce ne sont pas toujours les mêmes identificateurs de code de langue (LCID), car la recherche Windows est proposée dans plusieurs versions internationales et comprend également des packs MUI pour d’autres langues.</span><span class="sxs-lookup"><span data-stu-id="436df-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="436df-106">La fonction InputLocale identifie le LCID pour le langage que les utilisateurs saisissent dans la requête de recherche, tandis que le keywordlocale identifie le LCID que le moteur de recherche utilise pour les mots clés.</span><span class="sxs-lookup"><span data-stu-id="436df-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="436df-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="436df-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="436df-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="436df-108">Example</span></span>](#example)
-   [<span data-ttu-id="436df-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="436df-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="436df-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="436df-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="436df-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="436df-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="436df-112">Prise en main avec des arguments Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="436df-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="436df-113">Argument de navigation</span><span class="sxs-lookup"><span data-stu-id="436df-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="436df-114">Argument de syntaxe</span><span class="sxs-lookup"><span data-stu-id="436df-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="436df-115">Argument STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="436df-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="436df-116">Argument de sous-requête</span><span class="sxs-lookup"><span data-stu-id="436df-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



