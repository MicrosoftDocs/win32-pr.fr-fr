---
title: Obtention et définition des métadonnées et des attributs
description: Obtention et définition des métadonnées et des attributs
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Gestionnaire de périphériques Windows Media, attributs
- Gestionnaire de périphériques, attributs
- applications de bureau, attributs
- fournisseurs de services, attributs
- Guide de programmation, attributs
- attributs
- Gestionnaire de périphériques Windows Media, métadonnées
- Gestionnaire de périphériques, métadonnées
- applications de bureau, métadonnées
- fournisseurs de services, métadonnées
- Guide de programmation, métadonnées
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8697f62dac44f5aab4b08aa4f6c516ac35a17e4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840234"
---
# <a name="getting-and-setting-metadata-and-attributes"></a><span data-ttu-id="e2ab0-115">Obtention et définition des métadonnées et des attributs</span><span class="sxs-lookup"><span data-stu-id="e2ab0-115">Getting and Setting Metadata and Attributes</span></span>

<span data-ttu-id="e2ab0-116">Une application peut obtenir deux types d’informations sur un stockage ou un appareil : les attributs et les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-116">An application can get two kinds of information about a storage or device: attributes and metadata.</span></span> <span data-ttu-id="e2ab0-117">Les attributs sont des valeurs booléennes plus simples qui décrivent généralement les informations du système de fichiers, par exemple si un stockage a des objets enfants, s’il peut être renommé, lu ou supprimé, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-117">Attributes are simpler Boolean values that generally describe file system information, such as whether a storage has child objects, whether it can be renamed, read, or deleted, and so on.</span></span> <span data-ttu-id="e2ab0-118">Les attributs sont récupérés en tant que valeurs d’indicateurs en appelant [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2 :: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span><span class="sxs-lookup"><span data-stu-id="e2ab0-118">Attributes are retrieved as flags values by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) or [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2).</span></span> <span data-ttu-id="e2ab0-119">Les attributs sont définis en appelant [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="e2ab0-119">Attributes are set by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span>

<span data-ttu-id="e2ab0-120">Une application peut également demander des données plus complexes (numériques, de chaîne ou d’autres types de données) en tant que *métadonnées*.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-120">An application can also request more complex data (numeric, string, or other data types) as *metadata*.</span></span> <span data-ttu-id="e2ab0-121">Les valeurs de métadonnées sont identifiées par des noms de chaîne uniques.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-121">Metadata values are identified by unique string names.</span></span> <span data-ttu-id="e2ab0-122">Windows Media Gestionnaire de périphériques définit une liste de constantes de chaîne qui peuvent être utilisées pour demander des valeurs. ces valeurs définies sont répertoriées dans [constantes de métadonnées](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2ab0-122">Windows Media Device Manager defines a list of string constants that can be used to request values; these defined values are listed in [Metadata Constants](metadata-constants.md).</span></span> <span data-ttu-id="e2ab0-123">Un fournisseur de services peut définir ses propres constantes, mais une application appelante doit être consciente de ces définitions pour pouvoir demander ou définir ces valeurs de métadonnées personnalisées.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-123">A service provider can define its own constants, but a calling application must be aware of these definitions in order to request or set these custom metadata values.</span></span> <span data-ttu-id="e2ab0-124">L’application demande des métadonnées en appelant [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="e2ab0-124">The application requests metadata by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span>

<span data-ttu-id="e2ab0-125">L’un des aspects importants de l’obtention et de la définition des métadonnées et des attributs est de savoir où proviennent les valeurs récupérées.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-125">An important aspect of getting and setting metadata and attributes is understanding where the retrieved values come from.</span></span> <span data-ttu-id="e2ab0-126">Le fournisseur de services ou l’appareil peut récupérer ces valeurs à partir de différents emplacements, y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e2ab0-126">The service provider or the device can get these values from many different places, including the following:</span></span>

-   <span data-ttu-id="e2ab0-127">À partir de l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-127">From the file header.</span></span> <span data-ttu-id="e2ab0-128">Par exemple, dans un fichier ASF, la vitesse de transmission est stockée dans l’en-tête de fichier.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-128">For example, in an ASF file, the bit rate is stored in the file header.</span></span>
-   <span data-ttu-id="e2ab0-129">À partir de valeurs définies explicitement par l’application lors de l’appel d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-129">From values set explicitly by the application when calling a method.</span></span> <span data-ttu-id="e2ab0-130">Ces valeurs peuvent être enregistrées dans un magasin de métadonnées externe dans le fournisseur de services ou l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-130">These values may be saved in an external metadata store in the service provider or the device.</span></span> <span data-ttu-id="e2ab0-131">Ce magasin peut ou non persister quand l’appareil se déconnecte ou s’éteint.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-131">This store may or may not persist when the device disconnects or turns off.</span></span> <span data-ttu-id="e2ab0-132">Par exemple, les évaluations nombre de lecture et étoile de l’utilisateur sont généralement stockées dans des magasins externes sur l’ordinateur ou l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-132">For example, the play count and user star ratings are typically stored in external stores on the computer or device.</span></span>
-   <span data-ttu-id="e2ab0-133">En examinant les informations fournies par le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-133">By examining information provided by the file system.</span></span> <span data-ttu-id="e2ab0-134">Par exemple, si un fichier est en lecture seule ou si un dossier a des enfants.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-134">For example, whether a file is read-only or whether a folder has children.</span></span>
-   <span data-ttu-id="e2ab0-135">En ouvrant et en analysant les données de fichier.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-135">By opening and parsing the file data.</span></span>

<span data-ttu-id="e2ab0-136">Il est important de se rendre compte qu’une propriété peut être stockée dans plusieurs emplacements (dans l’en-tête de fichier et également dans un magasin local), et qu’elle peut être modifiable ou non.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-136">It is important to realize that a property might be stored in more than one location (within the file header and also in a local store), and that it may or may not be editable.</span></span> <span data-ttu-id="e2ab0-137">Par exemple, la modification d’une description de fichier peut ou non être persistante ; Si le fournisseur de services stocke la description localement, elle ne sera pas conservée sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-137">For example, changing a file description may or may not be persistent; if the service provider stores the description locally, it will not persist on the device.</span></span> <span data-ttu-id="e2ab0-138">De même, si la description de fichier est extraite de l’en-tête de fichier, sa modification est persistante uniquement si le fournisseur de services ou l’appareil ouvre et modifie les données d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-138">Similarly, if the file description is taken from the file header, modifying this will only be persistent if the service provider or device opens and modifies the header data.</span></span> <span data-ttu-id="e2ab0-139">La plupart des applications font une meilleure tentative en modifiant les valeurs souhaitées, mais ne dépendent pas des propriétés qui doivent être modifiées de manière permanente.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-139">Most applications make a best attempt by changing desired values, but do not depend on any properties to be persistently changed.</span></span>

<span data-ttu-id="e2ab0-140">Pour plus d’informations sur l’obtention et la définition des valeurs, reportez-vous aux sections appropriées pour les développeurs d’applications et les développeurs de fournisseurs de services, plus loin dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="e2ab0-140">More information on getting and setting values is given in the appropriate sections for application developers and service provider developers later in the documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2ab0-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e2ab0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2ab0-142">**Tâches communes aux applications et aux fournisseurs de services**</span><span class="sxs-lookup"><span data-stu-id="e2ab0-142">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




