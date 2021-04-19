---
title: Gestionnaire de profils, objet
description: Gestionnaire de profils, objet
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media Format SDK, objets du gestionnaire de profils
- ASF (Advanced Systems Format), objets du gestionnaire de profils
- ASF (format des systèmes avancés), objets du gestionnaire de profils
- objets, objets du gestionnaire de profils
- profils, objets
- profils, objets du gestionnaire de profils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "106511670"
---
# <a name="profile-manager-object"></a><span data-ttu-id="01292-109">Gestionnaire de profils, objet</span><span class="sxs-lookup"><span data-stu-id="01292-109">Profile Manager Object</span></span>

<span data-ttu-id="01292-110">Un profil est un ensemble de paramètres multimédias utilisés pour créer un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="01292-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="01292-111">L’objet gestionnaire de profils crée des objets de profil pour la modification.</span><span class="sxs-lookup"><span data-stu-id="01292-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="01292-112">Les objets de profil peuvent être créés sans aucune donnée ni être généré à partir de données de profil existantes.</span><span class="sxs-lookup"><span data-stu-id="01292-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="01292-113">L’objet gestionnaire de profils fournit également des méthodes pour l’énumération des codecs pris en charge et l’interrogation de ces codecs pour obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="01292-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="01292-114">L’objet gestionnaire de profils est créé par la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , qui définit un pointeur vers une interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="01292-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="01292-115">Les autres interfaces de l’objet gestionnaire de profils peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="01292-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="01292-116">Les interfaces suivantes sont prises en charge par l’objet gestionnaire de profils.</span><span class="sxs-lookup"><span data-stu-id="01292-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="01292-117">Interface</span><span class="sxs-lookup"><span data-stu-id="01292-117">Interface</span></span>                                                      | <span data-ttu-id="01292-118">Description</span><span class="sxs-lookup"><span data-stu-id="01292-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01292-119">**IWMCodecInfo**</span><span class="sxs-lookup"><span data-stu-id="01292-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="01292-120">Récupère des informations sur les codecs pris en charge et leurs formats.</span><span class="sxs-lookup"><span data-stu-id="01292-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="01292-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="01292-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="01292-122">Récupère les noms des codecs pris en charge et les descriptions de leurs formats.</span><span class="sxs-lookup"><span data-stu-id="01292-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="01292-123">Hérite de toutes les méthodes de **IWMCodecInfo**.</span><span class="sxs-lookup"><span data-stu-id="01292-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="01292-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="01292-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="01292-125">Récupère les codecs et les propriétés de codec pour les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="01292-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="01292-126">Hérite de toutes les méthodes de **IWMCodecInfo** et **IWMCodecInfo2**.</span><span class="sxs-lookup"><span data-stu-id="01292-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="01292-127">**IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="01292-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="01292-128">Crée de nouveaux profils, charge des profils existants et enregistre les profils personnalisés.</span><span class="sxs-lookup"><span data-stu-id="01292-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="01292-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="01292-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="01292-130">Contrôle la version des profils système énumérés par le gestionnaire de profils.</span><span class="sxs-lookup"><span data-stu-id="01292-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="01292-131">Hérite de toutes les méthodes de **IWMProfileManager**.</span><span class="sxs-lookup"><span data-stu-id="01292-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="01292-132">**IWMProfileManagerLanguage**</span><span class="sxs-lookup"><span data-stu-id="01292-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="01292-133">Contrôle la langue des profils système analysés par le gestionnaire de profils.</span><span class="sxs-lookup"><span data-stu-id="01292-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="01292-134">Notes</span><span class="sxs-lookup"><span data-stu-id="01292-134">Remarks</span></span>

<span data-ttu-id="01292-135">Lorsqu’un objet gestionnaire de profils est créé, il analyse tous les profils système, ce qui peut prendre plusieurs secondes.</span><span class="sxs-lookup"><span data-stu-id="01292-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="01292-136">La création et la libération d’un gestionnaire de profils chaque fois que vous devez l’utiliser, nuire aux performances.</span><span class="sxs-lookup"><span data-stu-id="01292-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="01292-137">Vous devez créer un gestionnaire de profils une fois dans votre application et le libérer uniquement lorsque vous n’avez plus besoin de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="01292-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01292-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01292-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01292-139">**Objets**</span><span class="sxs-lookup"><span data-stu-id="01292-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="01292-140">**Profile (objet)**</span><span class="sxs-lookup"><span data-stu-id="01292-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="01292-141">**Profils**</span><span class="sxs-lookup"><span data-stu-id="01292-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




