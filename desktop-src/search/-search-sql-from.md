---
description: À la suite de l’instruction SELECT, vous utilisez la clause FROM pour spécifier l’emplacement où rechercher les documents correspondants.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM, clause
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517459"
---
# <a name="from-clause"></a><span data-ttu-id="e6f88-103">FROM, clause</span><span class="sxs-lookup"><span data-stu-id="e6f88-103">FROM Clause</span></span>

<span data-ttu-id="e6f88-104">À la suite de l’instruction SELECT, vous utilisez la clause FROM pour spécifier l’emplacement où rechercher les documents correspondants.</span><span class="sxs-lookup"><span data-stu-id="e6f88-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="e6f88-105">La syntaxe de la clause FROM pour une requête locale est la suivante :</span><span class="sxs-lookup"><span data-stu-id="e6f88-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="e6f88-106">Actuellement, Windows Search ne prend en charge qu’un seul catalogue, SystemIndex.</span><span class="sxs-lookup"><span data-stu-id="e6f88-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="e6f88-107">Pour interroger le catalogue local d’un ordinateur distant, incluez le nom de l’ordinateur avant le catalogue et un chemin d’accès UNC (Universal Naming Convention) sur l’ordinateur distant dans la clause SCOPE ou DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="e6f88-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="e6f88-108">Vous spécifiez une étendue en tant que restriction dans la clause WHERE, comme décrit dans la rubrique relative aux [prédicats d’étendue et de répertoire](-search-sql-folderdepth.md) .</span><span class="sxs-lookup"><span data-stu-id="e6f88-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="e6f88-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="e6f88-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="e6f88-110">Dans le second des exemples précédents, la requête cible un ordinateur distant appelé « zarascomputer ».</span><span class="sxs-lookup"><span data-stu-id="e6f88-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="e6f88-111">Notez que ce nom d’ordinateur apparaît dans les clauses FROM et SCOPE.</span><span class="sxs-lookup"><span data-stu-id="e6f88-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="e6f88-112">Dans le troisième exemple, la requête cible un nom de partage « Users » sur un serveur nommé « Server » (où le chemin d’accès UNC est le \\ \\ serveur \\ users).</span><span class="sxs-lookup"><span data-stu-id="e6f88-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6f88-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e6f88-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e6f88-114">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="e6f88-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6f88-115">Vue d’ensemble de la syntaxe de recherche SQL</span><span class="sxs-lookup"><span data-stu-id="e6f88-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="e6f88-116">Instruction SELECT</span><span class="sxs-lookup"><span data-stu-id="e6f88-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="e6f88-117">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="e6f88-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="e6f88-118">Prédicats d’étendue et de répertoire</span><span class="sxs-lookup"><span data-stu-id="e6f88-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



