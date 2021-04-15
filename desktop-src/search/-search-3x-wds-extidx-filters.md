---
description: Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Meilleures pratiques pour les gestionnaires de filtres dans Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544992e252d9ec0e3a7c402d1c348d3e3bfa9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525539"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a><span data-ttu-id="cff3a-103">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="cff3a-103">Best Practices for Creating Filter Handlers in Windows Search</span></span>

<span data-ttu-id="cff3a-104">Microsoft Windows Search utilise des filtres pour extraire le contenu des éléments à inclure dans un index de recherche en texte intégral.</span><span class="sxs-lookup"><span data-stu-id="cff3a-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="cff3a-105">Vous pouvez étendre Windows Search pour indexer les types de fichiers nouveaux ou propriétaires en écrivant des gestionnaires de filtres pour extraire le contenu et les gestionnaires de propriétés pour extraire les propriétés des fichiers.</span><span class="sxs-lookup"><span data-stu-id="cff3a-105">You can extend Windows Search to index new or proprietary file types by writing filter handlers to extract the content, and property handlers to extract the properties of files.</span></span> <span data-ttu-id="cff3a-106">Les filtres sont associés à des types de fichiers, tels qu’ils sont dénotés par des extensions de nom de fichier, des types MIME ou des identificateurs de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="cff3a-106">Filters are associated with file types, as denoted by file name extensions, MIME types or class identifiers (CLSIDs).</span></span> <span data-ttu-id="cff3a-107">Alors qu’un filtre peut gérer plusieurs types de fichiers, chaque type fonctionne avec un seul filtre.</span><span class="sxs-lookup"><span data-stu-id="cff3a-107">While one filter can handle multiple file types, each type works with only one filter.</span></span>

<span data-ttu-id="cff3a-108">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="cff3a-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="cff3a-109">Code natif</span><span class="sxs-lookup"><span data-stu-id="cff3a-109">Native Code</span></span>](#native-code)
-   [<span data-ttu-id="cff3a-110">Pratiques de code sécurisé pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="cff3a-110">Secure Code Practices for Windows Search</span></span>](#secure-code-practices-for-windows-search)
-   [<span data-ttu-id="cff3a-111">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cff3a-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="cff3a-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cff3a-112">Related topics</span></span>](#related-topics)

## <a name="native-code"></a><span data-ttu-id="cff3a-113">Code natif</span><span class="sxs-lookup"><span data-stu-id="cff3a-113">Native Code</span></span>

<span data-ttu-id="cff3a-114">Dans Windows 7 et versions ultérieures, les filtres écrits en code managé sont bloqués explicitement.</span><span class="sxs-lookup"><span data-stu-id="cff3a-114">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="cff3a-115">Les filtres doivent être écrits en code natif en raison des éventuels problèmes de versioning du CLR avec le processus dans lequel plusieurs compléments s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="cff3a-115">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

## <a name="secure-code-practices-for-windows-search"></a><span data-ttu-id="cff3a-116">Pratiques de code sécurisé pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="cff3a-116">Secure Code Practices for Windows Search</span></span>

<span data-ttu-id="cff3a-117">Voici quelques pratiques pour écrire des applications sécurisées pour une utilisation avec Windows Search.</span><span class="sxs-lookup"><span data-stu-id="cff3a-117">The following are practices for writing secure applications for use with Windows Search.</span></span>

<span data-ttu-id="cff3a-118">**Pour les applications de requête :**</span><span class="sxs-lookup"><span data-stu-id="cff3a-118">**For query applications:**</span></span>

-   <span data-ttu-id="cff3a-119">Lorsque vous écrivez des clients de recherche, vous devez choisir l’API qui s’exécute dans un contexte de sécurité qui permet à l’utilisateur de disposer des privilèges minimum.</span><span class="sxs-lookup"><span data-stu-id="cff3a-119">When writing search clients, you should choose the API that runs in a security context that allows the user the least privilege.</span></span> <span data-ttu-id="cff3a-120">Par exemple, les pages ASP peuvent utiliser l’objet de requête IXSSO, qui s’exécute en tant que processus utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cff3a-120">For example, ASP pages can use the IXSSO query object, which runs as a user process.</span></span>

<span data-ttu-id="cff3a-121">**Pour les IFilters et les ressources de langue :**</span><span class="sxs-lookup"><span data-stu-id="cff3a-121">**For IFilters and Language Resources:**</span></span>

-   <span data-ttu-id="cff3a-122">Si un nouveau gestionnaire de filtres pour un type de fichier est en cours d’installation en remplacement d’une inscription de filtre existante, le programme d’installation doit enregistrer l’inscription actuelle et la restaurer si le nouveau gestionnaire de filtres est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="cff3a-122">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="cff3a-123">Il n’existe aucun mécanisme pour la chaîne de filtres.</span><span class="sxs-lookup"><span data-stu-id="cff3a-123">There is no mechanism to chain filters.</span></span> <span data-ttu-id="cff3a-124">Par conséquent, le nouveau gestionnaire de filtres est chargé de répliquer toutes les fonctionnalités nécessaires de l’ancien filtre.</span><span class="sxs-lookup"><span data-stu-id="cff3a-124">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>
-   <span data-ttu-id="cff3a-125">Les IFilters, les analyseurs lexicaux et les générateurs de formes dérivées pour Windows Search s’exécutent dans le contexte de sécurité local.</span><span class="sxs-lookup"><span data-stu-id="cff3a-125">IFilters, word breakers, and stemmers for Windows Search run in the Local Security context.</span></span> <span data-ttu-id="cff3a-126">Elles doivent être écrites pour gérer les mémoires tampons et les empiler correctement.</span><span class="sxs-lookup"><span data-stu-id="cff3a-126">They should be written to manage buffers and to stack correctly.</span></span> <span data-ttu-id="cff3a-127">Toutes les copies de chaînes doivent avoir des vérifications explicites pour se protéger contre les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cff3a-127">All string copies must have explicit checks to guard against buffer overruns.</span></span> <span data-ttu-id="cff3a-128">Vous devez toujours vérifier la taille allouée de la mémoire tampon et tester la taille des données en fonction de la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cff3a-128">You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.</span></span> <span data-ttu-id="cff3a-129">Les dépassements de mémoire tampon sont une technique courante pour exploiter du code qui n’applique pas les restrictions de taille de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cff3a-129">Buffer overruns are a common technique for exploiting code that does not enforce buffer size restrictions.</span></span>
-   <span data-ttu-id="cff3a-130">Les composants [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), analyseur lexical et générateur de formes dérivées ne doivent jamais appeler la fonction de [fonction EXITPROCESS](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ou une API similaire qui termine un processus et tous ses threads.</span><span class="sxs-lookup"><span data-stu-id="cff3a-130">[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), word breaker and stemmer components should never call the [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function or similar API that terminates a process and all its threads.</span></span>
-   <span data-ttu-id="cff3a-131">N’allouez pas ou ne libérez pas de ressources dans le point d’entrée DllMain.</span><span class="sxs-lookup"><span data-stu-id="cff3a-131">Do not allocate or free resources in the DllMain entry point.</span></span> <span data-ttu-id="cff3a-132">Cela peut entraîner des échecs lors des tests de contrainte de faible ressource.</span><span class="sxs-lookup"><span data-stu-id="cff3a-132">This can lead to failures during low-resource stress tests.</span></span>
-   <span data-ttu-id="cff3a-133">Coder tous les objets pour qu’ils soient thread-safe.</span><span class="sxs-lookup"><span data-stu-id="cff3a-133">Code all objects to be thread-safe.</span></span> <span data-ttu-id="cff3a-134">Windows Search appelle une instance de l’analyseur lexical ou du générateur de formes dérivées dans un thread à la fois, mais il peut appeler plusieurs instances en même temps sur plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="cff3a-134">Windows Search calls any one instance of a word breaker or stemmer in one thread at a time, but it may call multiple instances at the same time across multiple threads.</span></span>
-   <span data-ttu-id="cff3a-135">Évitez de créer des fichiers temporaires ou d’écrire dans le registre.</span><span class="sxs-lookup"><span data-stu-id="cff3a-135">Avoid creating temporary files or writing to the registry.</span></span>
-   <span data-ttu-id="cff3a-136">Si vous utilisez le compilateur Microsoft Visual C++, veillez à compiler votre application à l’aide de l’option **/GS** .</span><span class="sxs-lookup"><span data-stu-id="cff3a-136">If you use the Microsoft Visual C++ compiler, ensure that you compile your application using the **/GS** option.</span></span> <span data-ttu-id="cff3a-137">L’option **/GS** est utilisée pour détecter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cff3a-137">The **/GS** option is used to detect buffer overruns.</span></span> <span data-ttu-id="cff3a-138">L’option/GS place les contrôles de sécurité dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="cff3a-138">The /GS option places security checks into the compiled code.</span></span> <span data-ttu-id="cff3a-139">Pour plus d’informations, consultez [fonction DllGetClassObject](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (vérification de la sécurité de la mémoire tampon) dans la section Options du compilateur Visual C++ du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="cff3a-139">For more information, see [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx) /**GS** (Buffer Security Check) in the Visual C++ Compiler Options section of the Platform SDK.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cff3a-140">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cff3a-140">Additional Resources</span></span>

-   <span data-ttu-id="cff3a-141">L’exemple [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) montre comment créer une classe de base IFilter pour implémenter l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="cff3a-141">The [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
-   <span data-ttu-id="cff3a-142">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cff3a-142">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
-   <span data-ttu-id="cff3a-143">Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="cff3a-143">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
-   <span data-ttu-id="cff3a-144">Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cff3a-144">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cff3a-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cff3a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff3a-146">Développement de gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="cff3a-146">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
</dt> <dt>

[<span data-ttu-id="cff3a-147">À propos des gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="cff3a-147">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
</dt> <dt>

[<span data-ttu-id="cff3a-148">Retour des propriétés d’un gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="cff3a-148">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
</dt> <dt>

[<span data-ttu-id="cff3a-149">Gestionnaires de filtres fournis avec Windows</span><span class="sxs-lookup"><span data-stu-id="cff3a-149">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
</dt> <dt>

[<span data-ttu-id="cff3a-150">Implémentation de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="cff3a-150">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
</dt> <dt>

[<span data-ttu-id="cff3a-151">Inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="cff3a-151">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
</dt> <dt>

[<span data-ttu-id="cff3a-152">Test des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="cff3a-152">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
