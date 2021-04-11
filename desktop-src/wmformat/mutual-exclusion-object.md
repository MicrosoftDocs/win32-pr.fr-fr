---
title: Objet d’exclusion mutuelle
description: Objet d’exclusion mutuelle
ms.assetid: dd1f7865-e409-4bf9-9fa0-769a29eaed60
keywords:
- Windows Media Format SDK, objets d’exclusion mutuelle
- ASF (Advanced Systems Format), objets d’exclusion mutuelle
- ASF (format des systèmes avancés), objets d’exclusion mutuelle
- objets, objets d’exclusion mutuelle
- exclusion mutuelle, objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8522b66f82bd88479b8c7b1d0d0b45bd038fdab3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101332"
---
# <a name="mutual-exclusion-object"></a><span data-ttu-id="1df6d-108">Objet d’exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="1df6d-108">Mutual Exclusion Object</span></span>

<span data-ttu-id="1df6d-109">Un objet d’exclusion mutuelle est utilisé pour spécifier un certain nombre de flux, dont un seul peut être remis à la fois.</span><span class="sxs-lookup"><span data-stu-id="1df6d-109">A mutual exclusion object is used to specify a number of streams, of which only one can be delivered at a time.</span></span> <span data-ttu-id="1df6d-110">Cela peut être utilisé de plusieurs façons, par exemple en fournissant un flux audio dans plusieurs langues en tant que piste audio pour un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="1df6d-110">This can be used in several ways, such as providing an audio stream in several languages as the soundtrack for one video stream.</span></span>

<span data-ttu-id="1df6d-111">L’exclusion mutuelle est une partie facultative d’un profil.</span><span class="sxs-lookup"><span data-stu-id="1df6d-111">Mutual exclusion is an optional part of a profile.</span></span> <span data-ttu-id="1df6d-112">Des objets d’exclusion mutuelle peuvent être créés pour des informations d’exclusion mutuelle existantes dans un profil ou peuvent être créés vides, prêts à recevoir de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="1df6d-112">Mutual exclusion objects can be created for existing mutual exclusion information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="1df6d-113">Les objets d’exclusion mutuelle ne peuvent pas exister indépendamment d’un objet de profil.</span><span class="sxs-lookup"><span data-stu-id="1df6d-113">Mutual exclusion objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="1df6d-114">Pour enregistrer le contenu d’un objet d’exclusion mutuelle, vous devez appeler [**IWMProfile :: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="1df6d-114">To save the contents of a mutual exclusion object, you must call [**IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).</span></span>

<span data-ttu-id="1df6d-115">Pour créer un objet d’exclusion mutuelle, utilisez l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1df6d-115">To create a mutual exclusion object, use one of the following methods.</span></span>



| <span data-ttu-id="1df6d-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="1df6d-116">Method</span></span>                                                                              | <span data-ttu-id="1df6d-117">Description</span><span class="sxs-lookup"><span data-stu-id="1df6d-117">Description</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1df6d-118">**IWMProfile::CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="1df6d-118">**IWMProfile::CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="1df6d-119">Crée un objet d’exclusion mutuelle sans aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="1df6d-119">Creates a mutual exclusion object without any data.</span></span>                                                                                                         |
| [<span data-ttu-id="1df6d-120">**IWMProfile::GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="1df6d-120">**IWMProfile::GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="1df6d-121">Crée un objet d’exclusion mutuelle rempli avec les données d’un profil.</span><span class="sxs-lookup"><span data-stu-id="1df6d-121">Creates a mutual exclusion object populated with data from a profile.</span></span> <span data-ttu-id="1df6d-122">Utilise l’index d’exclusion mutuelle pour identifier les informations d’exclusion mutuelle souhaitées.</span><span class="sxs-lookup"><span data-stu-id="1df6d-122">Uses the mutual exclusion index to identify the desired mutual exclusion information.</span></span> |



 

<span data-ttu-id="1df6d-123">Les deux méthodes du tableau précédent définissent un pointeur vers une interface **IWMMutualExclusion** .</span><span class="sxs-lookup"><span data-stu-id="1df6d-123">Both methods in the preceding table set a pointer to an **IWMMutualExclusion** interface.</span></span> <span data-ttu-id="1df6d-124">L’interface **IWMStreamList** est héritée par **IWMMutualExclusion** et n’a jamais besoin d’être accessible directement.</span><span class="sxs-lookup"><span data-stu-id="1df6d-124">The **IWMStreamList** interface is inherited by **IWMMutualExclusion** and never needs to be accessed directly.</span></span> <span data-ttu-id="1df6d-125">L’autre interface de l’objet d’exclusion mutuelle peut être obtenue en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="1df6d-125">The other interface of the mutual exclusion object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="1df6d-126">Les interfaces suivantes sont prises en charge par chaque objet d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="1df6d-126">The following interfaces are supported by every mutual exclusion object.</span></span>



| <span data-ttu-id="1df6d-127">Interface</span><span class="sxs-lookup"><span data-stu-id="1df6d-127">Interface</span></span>                                          | <span data-ttu-id="1df6d-128">Description</span><span class="sxs-lookup"><span data-stu-id="1df6d-128">Description</span></span>                                                                                                                                            |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1df6d-129">**IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="1df6d-129">**IWMMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)   | <span data-ttu-id="1df6d-130">Définit et récupère le type d’exclusion mutuelle à utiliser.</span><span class="sxs-lookup"><span data-stu-id="1df6d-130">Sets and retrieves the type of mutual exclusion to be used.</span></span>                                                                                            |
| [<span data-ttu-id="1df6d-131">**IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="1df6d-131">**IWMMutualExclusion2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) | <span data-ttu-id="1df6d-132">Organise les flux en enregistrements, qui peuvent être utilisés pour créer des scénarios d’exclusion mutuelle complexes.</span><span class="sxs-lookup"><span data-stu-id="1df6d-132">Organizes streams into records, which can be used to create complex mutual exclusion scenarios.</span></span> <span data-ttu-id="1df6d-133">Hérite de toutes les méthodes de **IWMMutualExclusion**.</span><span class="sxs-lookup"><span data-stu-id="1df6d-133">Inherits all of the methods of **IWMMutualExclusion**.</span></span> |
| [<span data-ttu-id="1df6d-134">**IWMStreamList**</span><span class="sxs-lookup"><span data-stu-id="1df6d-134">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="1df6d-135">Gère la liste des flux qui s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="1df6d-135">Manages the list of mutually exclusive streams.</span></span>                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="1df6d-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1df6d-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1df6d-137">**Exclusion mutuelle**</span><span class="sxs-lookup"><span data-stu-id="1df6d-137">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="1df6d-138">**Objets**</span><span class="sxs-lookup"><span data-stu-id="1df6d-138">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="1df6d-139">**Gestionnaire de profils, objet**</span><span class="sxs-lookup"><span data-stu-id="1df6d-139">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> </dl>

 

 




