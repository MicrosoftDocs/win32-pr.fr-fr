---
description: Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argument de sous-requête (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951033"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="ff06f-103">Argument de sous-requête (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="ff06f-103">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="ff06f-104">Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="ff06f-104">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="ff06f-105">Les résultats de la sous-requête sont utilisés comme source pour la nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="ff06f-105">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="ff06f-106">Par exemple, imaginons que vous ayez plusieurs fichiers de recherche enregistrés qui limitent une requête par liste de distribution de courrier électronique : myDepartment. search-ms, TeamProject. search-ms et corporatewide. search-ms.</span><span class="sxs-lookup"><span data-stu-id="ff06f-106">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="ff06f-107">L’utilisation de l' `subquery` argument vous permet de limiter les recherches par courrier électronique à tout ou partie de ces recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="ff06f-107">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="ff06f-108">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="ff06f-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="ff06f-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff06f-109">Example</span></span>](#example)
-   [<span data-ttu-id="ff06f-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff06f-110">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="ff06f-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="ff06f-111">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="ff06f-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff06f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff06f-113">Prise en main avec des arguments Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="ff06f-113">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="ff06f-114">Arguments de l’identificateur de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="ff06f-114">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="ff06f-115">Argument de navigation</span><span class="sxs-lookup"><span data-stu-id="ff06f-115">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="ff06f-116">Argument de syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff06f-116">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="ff06f-117">Argument STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="ff06f-117">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



