---
description: En savoir plus sur l’argument de sous-requête dans Windows Search. Une sous-requête est un fichier de recherche enregistré que vous pouvez utiliser comme filtre pour une nouvelle requête.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Argument de sous-requête (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011032"
---
# <a name="subquery-argument-windows-search"></a><span data-ttu-id="da807-104">Argument de sous-requête (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="da807-104">SUBQUERY Argument (Windows Search)</span></span>

<span data-ttu-id="da807-105">Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="da807-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="da807-106">Les résultats de la sous-requête sont utilisés comme source pour la nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="da807-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="da807-107">Par exemple, imaginons que vous ayez plusieurs fichiers de recherche enregistrés qui limitent une requête par liste de distribution de courrier électronique : myDepartment. search-ms, TeamProject. search-ms et corporatewide. search-ms.</span><span class="sxs-lookup"><span data-stu-id="da807-107">For example, let's say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="da807-108">L’utilisation de l' `subquery` argument vous permet de limiter les recherches par courrier électronique à tout ou partie de ces recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="da807-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

<span data-ttu-id="da807-109">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="da807-109">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="da807-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="da807-110">Example</span></span>](#example)
-   [<span data-ttu-id="da807-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da807-111">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="da807-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="da807-112">Example</span></span>


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a><span data-ttu-id="da807-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da807-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da807-114">Prise en main avec des arguments Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="da807-114">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="da807-115">Arguments de l’identificateur de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="da807-115">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[<span data-ttu-id="da807-116">Argument de navigation</span><span class="sxs-lookup"><span data-stu-id="da807-116">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="da807-117">Argument de syntaxe</span><span class="sxs-lookup"><span data-stu-id="da807-117">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="da807-118">Argument STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="da807-118">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



