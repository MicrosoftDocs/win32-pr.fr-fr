---
description: Windows Search fournit des fonctionnalités d’analyse de contenu et de recherche qui prennent en charge la recherche en texte intégral. Le langage de requête utilisé par Windows Search étend la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Interrogation de l’index avec la syntaxe SQL de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484409"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a><span data-ttu-id="a706a-104">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="a706a-104">Querying the Index with Windows Search SQL Syntax</span></span>

<span data-ttu-id="a706a-105">Windows Search fournit des fonctionnalités d’analyse de contenu et de recherche qui prennent en charge la recherche en texte intégral.</span><span class="sxs-lookup"><span data-stu-id="a706a-105">Windows Search provides content crawling and search features that support full-text searching.</span></span> <span data-ttu-id="a706a-106">Le langage de requête utilisé par Windows Search étend la syntaxe de requête de base de données SQL-92 et SQL-99 standard pour améliorer son utilité avec les recherches textuelles.</span><span class="sxs-lookup"><span data-stu-id="a706a-106">The query language used by Windows Search extends the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span>

<span data-ttu-id="a706a-107">Toutes les fonctionnalités de la langage SQL de recherche Windows (SQL) sont compatibles avec Windows Search sur Windows Vista et versions ultérieures, y compris toutes les versions de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a706a-107">All features of Windows Search Structured Query Language (SQL) are compatible with Windows Search on Windows Vista, and later, including all versions of Windows 10.</span></span>

<span data-ttu-id="a706a-108">Cette section fournit une vue d’ensemble de la syntaxe SQL dans Windows Search et inclut les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a706a-108">This section provides an overview of SQL syntax in Windows Search, and includes the following topics:</span></span>

- [<span data-ttu-id="a706a-109">Vue d’ensemble de la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="a706a-109">Overview of Windows Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
- [<span data-ttu-id="a706a-110">Informations générales sur le langage de requête</span><span class="sxs-lookup"><span data-stu-id="a706a-110">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)
- [<span data-ttu-id="a706a-111">REGROUPER... ... Gestion</span><span class="sxs-lookup"><span data-stu-id="a706a-111">GROUP ON ... OVER... Statement</span></span>](-search-sql-group-on-over.md)
- [<span data-ttu-id="a706a-112">Instruction SELECT</span><span class="sxs-lookup"><span data-stu-id="a706a-112">SELECT Statement</span></span>](-search-sql-select.md)
- [<span data-ttu-id="a706a-113">FROM, clause</span><span class="sxs-lookup"><span data-stu-id="a706a-113">FROM Clause</span></span>](-search-sql-from.md)
- [<span data-ttu-id="a706a-114">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="a706a-114">WHERE Clause</span></span>](-search-sql-where.md)
- [<span data-ttu-id="a706a-115">Clause ORDER BY</span><span class="sxs-lookup"><span data-stu-id="a706a-115">ORDER BY Clause</span></span>](-search-sql-orderby.md)
- [<span data-ttu-id="a706a-116">RANK BY, clause</span><span class="sxs-lookup"><span data-stu-id="a706a-116">RANK BY Clause</span></span>](-search-sql-rankby.md)
- [<span data-ttu-id="a706a-117">Instruction SET</span><span class="sxs-lookup"><span data-stu-id="a706a-117">SET Statement</span></span>](-search-sql-set.md)
- [<span data-ttu-id="a706a-118">Propriétés du rowset</span><span class="sxs-lookup"><span data-stu-id="a706a-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)

<span data-ttu-id="a706a-119">Cette documentation suppose que vous êtes familiarisé avec la fonction de liaison et d’incorporation d’objets (OLE DB) et SQL.</span><span class="sxs-lookup"><span data-stu-id="a706a-119">This documentation assumes familiarity with Object Linking and Embedding Database (OLE DB), and SQL.</span></span>

## <a name="code-samples"></a><span data-ttu-id="a706a-120">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="a706a-120">Code samples</span></span>

<span data-ttu-id="a706a-121">L’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via SQL.</span><span class="sxs-lookup"><span data-stu-id="a706a-121">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="a706a-122">L’exemple de code WSOleDB illustre Active Template Library (ATL) OLE DB l’accès aux applications Windows Search et deux méthodes supplémentaires pour récupérer les résultats de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="a706a-122">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="a706a-123">Les deux exemples sont disponibles dans les [exemples Windows Search](-search-samples-ovw.md) et le [Kit de développement logiciel (SDK) Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="a706a-123">Both samples are available in the [Windows Search Samples](-search-samples-ovw.md) and the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a706a-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a706a-124">Related topics</span></span>

[<span data-ttu-id="a706a-125">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="a706a-125">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="a706a-126">Utilisation des approches SQL et AQS pour interroger l’index</span><span class="sxs-lookup"><span data-stu-id="a706a-126">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)

[<span data-ttu-id="a706a-127">Interrogation de l’index avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="a706a-127">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)

[<span data-ttu-id="a706a-128">Interrogation de l’index avec le protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="a706a-128">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)

[<span data-ttu-id="a706a-129">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="a706a-129">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="a706a-130">Utilisation de la syntaxe de requête avancée par programmation</span><span class="sxs-lookup"><span data-stu-id="a706a-130">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
