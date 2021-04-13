---
title: Accès aux métadonnées et aux attributs dans l’application
description: Obtention et définition des métadonnées et des attributs dans l’application
ms.assetid: 308a722d-1c65-41eb-a0e2-21171eb410d5
keywords:
- Gestionnaire de périphériques Windows Media, métadonnées
- Gestionnaire de périphériques, métadonnées
- Guide de programmation, métadonnées
- applications de bureau, métadonnées
- création d’applications Windows Media Gestionnaire de périphériques, de métadonnées
- metadata
- Gestionnaire de périphériques Windows Media, attributs
- Gestionnaire de périphériques, attributs
- Guide de programmation, attributs
- applications de bureau, attributs
- création d’applications Windows Media Gestionnaire de périphériques, attributs
- attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a78dbb31ebcc5ec99b1db3503b386b09b5a3c05
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104313852"
---
# <a name="accessing-metadata-and-attributes-in-the-app"></a><span data-ttu-id="aa64c-115">Accès aux métadonnées et aux attributs dans l’application</span><span class="sxs-lookup"><span data-stu-id="aa64c-115">Accessing metadata and attributes in the app</span></span>

<span data-ttu-id="aa64c-116">Une discussion générale sur les métadonnées et les attributs est disponible dans [obtention et définition des métadonnées et des attributs](getting-and-setting-metadata-and-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="aa64c-116">A general discussion of metadata and attributes is available in [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md).</span></span> <span data-ttu-id="aa64c-117">Cette section traite des appels de méthode d’application spécifiques pour extraire ou définir des valeurs.</span><span class="sxs-lookup"><span data-stu-id="aa64c-117">This section covers specific application method calls to retrieve or set values.</span></span>

<span data-ttu-id="aa64c-118">Les applications peuvent récupérer des attributs ou des métadonnées sur un stockage spécifique en appelant [**IWMDMStorage :: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2 :: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3 :: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4 :: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span><span class="sxs-lookup"><span data-stu-id="aa64c-118">Applications can retrieve attributes or metadata about a specific storage by calling [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes), [**IWMDMStorage2::GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2), [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).</span></span> <span data-ttu-id="aa64c-119">**GetMetadata** récupère une collection complète de toutes les métadonnées associées à un stockage, et l’application peut ensuite énumérer toutes les valeurs ou demander des valeurs spécifiques de la collection.</span><span class="sxs-lookup"><span data-stu-id="aa64c-119">**GetMetadata** retrieves a full collection of all the metadata associated with a storage, and the application can then enumerate through all values or request specific values from the collection.</span></span> <span data-ttu-id="aa64c-120">**GetSpecifiedMetadata** crée un objet de métadonnées pour le compte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="aa64c-120">**GetSpecifiedMetadata** creates a metadata object on behalf of the caller.</span></span> <span data-ttu-id="aa64c-121">L’appelant peut demander un sous-ensemble des données disponibles en remplissant le paramètre *ppwszPropNames* avec un tableau des chaînes de propriétés de gestionnaire de périphériques Windows Media souhaitées, ainsi que le nombre de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="aa64c-121">The caller may request a subset of the available data by filling in the *ppwszPropNames* parameter with an array of the desired Windows Media Device Manager property strings, and the count of that array.</span></span> <span data-ttu-id="aa64c-122">L’objet de métadonnées retourné sera rempli avec les propriétés qui peuvent être récupérées.</span><span class="sxs-lookup"><span data-stu-id="aa64c-122">The returned metadata object will be filled with those properties that could be retrieved.</span></span> <span data-ttu-id="aa64c-123">Les propriétés qui n’ont pas pu être récupérées seront absentes.</span><span class="sxs-lookup"><span data-stu-id="aa64c-123">Those properties that couldn't be retrieved will be absent.</span></span> <span data-ttu-id="aa64c-124">Les métadonnées sont retournées en fonction du meilleur effort.</span><span class="sxs-lookup"><span data-stu-id="aa64c-124">Metadata is returned on a best-effort basis.</span></span>

<span data-ttu-id="aa64c-125">Un appareil peut définir des attributs ou des métadonnées sur un stockage en appelant [**IWMDMStorage :: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2 :: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)ou [**IWMDMStorage3 :: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span><span class="sxs-lookup"><span data-stu-id="aa64c-125">A device can set attributes or metadata on a storage by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes), [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2), or [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).</span></span> <span data-ttu-id="aa64c-126">Notez qu’il n’y a aucune garantie que les valeurs définies sont conservées, car elles peuvent être stockées dans un magasin de fichiers externes non persistant, les valeurs peuvent ne pas être prises en charge ou l’appareil peut ne pas prendre en charge les propriétés comme étant accessibles en écriture.</span><span class="sxs-lookup"><span data-stu-id="aa64c-126">Note that there is no guarantee that any values set will persist, because they may be stored in a non-persistent external file store, the values may not be supported, or, the device may not support the properties as writeable.</span></span>

<span data-ttu-id="aa64c-127">Vous pouvez également obtenir ou définir les métadonnées relatives à un appareil en appelant [**IWMDMDevice3 :: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) ou [**IWMDMDevice3 :: SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span><span class="sxs-lookup"><span data-stu-id="aa64c-127">You can also get or set metadata about a device by calling [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) or [**IWMDMDevice3::SetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-setproperty).</span></span> <span data-ttu-id="aa64c-128">Une table distincte de constantes de métadonnées d’appareil est indiquée à la fin des [constantes de métadonnées](metadata-constants.md).</span><span class="sxs-lookup"><span data-stu-id="aa64c-128">There is a separate table of device metadata constants listed at the end of [Metadata Constants](metadata-constants.md).</span></span>

<span data-ttu-id="aa64c-129">Des exemples d’utilisation de ces méthodes sont fournis dans la documentation de référence de chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="aa64c-129">Examples of using these methods are given in each method's reference documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa64c-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa64c-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa64c-131">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="aa64c-131">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="aa64c-132">**Obtention et définition des métadonnées et des attributs**</span><span class="sxs-lookup"><span data-stu-id="aa64c-132">**Getting and Setting Metadata and Attributes**</span></span>](getting-and-setting-metadata-and-attributes.md)
</dt> </dl>

 

 




