---
description: Découvrez comment Windows Search vous permet de gérer l’index de recherche Windows avec le gestionnaire de recherche, le gestionnaire de catalogues et le gestionnaire de portée d’analyse.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces pour la gestion de l’index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68360ec9c4a616f74392fd9dd34fc9f53b46114
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120014"
---
# <a name="interfaces-for-managing-the-index"></a><span data-ttu-id="fc2c1-103">Interfaces pour la gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="fc2c1-103">Interfaces for Managing the Index</span></span>

<span data-ttu-id="fc2c1-104">Windows Search vous permet de gérer l’index de recherche Windows avec trois composants principaux : le gestionnaire de recherche, le gestionnaire de catalogues et le gestionnaire de l’étendue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-104">Windows Search enables you to manage the Windows Search index with three main components: Search Manager, Catalog Manager, and Crawl Scope Manager.</span></span> <span data-ttu-id="fc2c1-105">Certaines de ces interfaces de gestion peuvent être utilisées avec des privilèges d’utilisateur standard, mais celles qui modifient l’état de l’index requièrent des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-105">Some of these management interfaces can be used with standard user privileges, but those that change the state of the index require administrative privileges.</span></span>

## <a name="about-the-interfaces-for-managing-the-index"></a><span data-ttu-id="fc2c1-106">À propos des interfaces pour la gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="fc2c1-106">About the Interfaces for Managing the Index</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc2c1-107">Composant</span><span class="sxs-lookup"><span data-stu-id="fc2c1-107">Component</span></span></th>
<th><span data-ttu-id="fc2c1-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="fc2c1-108">Interfaces</span></span></th>
<th><span data-ttu-id="fc2c1-109">Description</span><span class="sxs-lookup"><span data-stu-id="fc2c1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc2c1-110">Gestionnaire de recherche</span><span class="sxs-lookup"><span data-stu-id="fc2c1-110">Search Manager</span></span></td>
<td><span data-ttu-id="fc2c1-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-111"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a></span></span></td>
<td><span data-ttu-id="fc2c1-112">Fournit des méthodes pour récupérer et définir des informations sur la recherche Windows :</span><span class="sxs-lookup"><span data-stu-id="fc2c1-112">Provides methods to retrieve and set information about Windows Search:</span></span>
<ul>
<li><span data-ttu-id="fc2c1-113">Obtention d’une instance du gestionnaire de catalogues pour un catalogue spécifique.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-113">Getting an instance of the Catalog Manager for a specific catalog.</span></span></li>
<li><span data-ttu-id="fc2c1-114">Obtention ou définition d’informations de proxy.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-114">Getting or setting proxy information.</span></span></li>
<li><span data-ttu-id="fc2c1-115">Obtention d’informations de version sur le moteur de recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-115">Getting version information about the Windows Search engine.</span></span></li>
</ul>
<span data-ttu-id="fc2c1-116">Pour plus d’informations, consultez <a href="-search-3x-wds-mngidx-searchmanager.md">utilisation du gestionnaire de recherche</a>.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-116">For more information, see <a href="-search-3x-wds-mngidx-searchmanager.md">Using the Search Manager</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fc2c1-117">Gestionnaire de catalogues</span><span class="sxs-lookup"><span data-stu-id="fc2c1-117">Catalog Manager</span></span></td>
<td><span data-ttu-id="fc2c1-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-118"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a></span></span><br/> <span data-ttu-id="fc2c1-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-119"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a></span></span><br/></td>
<td><span data-ttu-id="fc2c1-120">Fournit des méthodes pour gérer un catalogue de recherche individuel, par exemple pour provoquer une réindexation ou définir des délais d’attente.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-120">Provides methods to manage an individual search catalog, such as causing a re-indexing or setting time-outs.</span></span> <span data-ttu-id="fc2c1-121">Cette interface gère le catalogue dans quatre domaines :</span><span class="sxs-lookup"><span data-stu-id="fc2c1-121">This interface manages the catalog in four areas:</span></span>
<ul>
<li><span data-ttu-id="fc2c1-122">Contenu du catalogue : s’assurer que les nouvelles données sont indexées et que d’autres applications et composants fonctionnent correctement en forçant la réindexation de tout ou partie du catalogue ou en réinitialisant l’intégralité du catalogue.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-122">Catalog contents - ensuring that new data is indexed and that other applications and components work properly by forcing a re-indexing of all or part of the catalog or by resetting the entire catalog.</span></span></li>
<li><span data-ttu-id="fc2c1-123">Propriétés du catalogue-définition des propriétés qui déterminent comment le catalogue gère les délais d’attente lors de la connexion aux gestionnaires de protocole et comment les marques diacritiques sont traitées dans les recherches.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-123">Catalog properties - setting properties that determine how the catalog manages time-outs when connecting to protocol handlers and how diacritical marks are treated in searches.</span></span></li>
<li><span data-ttu-id="fc2c1-124">État du catalogue : obtention d’informations sur le catalogue, y compris l’État, la taille et l’état de l’activité actuelle.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-124">Catalog status - getting information about the catalog, including status, size, and current activity state.</span></span></li>
<li><span data-ttu-id="fc2c1-125">Accès à d’autres interfaces : récupération d’autres interfaces relatives à la recherche requises par le gestionnaire de portée d’analyse, les notifications de modification de données et l’interface <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fc2c1-125">Access to other interfaces - retrieving other search-related interfaces required by the Crawl Scope Manager, data change notifications, and the <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> interface.</span></span></li>
</ul>
<span data-ttu-id="fc2c1-126">Pour plus d’informations, consultez <a href="-search-3x-wds-mngidx-catalog-manager.md">utilisation du gestionnaire de catalogues</a>.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-126">For more information, see <a href="-search-3x-wds-mngidx-catalog-manager.md">Using the Catalog Manager</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fc2c1-127">Gestionnaire de l’étendue de l’analyse</span><span class="sxs-lookup"><span data-stu-id="fc2c1-127">Crawl Scope Manager</span></span></td>
<td><span data-ttu-id="fc2c1-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-128"><a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a></span></span><br/> <span data-ttu-id="fc2c1-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-129"><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a></span></span><br/> <span data-ttu-id="fc2c1-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-130"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a></span></span><br/> <span data-ttu-id="fc2c1-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-131"><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a></span></span><br/> <span data-ttu-id="fc2c1-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-132"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a></span></span><br/> <span data-ttu-id="fc2c1-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-133"><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a></span></span><br/> <span data-ttu-id="fc2c1-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span><span class="sxs-lookup"><span data-stu-id="fc2c1-134"><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a></span></span><br/></td>
<td><span data-ttu-id="fc2c1-135">Fournit des méthodes pour informer le moteur de recherche des conteneurs à analyser ou à surveiller, et les éléments sous ces conteneurs à inclure ou exclure dans l’index.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-135">Provides methods to inform the search engine about containers to crawl or watch, and items under those containers to include or exclude in the index.</span></span> <span data-ttu-id="fc2c1-136">Vous pouvez également interroger le gestionnaire de l’étendue de l’analyse pour voir si une URL particulière se trouve dans l’étendue de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-136">You can also query the Crawl Scope Manager to see if a particular URL is in the crawl scope.</span></span> <span data-ttu-id="fc2c1-137">Pour plus d’informations, consultez <a href="-search-3x-wds-extidx-csm.md">utilisation du gestionnaire de portée d’analyse</a>.</span><span class="sxs-lookup"><span data-stu-id="fc2c1-137">For more information, see <a href="-search-3x-wds-extidx-csm.md">Using the Crawl Scope Manager</a>.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="fc2c1-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc2c1-138">Related topics</span></span>

[<span data-ttu-id="fc2c1-139">Gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="fc2c1-139">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)

[<span data-ttu-id="fc2c1-140">Utilisation du gestionnaire de recherche</span><span class="sxs-lookup"><span data-stu-id="fc2c1-140">Using the Search Manager</span></span>](-search-3x-wds-mngidx-searchmanager.md)

[<span data-ttu-id="fc2c1-141">Utilisation du gestionnaire de catalogues</span><span class="sxs-lookup"><span data-stu-id="fc2c1-141">Using the Catalog Manager</span></span>](-search-3x-wds-mngidx-catalog-manager.md)

[<span data-ttu-id="fc2c1-142">Utilisation du gestionnaire de portée d’analyse</span><span class="sxs-lookup"><span data-stu-id="fc2c1-142">Using the Crawl Scope Manager</span></span>](-search-3x-wds-extidx-csm.md)
