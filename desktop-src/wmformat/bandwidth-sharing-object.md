---
title: Objet de partage de bande passante
description: Objet de partage de bande passante
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media Format SDK, objets de partage de bande passante
- ASF (Advanced Systems Format), objets de partage de bande passante
- ASF (format de systèmes avancés), objets de partage de bande passante
- objets, objets de partage de bande passante
- partage de bande passante, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381531"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="8bb94-108">Objet de partage de bande passante</span><span class="sxs-lookup"><span data-stu-id="8bb94-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="8bb94-109">Un objet de partage de bande passante est utilisé pour indiquer que deux flux ou plus, indépendamment de leurs vitesses de transmission individuelles, n’utiliseront jamais plus d’une quantité de bande passante spécifiée entre eux.</span><span class="sxs-lookup"><span data-stu-id="8bb94-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="8bb94-110">Il s’agit d’un objet purement informatif. les vitesses de transmission définies dans cet ensemble ne sont pas appliquées par programmation par un objet de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="8bb94-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="8bb94-111">Les informations de partage de bande passante sont une partie facultative d’un profil.</span><span class="sxs-lookup"><span data-stu-id="8bb94-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="8bb94-112">Les objets de partage de bande passante peuvent être créés pour les informations de partage de bande passante existantes dans un profil ou peuvent être créés vides, prêts à recevoir de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="8bb94-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="8bb94-113">Les objets de partage de bande passante ne peuvent pas exister indépendamment d’un objet de profil.</span><span class="sxs-lookup"><span data-stu-id="8bb94-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="8bb94-114">Pour enregistrer le contenu d’un objet de partage de bande passante, vous devez appeler [**IWMProfile3 :: AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span><span class="sxs-lookup"><span data-stu-id="8bb94-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="8bb94-115">Pour créer un objet de partage de bande passante, appelez l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8bb94-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="8bb94-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="8bb94-116">Method</span></span>                                                                                  | <span data-ttu-id="8bb94-117">Description</span><span class="sxs-lookup"><span data-stu-id="8bb94-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8bb94-118">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="8bb94-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="8bb94-119">Crée un objet de partage de bande passante sans aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="8bb94-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="8bb94-120">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="8bb94-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="8bb94-121">Crée un objet de partage de bande passante rempli avec les données d’un profil.</span><span class="sxs-lookup"><span data-stu-id="8bb94-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="8bb94-122">Utilise l’index de partage de bande passante pour identifier les informations de partage de bande passante souhaitées.</span><span class="sxs-lookup"><span data-stu-id="8bb94-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="8bb94-123">Les deux méthodes du tableau précédent définissent un pointeur vers une interface **IWMBandwidthSharing** .</span><span class="sxs-lookup"><span data-stu-id="8bb94-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="8bb94-124">L’interface **IWMStreamList** est héritée par **IWMBandwidthSharing**. il n’est donc pas nécessaire d’appeler **QueryInterface** avec cet objet.</span><span class="sxs-lookup"><span data-stu-id="8bb94-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="8bb94-125">Les interfaces suivantes sont prises en charge par chaque objet de partage de bande passante.</span><span class="sxs-lookup"><span data-stu-id="8bb94-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="8bb94-126">Interface</span><span class="sxs-lookup"><span data-stu-id="8bb94-126">Interface</span></span>                                          | <span data-ttu-id="8bb94-127">Description</span><span class="sxs-lookup"><span data-stu-id="8bb94-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="8bb94-128">**IWMBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="8bb94-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="8bb94-129">Gère les propriétés d’un groupe de flux qui partageront la bande passante.</span><span class="sxs-lookup"><span data-stu-id="8bb94-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="8bb94-130">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="8bb94-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="8bb94-131">Gère la liste des flux qui partageront la bande passante.</span><span class="sxs-lookup"><span data-stu-id="8bb94-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="8bb94-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bb94-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bb94-133">**Partage de bande passante**</span><span class="sxs-lookup"><span data-stu-id="8bb94-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="8bb94-134">**Gestionnaire de profils, objet**</span><span class="sxs-lookup"><span data-stu-id="8bb94-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="8bb94-135">**Profile (objet)**</span><span class="sxs-lookup"><span data-stu-id="8bb94-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 




