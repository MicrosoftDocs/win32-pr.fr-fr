---
title: Implémentation d’un gestionnaire de protocole pour WDS
description: La création d’un gestionnaire de protocole implique l’implémentation de ISearchProtocol pour gérer des objets UrlAccessor, IUrlAccessor pour générer des métadonnées sur et pour identifier les filtres appropriés pour les éléments dans le magasin de données, IProtocolHandlerSite pour instancier un objet SearchProtocol et identifier les filtres appropriés, et IFilterto filtrer les fichiers propriétaires ou pour énumérer et filtrer les fichiers stockés de manière hiérarchique.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101537"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="65bf5-103">Implémentation d’un gestionnaire de protocole pour WDS</span><span class="sxs-lookup"><span data-stu-id="65bf5-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="65bf5-104">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="65bf5-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="65bf5-105">Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="65bf5-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="65bf5-106">La création d’un gestionnaire de protocole implique l’implémentation de [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) pour gérer des objets UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) pour générer des métadonnées sur et pour identifier les filtres appropriés pour les éléments dans le magasin de données, IProtocolHandlerSite pour instancier un objet SearchProtocol et identifier les filtres appropriés, et [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)pour filtrer des fichiers propriétaires ou pour énumérer et filtrer des fichiers stockés de manière hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="65bf5-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="65bf5-107">Le gestionnaire de protocole doit être multithread.</span><span class="sxs-lookup"><span data-stu-id="65bf5-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="65bf5-108">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="65bf5-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="65bf5-109">Remarque sur les URL</span><span class="sxs-lookup"><span data-stu-id="65bf5-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="65bf5-110">Interfaces du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="65bf5-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="65bf5-111">IFilters pour conteneurs</span><span class="sxs-lookup"><span data-stu-id="65bf5-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="65bf5-112">Ajout de la fonctionnalité options du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="65bf5-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="65bf5-113">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="65bf5-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="65bf5-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65bf5-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="65bf5-115">Remarque sur les URL</span><span class="sxs-lookup"><span data-stu-id="65bf5-115">Note on URLs</span></span>

<span data-ttu-id="65bf5-116">Microsoft Windows Desktop Search (WDS) utilise des URL pour identifier de manière unique les éléments dans un système de fichiers, à l’intérieur d’un magasin de base de données ou sur le Web.</span><span class="sxs-lookup"><span data-stu-id="65bf5-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="65bf5-117">Une URL qui définit un nœud d’entrée est appelée page de démarrage ; WDS commence à cette page de démarrage et analyse de manière récursive le magasin de données.</span><span class="sxs-lookup"><span data-stu-id="65bf5-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="65bf5-118">La structure d’URL standard est la suivante :</span><span class="sxs-lookup"><span data-stu-id="65bf5-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="65bf5-119">Lorsque vous souhaitez ajouter un nouveau magasin de données, vous devez sélectionner un nom pour l’identifier, qui n’est pas en conflit avec les nouveaux.</span><span class="sxs-lookup"><span data-stu-id="65bf5-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="65bf5-120">Nous recommandons cette Convention d’affectation de noms : companyName. Scheme.</span><span class="sxs-lookup"><span data-stu-id="65bf5-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="65bf5-121">Interfaces du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="65bf5-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="65bf5-122">**ISearchProtocol**</span><span class="sxs-lookup"><span data-stu-id="65bf5-122">**ISearchProtocol**</span></span>

<span data-ttu-id="65bf5-123">L’interface [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) appelle, initialise et gère les objets UrlAccessor.</span><span class="sxs-lookup"><span data-stu-id="65bf5-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="65bf5-124">Pour plus d’informations sur l’implémentation de l’interface ISearchProtocol, consultez Référence de l' **interface ISearchProtocol**.</span><span class="sxs-lookup"><span data-stu-id="65bf5-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="65bf5-125">**IUrlAccessor**</span><span class="sxs-lookup"><span data-stu-id="65bf5-125">**IUrlAccessor**</span></span>

<span data-ttu-id="65bf5-126">Pour une URL spécifiée, l’interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) génère des métadonnées sur la structure d’emplacement ainsi que des éléments contenus, et lie ces éléments à un filtre.</span><span class="sxs-lookup"><span data-stu-id="65bf5-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="65bf5-127">L’objet **IUrlAccessor** est instancié et initialisé par un objet SearchProtocol ; Toutefois, vous pouvez également implémenter une méthode d’initialisation interne afin que votre objet **IUrlAccessor** puisse effectuer des tâches d’initialisation spécifiques à votre gestionnaire de protocole, telles que la validation de l’URL pour un élément faisant l’objet d’un accès ou la vérification de l’heure de dernière modification pour déterminer si un fichier doit être traité dans l’analyse en cours.</span><span class="sxs-lookup"><span data-stu-id="65bf5-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="65bf5-128">Les heures de modification des répertoires sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="65bf5-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="65bf5-129">L’objet [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) doit énumérer les objets enfants pour déterminer s’il y a eu des modifications ou des suppressions.</span><span class="sxs-lookup"><span data-stu-id="65bf5-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="65bf5-130">Une grande partie de la conception de l’objet **UrlAccessor** dépend de l’ordre hiérarchique ou basé sur les liens de la structure.</span><span class="sxs-lookup"><span data-stu-id="65bf5-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="65bf5-131">Pour les magasins de données hiérarchiques, l’objet **UrlAccessor** doit trouver un filtre qui peut énumérer son contenu.</span><span class="sxs-lookup"><span data-stu-id="65bf5-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="65bf5-132">Une autre différence entre les gestionnaires de protocoles hiérarchiques et basés sur les liaisons est l’utilisation de la méthode IsDirectory.</span><span class="sxs-lookup"><span data-stu-id="65bf5-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="65bf5-133">Dans les gestionnaires de protocole basés sur des liens, cette méthode doit retourner S \_ false.</span><span class="sxs-lookup"><span data-stu-id="65bf5-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="65bf5-134">Les gestionnaires de protocole hiérarchiques doivent retourner S \_ OK pour les conteneurs.</span><span class="sxs-lookup"><span data-stu-id="65bf5-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="65bf5-135">Pour obtenir des instructions supplémentaires sur l’implémentation d’une interface [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , consultez la référence de l' [**interface IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .</span><span class="sxs-lookup"><span data-stu-id="65bf5-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="65bf5-136">**IProtocolHandlerSite**</span><span class="sxs-lookup"><span data-stu-id="65bf5-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="65bf5-137">Cette interface est utilisée pour instancier un objet **SearchProtocol** et fournit également l’objet **UrlAccessor** avec un filtre approprié pour un ID de classe (CLSID) spécifié.</span><span class="sxs-lookup"><span data-stu-id="65bf5-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="65bf5-138">IFilters pour conteneurs</span><span class="sxs-lookup"><span data-stu-id="65bf5-138">IFilters for Containers</span></span>

<span data-ttu-id="65bf5-139">Si vous implémentez un gestionnaire de protocole hiérarchique, vous devez implémenter un composant conteneur [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)qui énumère les URL représentant des conteneurs ou des dossiers.</span><span class="sxs-lookup"><span data-stu-id="65bf5-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="65bf5-140">Le processus d’énumération est une boucle par le biais des méthodes **GetChunk** et **GetValue** de l’interface IFilter qui retournent une liste d’URL représentant chaque élément dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="65bf5-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="65bf5-141">En premier lieu, **GetChunk** retourne un FULLPROSPEC avec le jeu de propriétés Gather \_ PROPSET et l’un ou l’autre des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="65bf5-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="65bf5-142">PID \_ GTHR \_ DIRLINK, URL de l’élément sans l’heure de la dernière modification, ou</span><span class="sxs-lookup"><span data-stu-id="65bf5-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="65bf5-143">PID \_ GTHR \_ DIRLINK \_ avec \_ Time, URL avec l’heure de la dernière modification</span><span class="sxs-lookup"><span data-stu-id="65bf5-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="65bf5-144">Le GUID du jeu de propriétés pour la collecte \_ PROPSET est 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span><span class="sxs-lookup"><span data-stu-id="65bf5-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="65bf5-145">La propriété PROPSPEC est un PID \_ GTHR \_ DIRLINK = 2 ou un PID \_ GTHR \_ DIRLINK \_ avec \_ Time = 12 Decimal.</span><span class="sxs-lookup"><span data-stu-id="65bf5-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="65bf5-146">Le retour \_ d’un PID GTHR \_ DIRLINK \_ avec \_ Time est plus efficace, car l’indexeur peut déterminer immédiatement si l’élément doit être indexé sans appeler les méthodes ISearchProtocol->CreateUrlAccessor () et IUrlAccessor->GetLastModified ().</span><span class="sxs-lookup"><span data-stu-id="65bf5-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="65bf5-147">La méthode **GetValue** retourne alors un PROPVARIANT pour l’URL (et l’heure de dernière modification, si elle est utilisée), comme suit :</span><span class="sxs-lookup"><span data-stu-id="65bf5-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="65bf5-148">VT \_ LPWStr, URL de l’élément enfant, ou</span><span class="sxs-lookup"><span data-stu-id="65bf5-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="65bf5-149">Vecteur de l’URL suivi d’un FILETIME</span><span class="sxs-lookup"><span data-stu-id="65bf5-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="65bf5-150">L’exemple de code suivant montre comment créer le PID \_ GTHR \_ DIRLINK approprié \_ avec \_ Time.</span><span class="sxs-lookup"><span data-stu-id="65bf5-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="65bf5-151">**CE CODE ET CES INFORMATIONS SONT FOURNIS « EN L’ÉTAT », SANS GARANTIE D’AUCUNE SORTE, EXPRESSE OU IMPLICITE, Y COMPRIS, MAIS SANS S’Y LIMITER, LES GARANTIES IMPLICITES DE QUALITÉ MARCHANDE ET/OU D’ADÉQUATION À UN USAGE PARTICULIER.**</span><span class="sxs-lookup"><span data-stu-id="65bf5-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="65bf5-152">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="65bf5-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="65bf5-153">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="65bf5-153">All rights reserved.</span></span>

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> <span data-ttu-id="65bf5-154">Un composant [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)container doit toujours énumérer toutes les URL enfants, même si les URL enfants n’ont pas changé, car l’indexeur détecte les suppressions via le processus d’énumération.</span><span class="sxs-lookup"><span data-stu-id="65bf5-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="65bf5-155">Si la sortie de date dans un répertoire de \_ liens \_ avec \_ l’heure indique que les données n’ont pas changé, l’indexeur ne met pas à jour les données de cette URL.</span><span class="sxs-lookup"><span data-stu-id="65bf5-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="65bf5-156">L’URL physique est l’URL que l’objet **UrlAccessor** traite.</span><span class="sxs-lookup"><span data-stu-id="65bf5-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="65bf5-157">Si le filtre n’émet pas de DisplayUrl convivial, WDS affiche l’URL physique à l’utilisateur dans le cadre des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="65bf5-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="65bf5-158">Le schéma WDS contient deux propriétés pour contrôler ce qui est affiché à l’utilisateur final, comme indiqué dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="65bf5-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="65bf5-159">GUID</span><span class="sxs-lookup"><span data-stu-id="65bf5-159">GUID</span></span>                                 | <span data-ttu-id="65bf5-160">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="65bf5-160">PROPSPEC</span></span>      | <span data-ttu-id="65bf5-161">Description</span><span class="sxs-lookup"><span data-stu-id="65bf5-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="65bf5-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="65bf5-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="65bf5-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="65bf5-163">DisplayFolder</span></span> | <span data-ttu-id="65bf5-164">Chemin de dossier affiché à l’utilisateur dans les résultats de la recherche</span><span class="sxs-lookup"><span data-stu-id="65bf5-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="65bf5-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="65bf5-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="65bf5-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="65bf5-166">FolderName</span></span>    | <span data-ttu-id="65bf5-167">Nom complet du dossier parent</span><span class="sxs-lookup"><span data-stu-id="65bf5-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="65bf5-168">Si votre code n’émet pas de DisplayFolder ou NomDossier, ces valeurs sont calculées à partir du DisplayUrl.</span><span class="sxs-lookup"><span data-stu-id="65bf5-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="65bf5-169">Les barres obliques dans l’URL désignent des conteneurs dans le magasin ou le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="65bf5-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="65bf5-170">Ajout de la fonctionnalité options du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="65bf5-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="65bf5-171">Pour que votre gestionnaire de protocole ait une page de démarrage par défaut (et une URL de nœud d’entrée), vous devez implémenter l’interface **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="65bf5-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="65bf5-172">Dans les versions ultérieures de WDS, cette interface fournit des raccordements à la boîte de dialogue Options pour une expérience utilisateur améliorée.</span><span class="sxs-lookup"><span data-stu-id="65bf5-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="65bf5-173">Cette interface fournit les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="65bf5-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="65bf5-174">Détermine si les exigences de votre gestionnaire de protocole sont satisfaites.</span><span class="sxs-lookup"><span data-stu-id="65bf5-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="65bf5-175">Par exemple, le magasin de votre gestionnaire de protocole peut nécessiter l’accès à une application donnée pour indexer correctement les données de l’application, mais cette application n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="65bf5-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="65bf5-176">Identifie la configuration minimale requise pour que votre gestionnaire de protocole doive traiter un élément.</span><span class="sxs-lookup"><span data-stu-id="65bf5-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="65bf5-177">Les spécifications peuvent être exprimées dans une description conviviale et localisée, telle que « Microsoft Outlook 2000 ou une version ultérieure ».</span><span class="sxs-lookup"><span data-stu-id="65bf5-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="65bf5-178">Définit les URL que votre gestionnaire de protocole doit traiter par défaut.</span><span class="sxs-lookup"><span data-stu-id="65bf5-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="65bf5-179">ISearchProtocolOptions</span><span class="sxs-lookup"><span data-stu-id="65bf5-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="65bf5-180">Le tableau suivant décrit les méthodes que vous devez implémenter pour l’interface **ISearchProtocolOptions** .</span><span class="sxs-lookup"><span data-stu-id="65bf5-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="65bf5-181">Méthode</span><span class="sxs-lookup"><span data-stu-id="65bf5-181">Method</span></span>               | <span data-ttu-id="65bf5-182">Description</span><span class="sxs-lookup"><span data-stu-id="65bf5-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65bf5-183">CheckRequirements</span><span class="sxs-lookup"><span data-stu-id="65bf5-183">CheckRequirements</span></span>    | <span data-ttu-id="65bf5-184">Détermine si la configuration minimale requise pour un gestionnaire de protocole personnalisé est remplie</span><span class="sxs-lookup"><span data-stu-id="65bf5-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="65bf5-185">GetDefaultCrawlScope</span><span class="sxs-lookup"><span data-stu-id="65bf5-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="65bf5-186">Retourne une liste d’URL par défaut dans un magasin spécifié pour un gestionnaire de protocole personnalisé</span><span class="sxs-lookup"><span data-stu-id="65bf5-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="65bf5-187">GetRequirements</span><span class="sxs-lookup"><span data-stu-id="65bf5-187">GetRequirements</span></span>      | <span data-ttu-id="65bf5-188">Identifie une description conviviale et localisée de la configuration minimale requise pour un gestionnaire de protocole personnalisé</span><span class="sxs-lookup"><span data-stu-id="65bf5-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="65bf5-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="65bf5-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="65bf5-190">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="65bf5-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="65bf5-191">Notification de l’index des modifications</span><span class="sxs-lookup"><span data-stu-id="65bf5-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="65bf5-192">Ajout d’icônes, d’aperçus et de menus contextuels avec des extensions de Shell</span><span class="sxs-lookup"><span data-stu-id="65bf5-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="65bf5-193">Installation et inscription de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="65bf5-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 