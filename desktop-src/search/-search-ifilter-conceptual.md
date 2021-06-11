---
description: Découvrez comment développer des gestionnaires de filtres dans la recherche Windows. La recherche utilise des filtres pour extraire les éléments à inclure dans un index de recherche en texte intégral.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Développement de gestionnaires de filtres pour Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988858"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="44532-104">Développement de gestionnaires de filtres pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="44532-104">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="44532-105">Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral.</span><span class="sxs-lookup"><span data-stu-id="44532-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="44532-106">Vous pouvez étendre Windows Search pour indexer les types de fichiers nouveaux ou propriétaires en écrivant des filtres pour extraire le contenu et les gestionnaires de propriétés pour extraire les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="44532-106">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="44532-107">Cette section fournit l’infrastructure conceptuelle nécessaire à l’implémentation d’un gestionnaire de filtres (une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).</span><span class="sxs-lookup"><span data-stu-id="44532-107">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="44532-108">Fonctionnement des gestionnaires de filtres dans la recherche Windows</span><span class="sxs-lookup"><span data-stu-id="44532-108">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="44532-109">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="44532-109">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="44532-110">Retour des propriétés d’un gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="44532-110">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="44532-111">Gestionnaires de filtres fournis avec Windows</span><span class="sxs-lookup"><span data-stu-id="44532-111">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="44532-112">Implémentation de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="44532-112">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="44532-113">Inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="44532-113">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="44532-114">Test des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="44532-114">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="44532-115">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="44532-115">Additional Resources</span></span>

- <span data-ttu-id="44532-116">L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="44532-116">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="44532-117">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="44532-117">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="44532-118">Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="44532-118">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="44532-119">Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="44532-119">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
