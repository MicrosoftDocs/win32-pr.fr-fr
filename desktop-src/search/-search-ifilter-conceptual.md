---
description: Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Développement de gestionnaires de filtres pour Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033883"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="243ec-103">Développement de gestionnaires de filtres pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="243ec-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="243ec-104">Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral.</span><span class="sxs-lookup"><span data-stu-id="243ec-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="243ec-105">Vous pouvez étendre Windows Search pour indexer les types de fichiers nouveaux ou propriétaires en écrivant des filtres pour extraire le contenu et les gestionnaires de propriétés pour extraire les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="243ec-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="243ec-106">Cette section fournit l’infrastructure conceptuelle nécessaire à l’implémentation d’un gestionnaire de filtres (une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).</span><span class="sxs-lookup"><span data-stu-id="243ec-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="243ec-107">Fonctionnement des gestionnaires de filtres dans la recherche Windows</span><span class="sxs-lookup"><span data-stu-id="243ec-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="243ec-108">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="243ec-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="243ec-109">Retour des propriétés d’un gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="243ec-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="243ec-110">Gestionnaires de filtres fournis avec Windows</span><span class="sxs-lookup"><span data-stu-id="243ec-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="243ec-111">Implémentation de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="243ec-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="243ec-112">Inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="243ec-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="243ec-113">Test des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="243ec-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="243ec-114">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="243ec-114">Additional Resources</span></span>

- <span data-ttu-id="243ec-115">L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="243ec-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="243ec-116">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="243ec-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="243ec-117">Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="243ec-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="243ec-118">Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="243ec-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
