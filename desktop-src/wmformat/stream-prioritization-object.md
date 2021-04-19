---
title: Objet de priorité de flux
description: Objet de priorité de flux
ms.assetid: cb0345ce-6847-435b-8cbb-f8b93856af9f
keywords:
- Windows Media Format SDK, objets de priorité de flux
- ASF (Advanced Systems Format), objets de définition de priorités de flux
- ASF (format des systèmes avancés), objets de priorité de flux
- objets, objets de priorité de flux
- objets de priorité de flux
- flux, objets de priorité de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cce4189f64e85cca4e0d649dbc00409cf9d7c06
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106511274"
---
# <a name="stream-prioritization-object"></a><span data-ttu-id="5041c-109">Objet de priorité de flux</span><span class="sxs-lookup"><span data-stu-id="5041c-109">Stream Prioritization Object</span></span>

<span data-ttu-id="5041c-110">Un objet de priorité de flux est utilisé pour spécifier un ordre d’importance pour les flux dans un profil.</span><span class="sxs-lookup"><span data-stu-id="5041c-110">A stream prioritization object is used to specify an order of importance for the streams in a profile.</span></span> <span data-ttu-id="5041c-111">Lorsque la lecture complète n’est pas possible en raison de limitations de la vitesse de transmission, les flux de priorité les plus faibles sont les premiers à être supprimés.</span><span class="sxs-lookup"><span data-stu-id="5041c-111">When full playback is not possible due to bit-rate limitations, the lowest priority streams will be the first to be dropped.</span></span>

<span data-ttu-id="5041c-112">Vous pouvez créer des objets de définition de priorités de flux pour les données de priorité de flux existantes dans un profil ou vous pouvez les créer vides, prêts à recevoir de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="5041c-112">Stream prioritization objects can be created for existing stream prioritization data in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="5041c-113">Les objets de définition de priorités de flux ne peuvent pas exister indépendamment d’un objet de profil.</span><span class="sxs-lookup"><span data-stu-id="5041c-113">Stream prioritization objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="5041c-114">Pour enregistrer le contenu d’un objet de priorité de flux, vous devez appeler [**IWMProfile3 :: SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span><span class="sxs-lookup"><span data-stu-id="5041c-114">To save the contents of a stream prioritization object, you must call [**IWMProfile3::SetStreamPrioritization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization).</span></span> <span data-ttu-id="5041c-115">Pour créer un objet de définition de priorités de flux, utilisez l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="5041c-115">To create a stream prioritization object, use one of the following methods.</span></span>



| <span data-ttu-id="5041c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="5041c-116">Method</span></span>                                                                                          | <span data-ttu-id="5041c-117">Description</span><span class="sxs-lookup"><span data-stu-id="5041c-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="5041c-118">**IWMProfile3::CreateNewStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="5041c-118">**IWMProfile3::CreateNewStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization) | <span data-ttu-id="5041c-119">Crée un objet de priorité de flux sans aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="5041c-119">Creates a stream prioritization object without any data.</span></span>                     |
| [<span data-ttu-id="5041c-120">**IWMProfile3::GetStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="5041c-120">**IWMProfile3::GetStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization)             | <span data-ttu-id="5041c-121">Crée un objet de priorité de flux rempli avec les données du profil.</span><span class="sxs-lookup"><span data-stu-id="5041c-121">Creates a stream prioritization object populated with data from the profile.</span></span> |



 

<span data-ttu-id="5041c-122">Les deux méthodes du tableau précédent définissent un pointeur vers une interface **IWMStreamPrioritization** .</span><span class="sxs-lookup"><span data-stu-id="5041c-122">Both methods in the preceding table set a pointer to an **IWMStreamPrioritization** interface.</span></span> <span data-ttu-id="5041c-123">Il s’agit de la seule interface prise en charge par l’objet de définition de priorités des flux.</span><span class="sxs-lookup"><span data-stu-id="5041c-123">This is the only interface supported by the stream prioritization object.</span></span>



| <span data-ttu-id="5041c-124">Interface</span><span class="sxs-lookup"><span data-stu-id="5041c-124">Interface</span></span>                                                  | <span data-ttu-id="5041c-125">Description</span><span class="sxs-lookup"><span data-stu-id="5041c-125">Description</span></span>                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="5041c-126">**IWMStreamPrioritization**</span><span class="sxs-lookup"><span data-stu-id="5041c-126">**IWMStreamPrioritization**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization) | <span data-ttu-id="5041c-127">Gère la liste des flux au sein de l’objet de définition de priorités des flux.</span><span class="sxs-lookup"><span data-stu-id="5041c-127">Manages the list of streams within the stream prioritization object.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5041c-128">Notes</span><span class="sxs-lookup"><span data-stu-id="5041c-128">Remarks</span></span>

<span data-ttu-id="5041c-129">Une seule priorité de flux de données peut exister pour un profil donné.</span><span class="sxs-lookup"><span data-stu-id="5041c-129">Only one stream prioritization can exist for a given profile.</span></span> <span data-ttu-id="5041c-130">Si vous créez une nouvelle définition de priorités de flux pour un profil qui contient déjà une priorité de flux, l’ancienne est supprimée.</span><span class="sxs-lookup"><span data-stu-id="5041c-130">If you create a new stream prioritization for a profile that already contains a stream prioritization, the old one will be deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5041c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5041c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5041c-132">**Objets**</span><span class="sxs-lookup"><span data-stu-id="5041c-132">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="5041c-133">**Profile (objet)**</span><span class="sxs-lookup"><span data-stu-id="5041c-133">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="5041c-134">**Utilisation de la hiérarchisation des flux**</span><span class="sxs-lookup"><span data-stu-id="5041c-134">**Using Stream Prioritization**</span></span>](using-stream-prioritization.md)
</dt> </dl>

 

 




