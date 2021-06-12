---
description: En savoir plus sur l’argument de sous-requête dans le shell Windows. Une sous-requête est un fichier de recherche enregistré que vous pouvez utiliser comme filtre pour une nouvelle requête.
title: Argument de sous-requête (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ef0b37c0f473f2b86c85c18a99124be3b366f447
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010662"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="389c7-104">Argument de sous-requête (shell Windows)</span><span class="sxs-lookup"><span data-stu-id="389c7-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="389c7-105">Une sous-requête est un fichier de recherche enregistré ( \* . search-ms) que vous pouvez utiliser comme filtre pour une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="389c7-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="389c7-106">Les résultats de la sous-requête sont utilisés comme source pour la nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="389c7-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="389c7-107">Par exemple, imaginons que vous ayez plusieurs fichiers de recherche enregistrés qui limitent une requête par liste de distribution de courrier électronique : myDepartment. search-ms, TeamProject. search-ms et corporatewide. search-ms.</span><span class="sxs-lookup"><span data-stu-id="389c7-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="389c7-108">L’utilisation de l' `subquery` argument vous permet de limiter les recherches par courrier électronique à tout ou partie de ces recherches enregistrées.</span><span class="sxs-lookup"><span data-stu-id="389c7-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="389c7-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="389c7-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="389c7-110">Informations sur les arguments</span><span class="sxs-lookup"><span data-stu-id="389c7-110">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="389c7-111">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="389c7-111">Minimum Operating System</span></span> | <span data-ttu-id="389c7-112">Windows Vista Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="389c7-112">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



