---
title: Configuration de flux, objet
description: Configuration de flux, objet
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Kit de développement logiciel (SDK) Windows Media format, objets de configuration de flux
- ASF (Advanced Systems Format), objets de configuration de flux
- ASF (format de systèmes avancés), objets de configuration de flux
- objets, objets de configuration de flux
- objets de configuration de flux
- flux, objets de configuration de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101348"
---
# <a name="stream-configuration-object"></a><span data-ttu-id="c514d-109">Configuration de flux, objet</span><span class="sxs-lookup"><span data-stu-id="c514d-109">Stream Configuration Object</span></span>

<span data-ttu-id="c514d-110">Un objet de configuration de flux est utilisé pour spécifier les propriétés d’un flux de média dans un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="c514d-110">A stream configuration object is used to specify the properties of a media stream in an ASF file.</span></span> <span data-ttu-id="c514d-111">Il est possible de créer des objets de configuration de flux pour des flux existants dans un profil ou de les créer vides, prêts à recevoir de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="c514d-111">Stream configuration objects can be created for existing streams in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="c514d-112">Les objets de configuration de flux ne peuvent pas exister indépendamment d’un objet de profil.</span><span class="sxs-lookup"><span data-stu-id="c514d-112">Stream configuration objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="c514d-113">Pour enregistrer le contenu d’un objet de configuration de flux, vous devez appeler [**IWMProfile :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) pour ajouter un nouveau flux ou [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) pour enregistrer les modifications apportées à un flux existant.</span><span class="sxs-lookup"><span data-stu-id="c514d-113">To save the contents of a stream configuration object, you must call either [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) to add a new stream or [**IWMProfile::ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) to save changes made to an existing stream.</span></span>

<span data-ttu-id="c514d-114">Pour créer un objet de configuration de flux, utilisez l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c514d-114">To create a stream configuration object, use one of the following methods.</span></span>



| <span data-ttu-id="c514d-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="c514d-115">Method</span></span>                                                                | <span data-ttu-id="c514d-116">Description</span><span class="sxs-lookup"><span data-stu-id="c514d-116">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c514d-117">**IWMProfile::CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="c514d-117">**IWMProfile::CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | <span data-ttu-id="c514d-118">Crée un objet de configuration de flux sans aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="c514d-118">Creates a stream configuration object without any data.</span></span>                                                                          |
| [<span data-ttu-id="c514d-119">**IWMProfile :: GetStream**</span><span class="sxs-lookup"><span data-stu-id="c514d-119">**IWMProfile::GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | <span data-ttu-id="c514d-120">Crée un objet de configuration de flux rempli avec les données d’un profil.</span><span class="sxs-lookup"><span data-stu-id="c514d-120">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="c514d-121">Utilise l’index de flux pour identifier le flux souhaité.</span><span class="sxs-lookup"><span data-stu-id="c514d-121">Uses the stream index to identify the desired stream.</span></span>  |
| [<span data-ttu-id="c514d-122">**IWMProfile::GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="c514d-122">**IWMProfile::GetStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | <span data-ttu-id="c514d-123">Crée un objet de configuration de flux rempli avec les données d’un profil.</span><span class="sxs-lookup"><span data-stu-id="c514d-123">Creates a stream configuration object populated with data from a profile.</span></span> <span data-ttu-id="c514d-124">Utilise le numéro de flux pour identifier le flux souhaité.</span><span class="sxs-lookup"><span data-stu-id="c514d-124">Uses the stream number to identify the desired stream.</span></span> |



 

<span data-ttu-id="c514d-125">Toutes les méthodes du tableau précédent définissent un pointeur vers une interface **IWMStreamConfig** .</span><span class="sxs-lookup"><span data-stu-id="c514d-125">All of the methods in the preceding table set a pointer to an **IWMStreamConfig** interface.</span></span> <span data-ttu-id="c514d-126">Les autres interfaces de l’objet de configuration Stream peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="c514d-126">The other interfaces of the stream configuration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="c514d-127">Les interfaces suivantes sont prises en charge par l’objet de configuration de flux.</span><span class="sxs-lookup"><span data-stu-id="c514d-127">The following interfaces are supported by the stream configuration object.</span></span>



| <span data-ttu-id="c514d-128">Interface</span><span class="sxs-lookup"><span data-stu-id="c514d-128">Interface</span></span>                                        | <span data-ttu-id="c514d-129">Description</span><span class="sxs-lookup"><span data-stu-id="c514d-129">Description</span></span>                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c514d-130">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="c514d-130">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="c514d-131">Définit et récupère la structure [**du \_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le flux.</span><span class="sxs-lookup"><span data-stu-id="c514d-131">Sets and retrieves the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream.</span></span>                                    |
| [<span data-ttu-id="c514d-132">**IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="c514d-132">**IWMPropertyVault**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | <span data-ttu-id="c514d-133">Définit et récupère les propriétés qui ne sont pas requises pour tous les flux, comme les paramètres de vitesse de transmission variable (VBR).</span><span class="sxs-lookup"><span data-stu-id="c514d-133">Sets and retrieves properties that are not required for all streams, like variable bit rate (VBR) settings.</span></span>                  |
| [<span data-ttu-id="c514d-134">**IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="c514d-134">**IWMStreamConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | <span data-ttu-id="c514d-135">Définit et récupère toutes les informations de base relatives à un flux.</span><span class="sxs-lookup"><span data-stu-id="c514d-135">Sets and retrieves all of the basic information about a stream.</span></span>                                                              |
| [<span data-ttu-id="c514d-136">**IWMStreamConfig2**</span><span class="sxs-lookup"><span data-stu-id="c514d-136">**IWMStreamConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | <span data-ttu-id="c514d-137">Configure les types d’extensions d’unité de données associées au flux.</span><span class="sxs-lookup"><span data-stu-id="c514d-137">Configures the types of data unit extensions associated with the stream.</span></span> <span data-ttu-id="c514d-138">Hérite de toutes les méthodes de **IWMStreamConfig**.</span><span class="sxs-lookup"><span data-stu-id="c514d-138">Inherits all of the methods of **IWMStreamConfig**.</span></span> |
| [<span data-ttu-id="c514d-139">**IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="c514d-139">**IWMStreamConfig3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | <span data-ttu-id="c514d-140">Définit et récupère la langue du flux.</span><span class="sxs-lookup"><span data-stu-id="c514d-140">Sets and retrieves the language for the stream.</span></span> <span data-ttu-id="c514d-141">Hérite de toutes les méthodes de **IWMStreamConfig** et **IWMStreamConfig2**.</span><span class="sxs-lookup"><span data-stu-id="c514d-141">Inherits all of the methods of **IWMStreamConfig** and **IWMStreamConfig2**.</span></span> |
| [<span data-ttu-id="c514d-142">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="c514d-142">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="c514d-143">Gère les propriétés d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c514d-143">Manages the properties of a video stream.</span></span> <span data-ttu-id="c514d-144">Il s’agit d’une interface facultative qui est disponible uniquement pour les flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="c514d-144">This is an optional interface, and is available only for video streams.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="c514d-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c514d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c514d-146">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="c514d-146">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="c514d-147">**Objets**</span><span class="sxs-lookup"><span data-stu-id="c514d-147">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="c514d-148">**Gestionnaire de profils, objet**</span><span class="sxs-lookup"><span data-stu-id="c514d-148">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




