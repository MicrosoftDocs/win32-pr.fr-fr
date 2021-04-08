---
description: La recherche-protocole d’application MS est une convention d’interrogation de l’index de recherche Windows.
ms.assetid: ab2695ed-4ef3-4687-81b0-416ca7086e5f
title: Interrogation de l’index avec le protocole search-ms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d835b6db1c9b05b97d5d075b62158069d89029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750420"
---
# <a name="querying-the-index-with-the-search-ms-protocol"></a><span data-ttu-id="e7852-103">Interrogation de l’index avec le protocole search-ms</span><span class="sxs-lookup"><span data-stu-id="e7852-103">Querying the Index with the search-ms Protocol</span></span>

<span data-ttu-id="e7852-104">La **recherche-**  [protocole d’application](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) MS est une convention d’interrogation de l’index de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="e7852-104">The **search-ms**  [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for querying the Windows Search index.</span></span> <span data-ttu-id="e7852-105">Le protocole permet aux applications, telles que l’Explorateur Windows, d’interroger l’index avec des arguments de valeur de paramètre, notamment des arguments de propriété, des recherches précédemment enregistrées, une syntaxe de requête avancée (AQS), une syntaxe de requête naturelle (NQS) et des identificateurs de code de langue (LCID) pour l’indexeur et la requête elle-même.</span><span class="sxs-lookup"><span data-stu-id="e7852-105">The protocol enables applications, like Windows Explorer, to query the index with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="e7852-106">Cette section est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="e7852-106">This section is organized as follows:</span></span>

-   [<span data-ttu-id="e7852-107">Prise en main avec des arguments Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="e7852-107">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
-   [<span data-ttu-id="e7852-108">Arguments de l’identificateur de paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="e7852-108">Locale Identifier Arguments</span></span>](-search-3x-wds-qryidx-localeidentifiers.md)
-   [<span data-ttu-id="e7852-109">Argument de navigation</span><span class="sxs-lookup"><span data-stu-id="e7852-109">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
-   [<span data-ttu-id="e7852-110">Argument de syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7852-110">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
-   [<span data-ttu-id="e7852-111">Argument STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="e7852-111">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
-   [<span data-ttu-id="e7852-112">Argument de sous-requête</span><span class="sxs-lookup"><span data-stu-id="e7852-112">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)

## <a name="related-topics"></a><span data-ttu-id="e7852-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7852-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7852-114">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="e7852-114">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e7852-115">Utilisation des approches SQL et AQS pour interroger l’index</span><span class="sxs-lookup"><span data-stu-id="e7852-115">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="e7852-116">Interrogation de l’index avec ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="e7852-116">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="e7852-117">Interrogation de l’index avec la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="e7852-117">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="e7852-118">Utilisation de la syntaxe de requête avancée par programmation</span><span class="sxs-lookup"><span data-stu-id="e7852-118">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 
