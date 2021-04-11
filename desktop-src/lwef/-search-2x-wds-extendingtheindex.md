---
title: Extension de l’index (fonctionnalités héritées de l’environnement Windows)
description: L’utilisation de et le développement des versions 2. x de Microsoft Windows Desktop Search (WDS) sont fortement déconseillées au profit de Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102768"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="24662-103">Extension de l’index (fonctionnalités héritées de l’environnement Windows)</span><span class="sxs-lookup"><span data-stu-id="24662-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="24662-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="24662-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="24662-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="24662-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="24662-106">L’utilisation de et le développement des versions 2. x de Microsoft Windows Desktop Search (WDS) sont fortement déconseillées au profit de [Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="24662-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="24662-107">WDS peut être étendu pour indexer le contenu de nouveaux types de fichiers et de nouveaux magasins de données.</span><span class="sxs-lookup"><span data-stu-id="24662-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="24662-108">Actuellement, WDS 2. x contient des filtres pour plus de 200 types d’éléments (y compris des éléments en texte brut tels que des fichiers HTML, XML et de code source) et utilise la même technologie [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)et le même gestionnaire de protocole que SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="24662-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="24662-109">Si vous avez déjà installé des implémentations de filtre pour vos nouveaux types de fichiers, WDS peut utiliser les interfaces de filtre existantes pour indexer ces données.</span><span class="sxs-lookup"><span data-stu-id="24662-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="24662-110">Les compléments WDS 2. x permettent à l’index de traverser et d’analyser les nouvelles données et structures de données pour les informations à ajouter au catalogue pouvant faire l’objet d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="24662-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="24662-111">Ces compléments peuvent également étendre le shell Windows pour associer des icônes et des gestionnaires de menus contextuels aux nouveaux types de fichiers et banques de données.</span><span class="sxs-lookup"><span data-stu-id="24662-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="24662-112">Pour inclure de nouveaux types de fichiers dans le catalogue WDS, un complément doit implémenter l’interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).</span><span class="sxs-lookup"><span data-stu-id="24662-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="24662-113">Pour inclure de nouveaux magasins de données, un complément doit être un gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="24662-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="24662-114">Si le nouveau magasin de données comprend des fichiers incorporés ou de nouveaux types de fichiers, vous devrez également écrire un filtre approprié.</span><span class="sxs-lookup"><span data-stu-id="24662-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="24662-115">Les filtres et les gestionnaires de protocole doivent être écrits en code natif en raison de problèmes potentiels de contrôle de version CLR avec le processus dans lequel tous les compléments s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="24662-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="24662-116">Ajout de types de fichiers à l’index</span><span class="sxs-lookup"><span data-stu-id="24662-116">Adding File Types to the Index</span></span>

<span data-ttu-id="24662-117">Les compléments peuvent étendre WDS pour indexer les types de fichiers nouveaux ou propriétaires et associer chaque nouveau type de fichier à une icône ou un menu contextuel propre au fichier.</span><span class="sxs-lookup"><span data-stu-id="24662-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="24662-118">Pour ce faire, vous pouvez créer et inscrire un complément qui :</span><span class="sxs-lookup"><span data-stu-id="24662-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="24662-119">Implémente une interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)pour chaque type de fichier afin que WDS puisse accéder et indexer le texte et les métadonnées du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="24662-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="24662-120">Implémente les interfaces **IExtractIcon** et **IContextMenu** pour ajouter des icônes et des menus contextuels pour une intégration et une convivialité supérieures.</span><span class="sxs-lookup"><span data-stu-id="24662-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="24662-121">Pour plus d’informations sur l’implémentation des filtres, consultez [développement de compléments IFilter](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="24662-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="24662-122">Ajout de magasins de données à l’index</span><span class="sxs-lookup"><span data-stu-id="24662-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="24662-123">Les compléments peuvent étendre WDS pour indexer de nouveaux magasins de données et associer des fichiers à une icône ou un menu contextuel propre à un fichier.</span><span class="sxs-lookup"><span data-stu-id="24662-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="24662-124">Pour ce faire, vous pouvez créer et inscrire un gestionnaire de protocole qui :</span><span class="sxs-lookup"><span data-stu-id="24662-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="24662-125">Implémente les interfaces **ISearchProtocol** et **IUrlAccessor** pour traiter et lier des éléments individuels dans la source de contenu.</span><span class="sxs-lookup"><span data-stu-id="24662-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="24662-126">WDS utilise des URL pour identifier de manière unique les éléments, que ces éléments se trouvent dans le système de fichiers, à l’intérieur d’un magasin de base de données ou sur le Web.</span><span class="sxs-lookup"><span data-stu-id="24662-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="24662-127">Implémente l’interface **IPersistFolder** et des parties de l’interface **IShellFolder** pour ajouter des icônes et des menus contextuels pour une intégration et une convivialité supérieures.</span><span class="sxs-lookup"><span data-stu-id="24662-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="24662-128">Pour plus d’informations sur l’implémentation de gestionnaires de protocole, consultez [développement de gestionnaires de protocole](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="24662-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="24662-129">Instructions du programme d’installation du complément</span><span class="sxs-lookup"><span data-stu-id="24662-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="24662-130">L’installation d’un complément doit suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="24662-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="24662-131">Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.</span><span class="sxs-lookup"><span data-stu-id="24662-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="24662-132">Des notes de publication doivent être fournies.</span><span class="sxs-lookup"><span data-stu-id="24662-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="24662-133">Une entrée **Ajout/suppression de programmes** doit être créée pour chaque complément installé.</span><span class="sxs-lookup"><span data-stu-id="24662-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="24662-134">Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.</span><span class="sxs-lookup"><span data-stu-id="24662-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="24662-135">Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24662-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="24662-136">Si un complément plus récent a remplacé le complément précédent, il devrait y avoir la possibilité de restaurer les fonctionnalités du complément précédent et de le faire en tant que complément par défaut pour ce type de fichier ou en magasin.</span><span class="sxs-lookup"><span data-stu-id="24662-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24662-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24662-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24662-138">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="24662-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24662-139">Développement de compléments IFilter</span><span class="sxs-lookup"><span data-stu-id="24662-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="24662-140">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="24662-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="24662-141">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="24662-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="24662-142">**Filtres**</span><span class="sxs-lookup"><span data-stu-id="24662-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
