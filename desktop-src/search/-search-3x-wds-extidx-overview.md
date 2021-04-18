---
description: Vous pouvez étendre Windows Search pour indexer le contenu et les propriétés de nouveaux formats de fichier, ainsi que les magasins de données à l’aide d’interfaces de complément de données.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Extension de l’index (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512943"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="5772c-103">Extension de l’index (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="5772c-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="5772c-104">Vous pouvez étendre Windows Search pour indexer le contenu et les propriétés de nouveaux formats de fichier, ainsi que les magasins de données à l’aide d' [interfaces de complément de données](./-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="5772c-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="5772c-105">Pour créer des compléments de recherche Windows, les développeurs tiers doivent tout d’abord implémenter un magasin de données Shell, puis développer un gestionnaire de protocole pour que la recherche Windows puisse accéder aux données pour l’indexation.</span><span class="sxs-lookup"><span data-stu-id="5772c-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="5772c-106">Si vous disposez d’un format de fichier personnalisé, vous devez développer un gestionnaire de filtre pour indexer le contenu du fichier et un gestionnaire de propriétés pour chaque type de fichier aux propriétés d’index.</span><span class="sxs-lookup"><span data-stu-id="5772c-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="5772c-107">Windows Search prend actuellement en charge l’indexation de plus de 200 types d’éléments (tels que les formats de fichier. txt,. html et. Xml) et peut fonctionner avec plusieurs types de magasins de données (tels que le système de fichiers NTFS et Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="5772c-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="5772c-108">Windows Search utilise une technologie de filtre et de gestionnaire de protocole similaire à celle de SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="5772c-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="5772c-109">Par conséquent, si vous avez déjà des implémentations pour votre format de fichier, vous pouvez mettre à jour les implémentations à initialiser avec un flux à l’aide de [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) afin que le filtre fonctionne avec la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="5772c-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="5772c-110">Les gestionnaires de filtres, les gestionnaires de propriétés et les gestionnaires de protocole doivent être écrits en code natif.</span><span class="sxs-lookup"><span data-stu-id="5772c-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="5772c-111">Cela est dû à des problèmes potentiels de contrôle de version du common language runtime (CLR) avec le processus dans lequel plusieurs compléments s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="5772c-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="5772c-112">Cette section sur l’extension de l’index avec les compléments contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5772c-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="5772c-113">Développement de gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="5772c-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="5772c-114">Développement de gestionnaires de propriétés pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="5772c-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="5772c-115">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="5772c-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="5772c-116">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="5772c-116">Additional Resources</span></span>

<span data-ttu-id="5772c-117">Pour obtenir des exemples de code associés, consultez [exemples de code Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="5772c-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5772c-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5772c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5772c-119">Guide de développement de Windows Search</span><span class="sxs-lookup"><span data-stu-id="5772c-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="5772c-120">Gestion de l’index</span><span class="sxs-lookup"><span data-stu-id="5772c-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="5772c-121">Interrogation de l’index programmatiquement</span><span class="sxs-lookup"><span data-stu-id="5772c-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="5772c-122">Extension des ressources linguistiques</span><span class="sxs-lookup"><span data-stu-id="5772c-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
