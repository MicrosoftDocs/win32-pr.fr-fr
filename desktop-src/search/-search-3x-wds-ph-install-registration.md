---
description: L’installation d’un gestionnaire de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files, puis l’inscription du gestionnaire de protocole dans le registre.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Installation et inscription de gestionnaires de protocole (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516622"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a><span data-ttu-id="8857b-103">Installation et inscription de gestionnaires de protocole (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="8857b-103">Installing and Registering Protocol Handlers (Windows Search)</span></span>

<span data-ttu-id="8857b-104">L’installation d’un gestionnaire de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files, puis l’inscription du gestionnaire de protocole dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8857b-104">Installing a protocol handler involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the protocol handler through the registry.</span></span> <span data-ttu-id="8857b-105">L’application d’installation peut également ajouter une racine de recherche et des règles d’étendue pour définir une étendue d’analyse par défaut pour la source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="8857b-105">The installation application can also add a search root and scope rules to define a default crawl scope for the Shell data source.</span></span>

<span data-ttu-id="8857b-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="8857b-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="8857b-107">À propos des URL</span><span class="sxs-lookup"><span data-stu-id="8857b-107">About URLs</span></span>](#about-urls)
-   [<span data-ttu-id="8857b-108">Implémentation d’interfaces de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-108">Implementing Protocol Handler Interfaces</span></span>](#implementing-protocol-handler-interfaces)
    -   [<span data-ttu-id="8857b-109">ISearchProtocol et ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="8857b-109">ISearchProtocol and ISearchProtocol2</span></span>](#isearchprotocol-and-isearchprotocol2)
    -   [<span data-ttu-id="8857b-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 et IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="8857b-110">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [<span data-ttu-id="8857b-111">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="8857b-111">IProtocolHandlerSite</span></span>](#iprotocolhandlersite)
-   [<span data-ttu-id="8857b-112">Implémentation de gestionnaires de filtres pour les conteneurs</span><span class="sxs-lookup"><span data-stu-id="8857b-112">Implementing Filter Handlers for Containers</span></span>](#implementing-filter-handlers-for-containers)
-   [<span data-ttu-id="8857b-113">Installation et inscription d’un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-113">Installing and Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="8857b-114">Instructions pour l’inscription d’un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-114">Guidelines for Registering a Protocol Handler</span></span>](#guidelines-for-registering-a-protocol-handler)
    -   [<span data-ttu-id="8857b-115">Inscription d’un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-115">Registering a Protocol Handler</span></span>](#installing-and-registering-a-protocol-handler)
    -   [<span data-ttu-id="8857b-116">Inscription du gestionnaire de type de fichier du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-116">Registering the Protocol Handler's File Type Handler</span></span>](#registering-the-protocol-handlers-file-type-handler)
-   [<span data-ttu-id="8857b-117">Vérification de l’indexation de vos éléments</span><span class="sxs-lookup"><span data-stu-id="8857b-117">Ensuring that Your Items are Indexed</span></span>](#ensuring-that-your-items-are-indexed)
-   [<span data-ttu-id="8857b-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8857b-118">Related topics</span></span>](#related-topics)

## <a name="about-urls"></a><span data-ttu-id="8857b-119">À propos des URL</span><span class="sxs-lookup"><span data-stu-id="8857b-119">About URLs</span></span>

<span data-ttu-id="8857b-120">Windows Search utilise des URL pour identifier de manière unique les éléments dans la hiérarchie de votre source de données de Shell.</span><span class="sxs-lookup"><span data-stu-id="8857b-120">Windows Search uses URLs to uniquely identify items in the hierarchy of your Shell data source.</span></span> <span data-ttu-id="8857b-121">L’URL qui est le premier nœud de la hiérarchie est appelée [racine de recherche](-search-3x-wds-extidx-csm-searchroots.md). La recherche Windows commence l’indexation à la racine de recherche, en demandant que le gestionnaire de protocole énumère les liens enfants pour chaque URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-121">The URL that is the first node in the hierarchy is called the [search root](-search-3x-wds-extidx-csm-searchroots.md); Windows Search will begin indexing at the search root, requesting that the protocol handler enumerate child links for each URL.</span></span>

<span data-ttu-id="8857b-122">La structure d’URL standard est la suivante :</span><span class="sxs-lookup"><span data-stu-id="8857b-122">The typical URL structure is:</span></span>


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



<span data-ttu-id="8857b-123">La syntaxe de l’URL est décrite dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8857b-123">The URL syntax is described in the following table.</span></span>



| <span data-ttu-id="8857b-124">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8857b-124">Syntax</span></span>           | <span data-ttu-id="8857b-125">Description</span><span class="sxs-lookup"><span data-stu-id="8857b-125">Description</span></span>                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | <span data-ttu-id="8857b-126">Identifie le gestionnaire de protocole à appeler pour l’URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-126">Identifies which protocol handler to invoke for the URL.</span></span>                                                                                                                                                           |
| <span data-ttu-id="8857b-127">{SID utilisateur}</span><span class="sxs-lookup"><span data-stu-id="8857b-127">{user SID}</span></span>       | <span data-ttu-id="8857b-128">Identifie le contexte de sécurité de l’utilisateur sous lequel le gestionnaire de protocole est appelé.</span><span class="sxs-lookup"><span data-stu-id="8857b-128">Identifies the user security context under which the protocol handler is called.</span></span> <span data-ttu-id="8857b-129">Si aucun identificateur de sécurité (SID) utilisateur n’est identifié, le gestionnaire de protocole est appelé dans le contexte de sécurité du service système.</span><span class="sxs-lookup"><span data-stu-id="8857b-129">If no user security identifier (SID) is identified, the protocol handler is called in the security context of the system service.</span></span> |
| <path>     | <span data-ttu-id="8857b-130">Définit la hiérarchie du magasin, où chaque barre oblique (« / ») est un séparateur entre les noms de dossiers.</span><span class="sxs-lookup"><span data-stu-id="8857b-130">Defines the hierarchy of the store, where each forward slash ('/') is a separator between folder names.</span></span>                                                                                                            |
| <ItemID>   | <span data-ttu-id="8857b-131">Représente une chaîne unique qui identifie l’élément enfant (par exemple, le nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="8857b-131">Represents a unique string that identifies the child item (for example, the file name).</span></span>                                                                                                                            |



 

<span data-ttu-id="8857b-132">L’indexeur de recherche Windows supprime la barre oblique finale des URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-132">The Windows Search Indexer trims the final slash from URLs.</span></span> <span data-ttu-id="8857b-133">Par conséquent, vous ne pouvez pas compter sur l’existence d’une barre oblique finale pour identifier un répertoire par rapport à un élément.</span><span class="sxs-lookup"><span data-stu-id="8857b-133">As a result you cannot rely on the existence of a final slash to identify a directory versus an item.</span></span> <span data-ttu-id="8857b-134">Votre gestionnaire de protocole doit être en mesure de gérer cette syntaxe d’URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-134">Your protocol handler must be able to handle this URL syntax.</span></span> <span data-ttu-id="8857b-135">Assurez-vous que le nom du protocole que vous sélectionnez pour identifier votre source de données Shell n’est pas en conflit avec les noms actuels.</span><span class="sxs-lookup"><span data-stu-id="8857b-135">Ensure that the protocol name that you select to identify your Shell data source does not conflict with current ones.</span></span> <span data-ttu-id="8857b-136">Nous vous recommandons d’utiliser cette Convention d’affectation de noms : `companyName.scheme` .</span><span class="sxs-lookup"><span data-stu-id="8857b-136">We recommend this naming convention: `companyName.scheme`.</span></span>

<span data-ttu-id="8857b-137">Pour plus d’informations sur la création d’une source de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8857b-137">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

## <a name="implementing-protocol-handler-interfaces"></a><span data-ttu-id="8857b-138">Implémentation d’interfaces de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-138">Implementing Protocol Handler Interfaces</span></span>

<span data-ttu-id="8857b-139">La création d’un gestionnaire de protocole requiert l’implémentation des trois interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="8857b-139">Creating a protocol handler requires the implementation of the following three interfaces:</span></span>

-   <span data-ttu-id="8857b-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) pour gérer les objets UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="8857b-140">[**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects.</span></span>
-   <span data-ttu-id="8857b-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) pour exposer des propriétés et identifier les filtres appropriés pour les éléments dans la source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="8857b-141">[**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) to expose properties and identify appropriate filters for items in the Shell data source.</span></span>
-   <span data-ttu-id="8857b-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour filtrer les fichiers propriétaires ou pour énumérer et filtrer les fichiers stockés hiérarchiquement.</span><span class="sxs-lookup"><span data-stu-id="8857b-142">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span>

<span data-ttu-id="8857b-143">Outre les trois interfaces obligatoires répertoriées, les autres interfaces sont facultatives, et vous pouvez implémenter les interfaces facultatives les plus appropriées pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="8857b-143">Other than the three mandatory interfaces listed, the other interfaces are optional, and you are at liberty to implement whichever optional interfaces are most appropriate for the task at hand.</span></span>

### <a name="isearchprotocol-and-isearchprotocol2"></a><span data-ttu-id="8857b-144">ISearchProtocol et ISearchProtocol2</span><span class="sxs-lookup"><span data-stu-id="8857b-144">ISearchProtocol and ISearchProtocol2</span></span>

<span data-ttu-id="8857b-145">Les interfaces SearchProtocol initialisent et gèrent les objets UrlAccessor du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="8857b-145">The SearchProtocol interfaces initialize and manage your protocol handler UrlAccessor objects.</span></span> <span data-ttu-id="8857b-146">L’interface [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) est une extension facultative de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)et comprend une méthode supplémentaire pour spécifier des informations supplémentaires sur l’utilisateur et l’élément.</span><span class="sxs-lookup"><span data-stu-id="8857b-146">The [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) interface is an optional extension of [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol), and includes an extra method to specify more information about the user and the item.</span></span>

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a><span data-ttu-id="8857b-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3 et IUrlAccessor4</span><span class="sxs-lookup"><span data-stu-id="8857b-147">IUrlAccessor, IUrlAccessor2, IUrlAccessor3, and IUrlAccessor4</span></span>

<span data-ttu-id="8857b-148">Les interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8857b-148">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces are described in the following table.</span></span>



| <span data-ttu-id="8857b-149">Interface</span><span class="sxs-lookup"><span data-stu-id="8857b-149">Interface</span></span>                                                 | <span data-ttu-id="8857b-150">Description</span><span class="sxs-lookup"><span data-stu-id="8857b-150">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8857b-151">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="8857b-151">**IUrlAccessor**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | <span data-ttu-id="8857b-152">Pour une URL spécifiée, l’interface [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fournit l’accès aux propriétés de l’élément qui est exposé dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-152">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interface provides access to the properties of the item that is exposed in the URL.</span></span> <span data-ttu-id="8857b-153">Il peut également lier ces propriétés à un filtre propre au gestionnaire de protocole (autrement dit, un filtre autre que celui associé au nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="8857b-153">It can also bind those properties to a protocol handler-specific filter (that is, a filter other than the one associated with the file name).</span></span> |
| <span data-ttu-id="8857b-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="8857b-154">[**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional)</span></span> | <span data-ttu-id="8857b-155">L’interface [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) étend [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) avec des méthodes qui obtiennent une page de codes pour les propriétés de l’élément et son URL d’affichage, et qui obtiennent le type d’élément dans l’URL (document ou répertoire).</span><span class="sxs-lookup"><span data-stu-id="8857b-155">The [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) interface extends [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) with methods that get a code page for the item's properties and its display URL, and that get the type of item in the URL (document or directory).</span></span>                                    |
| <span data-ttu-id="8857b-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="8857b-156">[**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional)</span></span> | <span data-ttu-id="8857b-157">L’interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) étend [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) avec une méthode qui obtient un tableau de sid d’utilisateur, ce qui permet à l’hôte de protocole de recherche d’emprunter l’identité de ces utilisateurs pour indexer l’élément.</span><span class="sxs-lookup"><span data-stu-id="8857b-157">The [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface extends [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) with a method that gets an array of user SIDs, enabling the search protocol host to impersonate these users to index the item.</span></span>                                                      |
| <span data-ttu-id="8857b-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (facultatif)</span><span class="sxs-lookup"><span data-stu-id="8857b-158">[**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional)</span></span> | <span data-ttu-id="8857b-159">L’interface [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) étend les fonctionnalités de l’interface [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) avec une méthode qui détermine si le contenu de l’élément doit être indexé.</span><span class="sxs-lookup"><span data-stu-id="8857b-159">The [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) interface extends the functionality of the [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) interface with a method that identifies whether the content of the item should be indexed.</span></span>                                                                 |



 

<span data-ttu-id="8857b-160">L’objet UrlAccessor est instancié et initialisé par un objet SearchProtocol.</span><span class="sxs-lookup"><span data-stu-id="8857b-160">The UrlAccessor object is instantiated and initialized by a SearchProtocol object.</span></span> <span data-ttu-id="8857b-161">Les interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) fournissent un accès à des informations importantes par le biais des méthodes décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8857b-161">The [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) interfaces provide access to important pieces of information through the methods described in the following table.</span></span>



| <span data-ttu-id="8857b-162">Méthode</span><span class="sxs-lookup"><span data-stu-id="8857b-162">Method</span></span>                                                                                        | <span data-ttu-id="8857b-163">Description</span><span class="sxs-lookup"><span data-stu-id="8857b-163">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8857b-164">**IUrlAccessor::GetLastModified**</span><span class="sxs-lookup"><span data-stu-id="8857b-164">**IUrlAccessor::GetLastModified**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | <span data-ttu-id="8857b-165">Retourne l’heure de la dernière modification de l’URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-165">Returns the time that the URL was last modified.</span></span> <span data-ttu-id="8857b-166">Si cette heure est plus récente que la dernière fois que l’indexeur a traité cette URL, les gestionnaires de filtres (implémentations de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) sont appelés pour extraire (éventuellement) les données modifiées pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="8857b-166">If this time is more recent than the last time the indexer processed this URL, filter handlers (implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) are called to extract the (possibly) changed data for that item.</span></span> <span data-ttu-id="8857b-167">Les heures de modification des répertoires sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="8857b-167">Modified times for directories are ignored.</span></span> |
| [<span data-ttu-id="8857b-168">**IUrlAccessor::IsDirectory**</span><span class="sxs-lookup"><span data-stu-id="8857b-168">**IUrlAccessor::IsDirectory**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | <span data-ttu-id="8857b-169">Identifie si l’URL représente un dossier contenant des URL enfants.</span><span class="sxs-lookup"><span data-stu-id="8857b-169">Identifies whether the URL represents a folder containing a child URLs.</span></span>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="8857b-170">**IUrlAccessor::BindToStream**</span><span class="sxs-lookup"><span data-stu-id="8857b-170">**IUrlAccessor::BindToStream**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | <span data-ttu-id="8857b-171">Établit une liaison avec une [interface IStream](/windows/win32/api/objidl/nn-objidl-istream) qui représente les données d’un fichier dans un magasin de données personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8857b-171">Binds to an [IStream interface](/windows/win32/api/objidl/nn-objidl-istream) that represents the data of a file in a custom data store.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="8857b-172">**IUrlAccessor::BindToFilter**</span><span class="sxs-lookup"><span data-stu-id="8857b-172">**IUrlAccessor::BindToFilter**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | <span data-ttu-id="8857b-173">Crée une liaison avec un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)spécifique au gestionnaire de protocole, qui peut exposer des propriétés pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="8857b-173">Binds to a protocol handler-specific [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), which can expose properties for the item.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="8857b-174">**IUrlAccessor4::ShouldIndexItemContent**</span><span class="sxs-lookup"><span data-stu-id="8857b-174">**IUrlAccessor4::ShouldIndexItemContent**</span></span>](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | <span data-ttu-id="8857b-175">Indique si le contenu de l’élément doit être indexé.</span><span class="sxs-lookup"><span data-stu-id="8857b-175">Identifies whether the content of the item should be indexed.</span></span>                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a><span data-ttu-id="8857b-176">IProtocolHandlerSite</span><span class="sxs-lookup"><span data-stu-id="8857b-176">IProtocolHandlerSite</span></span>

<span data-ttu-id="8857b-177">L’interface [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) est utilisée pour instancier un gestionnaire de filtre, qui est hébergé dans un processus isolé.</span><span class="sxs-lookup"><span data-stu-id="8857b-177">The [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) interface is used to instantiate a filter handler, which is hosted in an isolated process.</span></span> <span data-ttu-id="8857b-178">Le gestionnaire de filtre approprié est obtenu pour un identificateur de classe persistante (CLSID), une classe de stockage de document ou une extension de nom de fichier spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8857b-178">The appropriate filter handler is obtained for a specified persistent class identifier (CLSID), document storage class, or file name extension.</span></span> <span data-ttu-id="8857b-179">L’avantage de demander au processus hôte de se lier à [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est que le processus hôte peut gérer le processus de localisation d’un gestionnaire de filtres approprié et contrôler la sécurité impliquée dans l’appel du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="8857b-179">The benefit of asking the host process to bind to [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is that the host process can manage the process of locating an appropriate filter handler, and control the security involved in calling the handler.</span></span>

## <a name="implementing-filter-handlers-for-containers"></a><span data-ttu-id="8857b-180">Implémentation de gestionnaires de filtres pour les conteneurs</span><span class="sxs-lookup"><span data-stu-id="8857b-180">Implementing Filter Handlers for Containers</span></span>

<span data-ttu-id="8857b-181">Si vous implémentez un gestionnaire de protocole hiérarchique, vous devez implémenter un gestionnaire de filtres pour un conteneur qui énumère les URL enfants.</span><span class="sxs-lookup"><span data-stu-id="8857b-181">If you are implementing a hierarchical protocol handler, then you must implement a filter handler for a container that enumerates child URLs.</span></span> <span data-ttu-id="8857b-182">Un gestionnaire de filtres est une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="8857b-182">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span> <span data-ttu-id="8857b-183">Le processus d’énumération est une boucle par le biais des méthodes [**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) et [**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) de l’interface **IFilter** ; chaque URL enfant est exposée comme valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="8857b-183">The enumeration process is a loop through the [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) and [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) methods of the **IFilter** interface; each child URL is exposed as the value of the property.</span></span>

<span data-ttu-id="8857b-184">[**IFilter :: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) retourne les propriétés du conteneur.</span><span class="sxs-lookup"><span data-stu-id="8857b-184">[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) returns the properties of the container.</span></span> <span data-ttu-id="8857b-185">Pour énumérer les URL enfants, **IFilter :: GetChunk** retourne l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8857b-185">To enumerate child URLs, **IFilter::GetChunk** returns either of the following:</span></span>

-   <span data-ttu-id="8857b-186">A-la [ \_ Rechercher \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="8857b-186">[PKEY\_Search\_UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):</span></span>

    <span data-ttu-id="8857b-187">URL de l’élément sans l’heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="8857b-187">The URL to the item without the last modified time.</span></span> <span data-ttu-id="8857b-188">[**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne un PROPVARIANT contenant l’URL enfant.</span><span class="sxs-lookup"><span data-stu-id="8857b-188">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing the child URL.</span></span>

-   <span data-ttu-id="8857b-189">A-la [ \_ Rechercher \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span><span class="sxs-lookup"><span data-stu-id="8857b-189">[PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):</span></span>

    <span data-ttu-id="8857b-190">L’URL et l’heure de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="8857b-190">The URL and the last modified time.</span></span> <span data-ttu-id="8857b-191">[**IFilter :: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) retourne un PROPVARIANT contenant un vecteur de l’URL enfant et de l’heure de la dernière modification.</span><span class="sxs-lookup"><span data-stu-id="8857b-191">[**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) returns a PROPVARIANT containing a vector of the child URL and the last modified time.</span></span>

<span data-ttu-id="8857b-192">Le retour de la [ \_ recherche de \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) est plus efficace, car l’indexeur peut déterminer immédiatement si l’élément doit être indexé sans appeler les méthodes [**ISearchProtocol :: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) et [**IUrlAccessor :: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .</span><span class="sxs-lookup"><span data-stu-id="8857b-192">Returning [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) and [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) methods.</span></span>

<span data-ttu-id="8857b-193">L’exemple de code suivant montre comment retourner la [propriété \_ \_ UrlToIndexWithModificationTime de recherche](../properties/props-system-search-urltoindexwithmodificationtime.md) de renvoi à la valeur.</span><span class="sxs-lookup"><span data-stu-id="8857b-193">The following example code demonstrates how to return the [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) property.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8857b-194">Copyright (c) Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="8857b-194">Copyright (c) Microsoft Corporation.</span></span> <span data-ttu-id="8857b-195">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="8857b-195">All rights reserved.</span></span>

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> <span data-ttu-id="8857b-196">Un composant [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) container doit toujours énumérer toutes les URL enfants, même si les URL enfants n’ont pas changé, car l’indexeur détecte les suppressions via le processus d’énumération.</span><span class="sxs-lookup"><span data-stu-id="8857b-196">A container [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) component should always enumerate all child URLs even if the child URLs have not changed, because the indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="8857b-197">Si la sortie de date dans [une \_ \_ UrlToIndexWithModificationTime de recherche](../properties/props-system-search-urltoindexwithmodificationtime.md) de la valeur de la variable indique que les données n’ont pas changé, l’indexeur ne met pas à jour les données de cette URL.</span><span class="sxs-lookup"><span data-stu-id="8857b-197">If the date output in a [PKEY\_Search\_UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

## <a name="installing-and-registering-a-protocol-handler"></a><span data-ttu-id="8857b-198">Installation et inscription d’un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-198">Installing and Registering a Protocol Handler</span></span>

<span data-ttu-id="8857b-199">L’installation de gestionnaires de protocole implique la copie de la ou des DLL vers un emplacement approprié dans le répertoire Program Files, puis l’inscription de la ou des DLL.</span><span class="sxs-lookup"><span data-stu-id="8857b-199">Installing protocol handlers involves copying the DLL(s) to an appropriate location in the Program Files directory, and then registering the DLL(s).</span></span> <span data-ttu-id="8857b-200">Les gestionnaires de protocole doivent implémenter l’inscription automatique pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="8857b-200">Protocol handlers should implement self-registration for installation.</span></span> <span data-ttu-id="8857b-201">L’application d’installation peut également ajouter une racine de recherche et des règles d’étendue pour définir une étendue d’analyse par défaut pour la source de données Shell, qui est décrite dans la section Vérification de l' [indexation de vos éléments](#ensuring-that-your-items-are-indexed) à la fin de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8857b-201">The installation application can also add a search root, and scope rules to define a default crawl scope for the Shell data source, which is discussed in [Ensuring that Your Items are Indexed](#ensuring-that-your-items-are-indexed) at the end of this topic.</span></span>

### <a name="guidelines-for-registering-a-protocol-handler"></a><span data-ttu-id="8857b-202">Instructions pour l’inscription d’un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-202">Guidelines for Registering a Protocol Handler</span></span>

<span data-ttu-id="8857b-203">Vous devez suivre ces instructions lors de l’inscription d’un gestionnaire de protocole :</span><span class="sxs-lookup"><span data-stu-id="8857b-203">You should follow these guidelines when registering a protocol handler:</span></span>

-   <span data-ttu-id="8857b-204">Le programme d’installation doit utiliser le programme d’installation EXE ou MSI.</span><span class="sxs-lookup"><span data-stu-id="8857b-204">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="8857b-205">Des notes de publication doivent être fournies.</span><span class="sxs-lookup"><span data-stu-id="8857b-205">Release notes must be provided.</span></span>
-   <span data-ttu-id="8857b-206">Une entrée ajout/suppression de programmes doit être créée pour chaque complément installé.</span><span class="sxs-lookup"><span data-stu-id="8857b-206">An Add/Remove Programs entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="8857b-207">Le programme d’installation doit prendre en charge tous les paramètres du Registre pour le type de fichier spécifique ou le magasin que le complément actuel comprend.</span><span class="sxs-lookup"><span data-stu-id="8857b-207">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="8857b-208">Si un complément précédent est remplacé, le programme d’installation doit avertir l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8857b-208">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="8857b-209">Si un complément plus récent a remplacé le complément précédent, il doit être possible de restaurer les fonctionnalités précédentes du complément et de faire de nouveau le complément par défaut pour ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="8857b-209">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>
-   <span data-ttu-id="8857b-210">Le programme d’installation doit définir une étendue d’analyse par défaut pour l’indexeur en ajoutant une racine de recherche et des règles d’étendue à l’aide du gestionnaire de la portée d’analyse (CSM).</span><span class="sxs-lookup"><span data-stu-id="8857b-210">The installer should define a default crawl scope for the indexer by adding a search root, and scope rules using the Crawl Scope Manager (CSM).</span></span>

### <a name="registering-a-protocol-handler"></a><span data-ttu-id="8857b-211">Inscription d’un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-211">Registering a Protocol Handler</span></span>

<span data-ttu-id="8857b-212">Vous devez faire quatorze entrées dans le registre pour inscrire le composant de gestionnaire de protocole, où :</span><span class="sxs-lookup"><span data-stu-id="8857b-212">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="8857b-213">*Ver \_ IND \_ ProgID* est le ProgID indépendant de la version de l’implémentation du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="8857b-213">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="8857b-214">*Ver \_ L' \_ identificateur* de programme DEP est le ProgID dépendant de la version de l’implémentation du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="8857b-214">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation.</span></span>
-   <span data-ttu-id="8857b-215">*CLSID \_ 1* est le CLSID de l’implémentation du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="8857b-215">*CLSID\_1* is the CLSID of the protocol handler implementation.</span></span>

<span data-ttu-id="8857b-216">**Pour inscrire un gestionnaire de protocole :**</span><span class="sxs-lookup"><span data-stu-id="8857b-216">**To register a protocol handler:**</span></span>

1.  <span data-ttu-id="8857b-217">Enregistrez le ProgID indépendant de la version avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8857b-217">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="8857b-218">Enregistrez le ProgID dépendant de la version avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8857b-218">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="8857b-219">Enregistrez le CLSID du gestionnaire de protocole avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8857b-219">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  <span data-ttu-id="8857b-220">Inscrire le gestionnaire de protocole auprès de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="8857b-220">Register the protocol handler with Windows Search.</span></span> <span data-ttu-id="8857b-221">Dans l’exemple suivant, <Protocol Name> est le nom du Protocole lui-même, tel que fichier, MAPI, etc. :</span><span class="sxs-lookup"><span data-stu-id="8857b-221">In the following example, <Protocol Name> is the name of the protocol itself, such as file, mapi, and so forth:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    <span data-ttu-id="8857b-222">Avant Windows Vista :</span><span class="sxs-lookup"><span data-stu-id="8857b-222">Prior to Windows Vista:</span></span>

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a><span data-ttu-id="8857b-223">Inscription du gestionnaire de type de fichier du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-223">Registering the Protocol Handler's File Type Handler</span></span>

<span data-ttu-id="8857b-224">Vous devez créer deux entrées dans le registre pour inscrire le gestionnaire de type de fichier du gestionnaire de protocole (qui est également appelé extension d’interpréteur de commandes).</span><span class="sxs-lookup"><span data-stu-id="8857b-224">You need to make two entries in the registry to register the protocol handler's file type handler (which is also known as a Shell extension).</span></span>

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a><span data-ttu-id="8857b-225">Vérification de l’indexation de vos éléments</span><span class="sxs-lookup"><span data-stu-id="8857b-225">Ensuring that Your Items are Indexed</span></span>

<span data-ttu-id="8857b-226">Une fois que vous avez implémenté votre gestionnaire de protocole, vous devez spécifier les éléments de Shell que votre gestionnaire de protocole doit indexer.</span><span class="sxs-lookup"><span data-stu-id="8857b-226">After you have implemented your protocol handler, you must specify which Shell items your protocol handler is to index.</span></span> <span data-ttu-id="8857b-227">Vous pouvez utiliser le gestionnaire de catalogue pour lancer la réindexation (pour plus d’informations, consultez [utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md)).</span><span class="sxs-lookup"><span data-stu-id="8857b-227">You can use the Catalog Manager to initiate re-indexing (for more information, see [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md)).</span></span> <span data-ttu-id="8857b-228">Vous pouvez également utiliser le gestionnaire de portée d’analyse (CSM) pour configurer les règles par défaut indiquant les URL que vous souhaitez que l’indexeur analyse (pour plus d’informations, consultez [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md) et [gestion des règles d’étendue](-search-3x-wds-extidx-csm-scoperules.md)).</span><span class="sxs-lookup"><span data-stu-id="8857b-228">Or you can also use the Crawl Scope Manager (CSM) to set up default rules indicating the URLs that you want the indexer to crawl (for more information, see [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md) and [Managing Scope Rules](-search-3x-wds-extidx-csm-scoperules.md)).</span></span> <span data-ttu-id="8857b-229">Vous pouvez également ajouter une racine de recherche (pour plus d’informations, consultez [gestion des racines de recherche](-search-3x-wds-extidx-csm-searchroots.md)).</span><span class="sxs-lookup"><span data-stu-id="8857b-229">You can also add a search root (for more information, see [Managing Search Roots](-search-3x-wds-extidx-csm-searchroots.md)).</span></span> <span data-ttu-id="8857b-230">Une autre option consiste à suivre la procédure décrite dans l’exemple réindexer des [exemples du kit de développement logiciel (SDK) Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="8857b-230">Another option available to you is to follow the procedure in the ReIndex sample in [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="8857b-231">L’interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fournit des méthodes qui informent le moteur de recherche des conteneurs à l’analyse et/ou à la surveillance, et les éléments sous ces conteneurs à inclure ou exclure lors de l’analyse ou de la surveillance.</span><span class="sxs-lookup"><span data-stu-id="8857b-231">The [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) interface provides methods that notify the search engine of containers to crawl and/or watch, and items under those containers to include or exclude when crawling or watching.</span></span> <span data-ttu-id="8857b-232">Dans Windows 7 et versions ultérieures, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) étend **ISearchCrawlScopeManager** avec la méthode [**ISearchCrawlScopeManager2 :: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) qui obtient la version, qui informe les clients si l’état de l’CSM a changé.</span><span class="sxs-lookup"><span data-stu-id="8857b-232">In Windows 7 and later, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extends **ISearchCrawlScopeManager** with the [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) method that gets the version, which informs clients whether the state of the CSM has changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8857b-233">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8857b-233">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8857b-234">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8857b-234">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8857b-235">Fonctionnement des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-235">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="8857b-236">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-236">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="8857b-237">Notification de l’index des modifications</span><span class="sxs-lookup"><span data-stu-id="8857b-237">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="8857b-238">Ajout d’icônes et de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="8857b-238">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="8857b-239">Exemple de code : extensions de Shell pour les gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-239">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="8857b-240">Création d’un connecteur de recherche pour un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-240">Creating a Search Connector for a Protocol Handler</span></span>](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[<span data-ttu-id="8857b-241">Débogage de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="8857b-241">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
