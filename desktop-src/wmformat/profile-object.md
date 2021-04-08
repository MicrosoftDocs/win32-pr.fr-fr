---
title: Profile (objet)
description: Profile (objet)
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media Format SDK, objets de profil
- ASF (Advanced Systems Format), objets de profil
- ASF (format des systèmes avancés), objets de profil
- objets, objets de profil
- profils, objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103841966"
---
# <a name="profile-object"></a><span data-ttu-id="9bda9-108">Profile (objet)</span><span class="sxs-lookup"><span data-stu-id="9bda9-108">Profile Object</span></span>

<span data-ttu-id="9bda9-109">Un objet de profil gère les paramètres d’un profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="9bda9-110">Vous pouvez créer des objets de profil pour les données de profil existantes ou les créer vides, prêts à recevoir de nouvelles données.</span><span class="sxs-lookup"><span data-stu-id="9bda9-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="9bda9-111">Un objet de profil est également créé par l’objet lecteur (et l’objet lecteur synchrone) lorsqu’un fichier est chargé pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="9bda9-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="9bda9-112">Dans ce cas, l’objet est rempli avec les informations de profil stockées dans l’en-tête du fichier.</span><span class="sxs-lookup"><span data-stu-id="9bda9-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="9bda9-113">Pour enregistrer le contenu d’un objet de profil, vous devez appeler [**IWMProfileManager :: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span><span class="sxs-lookup"><span data-stu-id="9bda9-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="9bda9-114">Un profil contient plusieurs objets qui contrôlent différents aspects du profil (tels que les flux).</span><span class="sxs-lookup"><span data-stu-id="9bda9-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="9bda9-115">Tous ces objets sont subordonnés à l’objet de profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="9bda9-116">Vous ne créez pas ces objets avec les fonctions de création, comme vous le feriez avec les principaux objets de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="9bda9-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="9bda9-117">Au lieu de cela, les interfaces de l’objet de profil contiennent des méthodes qui créent les objets subordonnés.</span><span class="sxs-lookup"><span data-stu-id="9bda9-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="9bda9-118">Pour créer un objet de profil, appelez l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9bda9-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="9bda9-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="9bda9-119">Method</span></span>                                                                                | <span data-ttu-id="9bda9-120">Description</span><span class="sxs-lookup"><span data-stu-id="9bda9-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bda9-121">**IWMProfileManager::CreateEmptyProfile**</span><span class="sxs-lookup"><span data-stu-id="9bda9-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="9bda9-122">Crée un objet de profil sans données de profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="9bda9-123">**IWMProfileManager::LoadProfileByData**</span><span class="sxs-lookup"><span data-stu-id="9bda9-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="9bda9-124">Crée un objet de profil rempli avec les données d’un profil enregistré en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="9bda9-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="9bda9-125">Il s’agit de la seule façon de créer un objet de profil avec les données d’un profil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="9bda9-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="9bda9-126">**IWMProfileManager::LoadProfileByID**</span><span class="sxs-lookup"><span data-stu-id="9bda9-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="9bda9-127">Crée un objet de profil rempli avec les données d’un profil système.</span><span class="sxs-lookup"><span data-stu-id="9bda9-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="9bda9-128">Utilise le GUID pour identifier le profil système souhaité.</span><span class="sxs-lookup"><span data-stu-id="9bda9-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="9bda9-129">**IWMProfileManager::LoadSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="9bda9-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="9bda9-130">Crée un objet de profil rempli avec les données d’un profil système.</span><span class="sxs-lookup"><span data-stu-id="9bda9-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="9bda9-131">Utilise l’index de profil pour identifier le profil système souhaité.</span><span class="sxs-lookup"><span data-stu-id="9bda9-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="9bda9-132">Toutes les méthodes du tableau précédent définissent un pointeur vers une interface **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="9bda9-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="9bda9-133">Les autres interfaces de l’objet de profil peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="9bda9-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="9bda9-134">Les interfaces suivantes sont prises en charge par chaque objet de profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="9bda9-135">Interface</span><span class="sxs-lookup"><span data-stu-id="9bda9-135">Interface</span></span>                                  | <span data-ttu-id="9bda9-136">Description</span><span class="sxs-lookup"><span data-stu-id="9bda9-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bda9-137">**IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="9bda9-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="9bda9-138">Gère une liste de langues prises en charge par un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="9bda9-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="9bda9-139">**IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="9bda9-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="9bda9-140">Contrôle la taille maximale des paquets dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="9bda9-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="9bda9-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="9bda9-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="9bda9-142">Contrôle la taille minimale des paquets dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="9bda9-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="9bda9-143">Hérite de toutes les méthodes de **IWMPacketSize**.</span><span class="sxs-lookup"><span data-stu-id="9bda9-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="9bda9-144">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="9bda9-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="9bda9-145">Contrôle les paramètres de base et les objets inclus dans un profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="9bda9-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="9bda9-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="9bda9-147">Récupère l’identificateur global unique (GUID) associé au profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="9bda9-148">Hérite de toutes les méthodes de **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="9bda9-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="9bda9-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="9bda9-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="9bda9-150">Contrôle le partage de bande passante et les informations de hiérarchisation des flux dans un profil.</span><span class="sxs-lookup"><span data-stu-id="9bda9-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="9bda9-151">Hérite de toutes les méthodes de **IWMProfile** et **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="9bda9-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9bda9-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bda9-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bda9-153">**Objets**</span><span class="sxs-lookup"><span data-stu-id="9bda9-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="9bda9-154">**Gestionnaire de profils, objet**</span><span class="sxs-lookup"><span data-stu-id="9bda9-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="9bda9-155">**Profils**</span><span class="sxs-lookup"><span data-stu-id="9bda9-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




