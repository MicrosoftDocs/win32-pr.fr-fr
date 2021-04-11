---
description: Microsoft fournit plusieurs filtres standard avec Windows Search. Les clients appellent ces gestionnaires de filtres (qui sont des implémentations de l’interface IFilter) pour extraire du texte et des propriétés d’un document.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Gestionnaires de filtres fournis avec Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112451"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="94357-104">Gestionnaires de filtres fournis avec Windows</span><span class="sxs-lookup"><span data-stu-id="94357-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="94357-105">Microsoft fournit plusieurs filtres standard avec Windows Search.</span><span class="sxs-lookup"><span data-stu-id="94357-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="94357-106">Les clients appellent ces gestionnaires de filtres (qui sont des implémentations de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) pour extraire du texte et des propriétés d’un document.</span><span class="sxs-lookup"><span data-stu-id="94357-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="94357-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="94357-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="94357-108">Remarques sur l’implémentation de Windows Search</span><span class="sxs-lookup"><span data-stu-id="94357-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="94357-109">Implémentation de Windows 7 et 10</span><span class="sxs-lookup"><span data-stu-id="94357-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="94357-110">Implémentation de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94357-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="94357-111">Implémentation héritée</span><span class="sxs-lookup"><span data-stu-id="94357-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="94357-112">Filtres de recherche Windows</span><span class="sxs-lookup"><span data-stu-id="94357-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="94357-113">Gestionnaire de filtre MIME</span><span class="sxs-lookup"><span data-stu-id="94357-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="94357-114">Gestionnaire de filtre HTML</span><span class="sxs-lookup"><span data-stu-id="94357-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="94357-115">Gestionnaire de filtre de document</span><span class="sxs-lookup"><span data-stu-id="94357-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="94357-116">Gestionnaire de filtre de texte brut</span><span class="sxs-lookup"><span data-stu-id="94357-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="94357-117">Gestionnaire de filtres binaire ou null</span><span class="sxs-lookup"><span data-stu-id="94357-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="94357-118">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="94357-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="94357-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94357-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="94357-120">Remarques sur l’implémentation de Windows Search</span><span class="sxs-lookup"><span data-stu-id="94357-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="94357-121">Dans Windows 7 et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement.</span><span class="sxs-lookup"><span data-stu-id="94357-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="94357-122">Les filtres doivent être écrits en code natif en raison des éventuels problèmes de versioning du CLR avec le processus dans lequel plusieurs compléments s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="94357-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="94357-123">Implémentation de Windows 7 et 10</span><span class="sxs-lookup"><span data-stu-id="94357-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="94357-124">Dans Windows 7 et versions ultérieures, un nouveau comportement se produit lors de l’inscription d’un gestionnaire de filtres, d’un gestionnaire de propriétés ou d’une nouvelle extension.</span><span class="sxs-lookup"><span data-stu-id="94357-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="94357-125">Lorsqu’un nouveau gestionnaire de propriétés et/ou gestionnaire de filtres est installé, les fichiers avec les extensions correspondantes sont automatiquement réindexés.</span><span class="sxs-lookup"><span data-stu-id="94357-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="94357-126">Dans Windows 7 et versions ultérieures, nous vous recommandons d’installer un gestionnaire de filtres conjointement avec les gestionnaires de propriétés correspondants, et d’inscrire le gestionnaire de filtres avant le gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="94357-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="94357-127">L’inscription du gestionnaire de propriétés lance la réindexation immédiate des fichiers précédemment indexés sans nécessiter un redémarrage, et tire parti des gestionnaires de filtres précédemment enregistrés pour l’indexation du contenu.</span><span class="sxs-lookup"><span data-stu-id="94357-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="94357-128">Si seul un gestionnaire de filtres est installé sans gestionnaire de propriétés correspondant, la réindexation automatique se produit soit après un redémarrage du service d’indexation, soit par un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="94357-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="94357-129">Pour les indicateurs de description de propriété spécifiques à Windows 7, consultez les rubriques de référence suivantes : [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC \_ COLUMNINDEX \_ type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) et [PROPDESC \_ SEARCHINFO \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span><span class="sxs-lookup"><span data-stu-id="94357-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="94357-130">Implémentation de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94357-130">Windows Vista Implementation</span></span>

<span data-ttu-id="94357-131">Dans Windows Vista et les versions antérieures, l’installation d’un gestionnaire [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ou d’un gestionnaire de propriétés n’initie pas la réindexation des éléments existants, à moins qu’un éditeur de logiciels indépendant (ISV) appelle explicitement une régénération ou une réindexation des URL correspondantes.</span><span class="sxs-lookup"><span data-stu-id="94357-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="94357-132">Il existe deux différences majeures entre les applications héritées telles que le service d’indexation et les applications plus récentes telles que Windows Search dont vous devez être conscient lors de l’implémentation de filtres :</span><span class="sxs-lookup"><span data-stu-id="94357-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="94357-133">Utilisation de l’interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .</span><span class="sxs-lookup"><span data-stu-id="94357-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="94357-134">Utilisation de gestionnaires de propriétés.</span><span class="sxs-lookup"><span data-stu-id="94357-134">Use of property handlers.</span></span>

<span data-ttu-id="94357-135">Tout d’abord, Windows Vista et Windows Search 3,0 et versions ultérieures requièrent que vous utilisiez [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) pour les raisons suivantes :</span><span class="sxs-lookup"><span data-stu-id="94357-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="94357-136">Pour garantir les performances et la compatibilité future.</span><span class="sxs-lookup"><span data-stu-id="94357-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="94357-137">Pour renforcer la sécurité.</span><span class="sxs-lookup"><span data-stu-id="94357-137">To help increase security.</span></span> <span data-ttu-id="94357-138">Les filtres implémentés avec [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) sont plus sécurisés, car le contexte dans lequel le filtre s’exécute n’a pas besoin des droits pour ouvrir des fichiers sur le disque ou sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="94357-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="94357-139">Alors que Windows Search utilise uniquement [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), vous pouvez également inclure l' [interface IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) et/ou les implémentations d' [interface IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) dans vos filtres à des fins de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="94357-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="94357-140">La deuxième différence majeure réside dans le fait que Windows Vista et Windows Search 3,0 et versions ultérieures ont un nouveau [système de propriétés](../properties/building-property-handlers.md) qui utilise des gestionnaires de propriétés pour énumérer les propriétés des éléments.</span><span class="sxs-lookup"><span data-stu-id="94357-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="94357-141">Toutefois, il peut arriver que vous deviez implémenter un filtre qui gère à la fois le contenu et les propriétés afin d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="94357-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="94357-142">Prennent en charge les implémentations MSSearch héritées.</span><span class="sxs-lookup"><span data-stu-id="94357-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="94357-143">Parcourez les liens.</span><span class="sxs-lookup"><span data-stu-id="94357-143">Traverse links.</span></span>
- <span data-ttu-id="94357-144">Conserver les informations de langue.</span><span class="sxs-lookup"><span data-stu-id="94357-144">Preserve language information.</span></span>
- <span data-ttu-id="94357-145">Filtrer les éléments incorporés de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="94357-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="94357-146">Dans ce cas, vous avez besoin d’une implémentation de filtre complète, y compris la méthode [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) pour accéder aux valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="94357-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="94357-147">Implémentation héritée</span><span class="sxs-lookup"><span data-stu-id="94357-147">Legacy Implementation</span></span>

<span data-ttu-id="94357-148">Comme indiqué précédemment, Windows Vista et Windows Search incluent un nouveau système de propriétés qui encapsule les propriétés d’un élément qui sont séparées du contenu d’un élément.</span><span class="sxs-lookup"><span data-stu-id="94357-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="94357-149">Ce système de propriétés n’existe pas dans les versions antérieures de Microsoft Windows Desktop Search (WDS) 2. x.</span><span class="sxs-lookup"><span data-stu-id="94357-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="94357-150">Si votre filtre doit prendre en charge d’autres applications comme décrit ci-dessus, il peut être nécessaire de gérer le contenu et les propriétés.</span><span class="sxs-lookup"><span data-stu-id="94357-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="94357-151">Pour plus d’informations sur le développement d’un filtre compatible, consultez les rubriques suivantes, [IFilter (pour les applications héritées)](/windows/win32/api/filter/nn-filter-ifilter)et [développement de compléments de filtre (pour les applications héritées)](../lwef/-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="94357-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="94357-152">Filtres de recherche Windows</span><span class="sxs-lookup"><span data-stu-id="94357-152">Windows Search Filters</span></span>

<span data-ttu-id="94357-153">Microsoft fournit plusieurs filtres standard avec Windows Search.</span><span class="sxs-lookup"><span data-stu-id="94357-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="94357-154">Le contenu de la dll [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  est résumé dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94357-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="94357-155">Le fait de cliquer sur le nom d’un gestionnaire de filtres vous amène à la description de cette implémentation **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="94357-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="94357-156">Gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="94357-156">Filter handler</span></span>                                                  | <span data-ttu-id="94357-157">Fichiers filtrés</span><span class="sxs-lookup"><span data-stu-id="94357-157">Files filtered</span></span>                              | <span data-ttu-id="94357-158">DLL IFilter</span><span class="sxs-lookup"><span data-stu-id="94357-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="94357-159">Gestionnaire de filtre MIME</span><span class="sxs-lookup"><span data-stu-id="94357-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="94357-160">MIME (Multipurpose Internet Mail extension)</span><span class="sxs-lookup"><span data-stu-id="94357-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="94357-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="94357-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="94357-162">Gestionnaire de filtre HTML</span><span class="sxs-lookup"><span data-stu-id="94357-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="94357-163">HTML 3,0 ou version antérieure</span><span class="sxs-lookup"><span data-stu-id="94357-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="94357-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="94357-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="94357-165">Gestionnaire de filtre de document</span><span class="sxs-lookup"><span data-stu-id="94357-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="94357-166">Microsoft Word, Excel, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="94357-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="94357-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="94357-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="94357-168">Gestionnaire de filtre de texte brut</span><span class="sxs-lookup"><span data-stu-id="94357-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="94357-169">Fichiers texte brut-IFilter par défaut</span><span class="sxs-lookup"><span data-stu-id="94357-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="94357-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="94357-170">query.dll</span></span>    |
| [<span data-ttu-id="94357-171">Gestionnaire de filtres binaire ou null</span><span class="sxs-lookup"><span data-stu-id="94357-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="94357-172">Fichiers binaires-IFilter null</span><span class="sxs-lookup"><span data-stu-id="94357-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="94357-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="94357-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="94357-174">Gestionnaire de filtre MIME</span><span class="sxs-lookup"><span data-stu-id="94357-174">MIME Filter Handler</span></span>

<span data-ttu-id="94357-175">Le gestionnaire de filtre MIME (en mimefilt.dll) extrait les informations de texte et de propriété des fichiers avec les extensions. eml,. mht et. MHTML.</span><span class="sxs-lookup"><span data-stu-id="94357-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="94357-176">Gestionnaire de filtre HTML</span><span class="sxs-lookup"><span data-stu-id="94357-176">HTML Filter Handler</span></span>

<span data-ttu-id="94357-177">Le gestionnaire de filtre HTML (en nlhtml.dll) extrait les informations de texte et de propriété de la classe « HtmlFiles » afin qu’elles puissent être indexées par la recherche Windows.</span><span class="sxs-lookup"><span data-stu-id="94357-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="94357-178">Pour obtenir une description de l’association entre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et le type de fichier, consultez « recherche de la DLL IFilter pour un fichier » dans [inscription des gestionnaires de filtres](-search-ifilter-registering-filters.md).</span><span class="sxs-lookup"><span data-stu-id="94357-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="94357-179">Vous pouvez utiliser la `META` fonctionnalité tag des documents html pour transmettre des demandes de traitement spéciales au [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)html.</span><span class="sxs-lookup"><span data-stu-id="94357-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="94357-180">`META` les balises se produisent vers le début d’un fichier HTML au sein des `HEAD ... /HEAD` balises, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="94357-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="94357-181">Certaines `META` balises HTML sont automatiquement mappées à des valeurs de jeu de propriétés et d’ID de propriété (PID) bien connues afin que les requêtes sur ces propriétés recherchent le contenu mappé.</span><span class="sxs-lookup"><span data-stu-id="94357-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="94357-182">Certains exemples sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94357-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="94357-183">Pour obtenir la liste des propriétés système que vous pouvez utiliser pour vos formats de fichier, consultez [propriétés définies par le système pour les formats de fichiers personnalisés](-shell-systemdefinedpropertiesforfileformats.md).</span><span class="sxs-lookup"><span data-stu-id="94357-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="94357-184">Exemple de propriété</span><span class="sxs-lookup"><span data-stu-id="94357-184">Property example</span></span>                              | <span data-ttu-id="94357-185">Mappé à</span><span class="sxs-lookup"><span data-stu-id="94357-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="94357-186">Meta Name = "Author" Content = "Ruth"</span><span class="sxs-lookup"><span data-stu-id="94357-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="94357-187">Propriété Author dans la propriété informations récapitulatives définie.</span><span class="sxs-lookup"><span data-stu-id="94357-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="94357-188">Meta Name = "subject" Content = "traitement de texte"</span><span class="sxs-lookup"><span data-stu-id="94357-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="94357-189">Propriété Subject dans la propriété informations récapitulatives définie.</span><span class="sxs-lookup"><span data-stu-id="94357-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="94357-190">Meta Name = "Mots clés" Content = "polices, Serif"</span><span class="sxs-lookup"><span data-stu-id="94357-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="94357-191">Propriété de mot clé dans la propriété informations récapitulatives définie.</span><span class="sxs-lookup"><span data-stu-id="94357-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="94357-192">Meta Name = "ms. Category" Content = "fiction"</span><span class="sxs-lookup"><span data-stu-id="94357-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="94357-193">Propriété Category dans la propriété informations récapitulatives du document définie.</span><span class="sxs-lookup"><span data-stu-id="94357-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="94357-194">Certaines fonctionnalités du [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) HTML sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="94357-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (Cette table doit être au format HTML pour que les exemples soient correctement formatés.)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94357-196">Tâche</span><span class="sxs-lookup"><span data-stu-id="94357-196">Task</span></span></th>
<th><span data-ttu-id="94357-197">Action</span><span class="sxs-lookup"><span data-stu-id="94357-197">Action</span></span></th>
<th><span data-ttu-id="94357-198">Exemple</span><span class="sxs-lookup"><span data-stu-id="94357-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94357-199">Création d’abstractions spéciales à partir de fichiers</span><span class="sxs-lookup"><span data-stu-id="94357-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="94357-200">Utilisez la <code>META NAME=&quot;DESCRIPTION&quot;...</code> balise pour indiquer au <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> d’utiliser la chaîne qui suit le <code>CONTENT</code> mot clé comme Résumé du document.</span><span class="sxs-lookup"><span data-stu-id="94357-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="94357-201">Le processus de filtrage peut générer des abstractions pour chaque fichier filtré, qui est par défaut un ensemble de caractères au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="94357-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="94357-202">Empêcher le filtrage de fichiers individuels</span><span class="sxs-lookup"><span data-stu-id="94357-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="94357-203">Ajoutez une <code>meta name</code> balise au fichier.</span><span class="sxs-lookup"><span data-stu-id="94357-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94357-204">Définition du code de langue d’un fichier (pour s’assurer que le système choisit les analyseurs lexicaux de langue et les fichiers de mots parasites corrects)</span><span class="sxs-lookup"><span data-stu-id="94357-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="94357-205">Ajoutez la <code>meta name</code> balise suivante au fichier, où le champ de contenu spécifie le code de langue approprié (soit en caractères, soit en utilisant la valeur de paramètres régionaux).</span><span class="sxs-lookup"><span data-stu-id="94357-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="94357-206">Gestionnaire de filtre de document</span><span class="sxs-lookup"><span data-stu-id="94357-206">Document Filter Handler</span></span>

<span data-ttu-id="94357-207">Le gestionnaire de filtre de document (dans offilt.dll) filtre les fichiers pour certaines extensions de documents dans Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="94357-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="94357-208">Il s’agit notamment des fichiers avec les extensions. doc,. mdb,. ppt et. xlt, par exemple.</span><span class="sxs-lookup"><span data-stu-id="94357-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="94357-209">Gestionnaire de filtre de texte brut</span><span class="sxs-lookup"><span data-stu-id="94357-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="94357-210">Pour les fichiers en texte brut, Windows Search utilise le gestionnaire de filtre de texte, qui filtre les propriétés système (telles que les noms de fichiers) et le contenu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="94357-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="94357-211">Lorsqu’un type de fichier n’a pas d’association [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) dans le registre, Windows Search indexe uniquement les propriétés de l’interpréteur de commandes pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="94357-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="94357-212">Toutefois, l’utilisateur peut utiliser les **Options avancées** dans les **options d’indexation** du panneau de configuration pour **indexer les propriétés** ou les propriétés d' **index et le contenu des fichiers**.</span><span class="sxs-lookup"><span data-stu-id="94357-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![capture d’écran montrant la boîte de dialogue Options avancées](images/ifilteradvancedoptions.png)

<span data-ttu-id="94357-214">Si l’utilisateur choisit cette option pour un type de fichier sans [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)associé, le gestionnaire de filtre de texte est utilisé pour extraire le contenu du fichier.</span><span class="sxs-lookup"><span data-stu-id="94357-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="94357-215">Le gestionnaire de filtre de texte ne peut pas « comprendre » tout format de document ; lors du filtrage du contenu d’un fichier, il traite le fichier comme une séquence de caractères.</span><span class="sxs-lookup"><span data-stu-id="94357-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="94357-216">Il vérifie la marque d’ordre d’octet Unicode au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="94357-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="94357-217">Gestionnaire de filtres binaire ou null</span><span class="sxs-lookup"><span data-stu-id="94357-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="94357-218">Lorsqu’un fichier binaire enregistré est rencontré, le gestionnaire de filtre null est utilisé.</span><span class="sxs-lookup"><span data-stu-id="94357-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="94357-219">Le gestionnaire de filtre null récupère uniquement les propriétés système.</span><span class="sxs-lookup"><span data-stu-id="94357-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="94357-220">Le contenu d’un fichier binaire n’est pas filtré.</span><span class="sxs-lookup"><span data-stu-id="94357-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="94357-221">**Nom de fichier**, **LastWriteTime**, **taille** et **attributs** sont des exemples de propriétés système.</span><span class="sxs-lookup"><span data-stu-id="94357-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94357-222">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="94357-222">Additional Resources</span></span>

- <span data-ttu-id="94357-223">L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base IFilter pour l’implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="94357-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="94357-224">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94357-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="94357-225">Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="94357-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="94357-226">Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94357-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94357-227">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="94357-227">Related topics</span></span>

[<span data-ttu-id="94357-228">Développement de gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="94357-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="94357-229">À propos des gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="94357-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="94357-230">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="94357-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="94357-231">Retour des propriétés d’un gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="94357-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="94357-232">Implémentation de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="94357-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="94357-233">Inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="94357-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="94357-234">Test des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="94357-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
