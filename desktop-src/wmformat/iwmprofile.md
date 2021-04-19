---
title: Interface IWMProfile
description: L’interface IWMProfile est l’interface principale d’un objet de profil.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Format Windows Media de l’interface IWMProfile
- Interface IWMProfile format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "106511328"
---
# <a name="iwmprofile-interface"></a><span data-ttu-id="d85ac-105">Interface IWMProfile</span><span class="sxs-lookup"><span data-stu-id="d85ac-105">IWMProfile interface</span></span>

<span data-ttu-id="d85ac-106">L’interface **IWMProfile** est l’interface principale d’un objet de [*Profil*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="d85ac-106">The **IWMProfile** interface is the primary interface for a [*profile*](wmformat-glossary.md) object.</span></span> <span data-ttu-id="d85ac-107">Un objet de profil est utilisé pour configurer des profils personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d85ac-107">A profile object is used to configure custom profiles.</span></span> <span data-ttu-id="d85ac-108">Vous pouvez utiliser **IWMProfile** pour créer, supprimer ou modifier des objets de configuration de flux et des objets d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="d85ac-108">You can use **IWMProfile** to create, delete, or modify stream configuration objects and mutual exclusion objects.</span></span> <span data-ttu-id="d85ac-109">Vous pouvez également définir et récupérer des informations générales sur le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-109">You can also set and retrieve general information about the profile.</span></span> <span data-ttu-id="d85ac-110">Pour accéder à toutes les fonctionnalités de l’objet profil, vous devez utiliser [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), qui hérite de **IWMProfile** et [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span><span class="sxs-lookup"><span data-stu-id="d85ac-110">To access all the features of the profile object, you should use [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), which inherits from **IWMProfile** and [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).</span></span>

<span data-ttu-id="d85ac-111">**IWMProfile** est également accessible via l’objet Reader, où vous pouvez l’utiliser pour obtenir des informations sur les flux d’un fichier chargé dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="d85ac-111">**IWMProfile** is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader.</span></span> <span data-ttu-id="d85ac-112">Lors de l’accès à **IWMProfile** à partir du lecteur, vous pouvez apporter des modifications au profil, mais aucune des modifications ne peut être enregistrée dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="d85ac-112">When accessing **IWMProfile** from the reader, you can make changes to the profile, but none of the changes can be saved to the file.</span></span> <span data-ttu-id="d85ac-113">Il est souvent pratique d’utiliser le profil d’un fichier existant comme base d’un nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-113">It is often handy to use the profile of an existing file as the foundation of a new profile.</span></span> <span data-ttu-id="d85ac-114">Le lecteur synchrone prend en charge **IWMProfile** de la même façon que le lecteur.</span><span class="sxs-lookup"><span data-stu-id="d85ac-114">The synchronous reader supports **IWMProfile** in the same way as the reader.</span></span>

<span data-ttu-id="d85ac-115">Les informations de profil obtenues via le lecteur ou le lecteur synchrone ne proviennent pas d’un fichier. prx.</span><span class="sxs-lookup"><span data-stu-id="d85ac-115">The profile information obtained through the reader or synchronous reader does not come from a .prx file.</span></span> <span data-ttu-id="d85ac-116">Le lecteur utilise les informations du fichier ASF pour assembler les configurations de flux.</span><span class="sxs-lookup"><span data-stu-id="d85ac-116">The reader uses the information in the ASF file to assemble the stream configurations.</span></span> <span data-ttu-id="d85ac-117">Ainsi, certaines informations de profil, telles que le nom et la description, ne sont pas disponibles via le lecteur.</span><span class="sxs-lookup"><span data-stu-id="d85ac-117">Thus certain profile information, like the name and description, are not available through the reader.</span></span>

<span data-ttu-id="d85ac-118">Il existe plusieurs façons d’obtenir un pointeur vers une interface **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="d85ac-118">There are several ways to obtain a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="d85ac-119">Le gestionnaire de profils a des méthodes pour créer un nouveau profil et accéder aux profils existants.</span><span class="sxs-lookup"><span data-stu-id="d85ac-119">The profile manager has methods to create a new profile and to access existing profiles.</span></span> <span data-ttu-id="d85ac-120">Toutes ces méthodes définissent un pointeur **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="d85ac-120">All of these methods set an **IWMProfile** pointer.</span></span> <span data-ttu-id="d85ac-121">Lors de la lecture d’un fichier, un pointeur vers **IWMProfile** peut être obtenu en appelant la méthode **QueryInterface** de toute interface de lecteur.</span><span class="sxs-lookup"><span data-stu-id="d85ac-121">When reading a file, a pointer to **IWMProfile** can be obtained by calling the **QueryInterface** method of any reader interface.</span></span> <span data-ttu-id="d85ac-122">De même, toute interface de l’objet de lecteur synchrone peut obtenir un pointeur avec un appel à **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span><span class="sxs-lookup"><span data-stu-id="d85ac-122">Likewise, any interface of the synchronous reader object can obtain a pointer with a call to **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).</span></span>

## <a name="members"></a><span data-ttu-id="d85ac-123">Membres</span><span class="sxs-lookup"><span data-stu-id="d85ac-123">Members</span></span>

<span data-ttu-id="d85ac-124">L’interface **IWMProfile** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d85ac-124">The **IWMProfile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d85ac-125">**IWMProfile** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d85ac-125">**IWMProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="d85ac-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d85ac-126">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d85ac-127">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d85ac-127">Methods</span></span>

<span data-ttu-id="d85ac-128">L’interface **IWMProfile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d85ac-128">The **IWMProfile** interface has these methods.</span></span>



| <span data-ttu-id="d85ac-129">Méthode</span><span class="sxs-lookup"><span data-stu-id="d85ac-129">Method</span></span>                                                                  | <span data-ttu-id="d85ac-130">Description</span><span class="sxs-lookup"><span data-stu-id="d85ac-130">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d85ac-131">**AddMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="d85ac-131">**AddMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | <span data-ttu-id="d85ac-132">Ajoute un objet d’exclusion mutuelle au profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-132">Adds a mutual exclusion object to the profile.</span></span><br/>                                   |
| [<span data-ttu-id="d85ac-133">**AddStream**</span><span class="sxs-lookup"><span data-stu-id="d85ac-133">**AddStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | <span data-ttu-id="d85ac-134">Ajoute un flux au profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-134">Adds a stream to the profile.</span></span><br/>                                                    |
| [<span data-ttu-id="d85ac-135">**CreateNewMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="d85ac-135">**CreateNewMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | <span data-ttu-id="d85ac-136">Crée un objet d’exclusion mutuelle pour le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-136">Creates a mutual exclusion object for the profile.</span></span><br/>                               |
| [<span data-ttu-id="d85ac-137">**CreateNewStream**</span><span class="sxs-lookup"><span data-stu-id="d85ac-137">**CreateNewStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | <span data-ttu-id="d85ac-138">Crée un objet de configuration de flux pour le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-138">Creates a stream configuration object for the profile.</span></span><br/>                           |
| [<span data-ttu-id="d85ac-139">**GetDescription**</span><span class="sxs-lookup"><span data-stu-id="d85ac-139">**GetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | <span data-ttu-id="d85ac-140">Récupère la description du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-140">Retrieves the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="d85ac-141">**GetMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="d85ac-141">**GetMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | <span data-ttu-id="d85ac-142">Récupère un objet d’exclusion mutuelle à partir du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-142">Retrieves a mutual exclusion object from the profile.</span></span><br/>                            |
| [<span data-ttu-id="d85ac-143">**GetMutualExclusionCount**</span><span class="sxs-lookup"><span data-stu-id="d85ac-143">**GetMutualExclusionCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | <span data-ttu-id="d85ac-144">Récupère le nombre d’objets d’exclusion mutuelle dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-144">Retrieves the number of mutual exclusion objects in the profile.</span></span><br/>                 |
| [<span data-ttu-id="d85ac-145">**GetName**</span><span class="sxs-lookup"><span data-stu-id="d85ac-145">**GetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | <span data-ttu-id="d85ac-146">Récupère le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-146">Retrieves the name of the profile.</span></span><br/>                                               |
| [<span data-ttu-id="d85ac-147">**GetStream**</span><span class="sxs-lookup"><span data-stu-id="d85ac-147">**GetStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | <span data-ttu-id="d85ac-148">Récupère un flux, à l’aide d’un numéro d’index, à partir du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-148">Retrieves a stream, using an index number, from the profile.</span></span><br/>                     |
| [<span data-ttu-id="d85ac-149">**GetStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="d85ac-149">**GetStreamByNumber**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | <span data-ttu-id="d85ac-150">Récupère un flux, à l’aide du numéro du flux, à partir du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-150">Retrieves a stream, using the number of the stream, from the profile.</span></span><br/>            |
| [<span data-ttu-id="d85ac-151">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="d85ac-151">**GetStreamCount**</span></span>](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | <span data-ttu-id="d85ac-152">Récupère le nombre de flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-152">Retrieves the number of streams in the profile.</span></span><br/>                                  |
| [<span data-ttu-id="d85ac-153">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="d85ac-153">**GetVersion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | <span data-ttu-id="d85ac-154">Récupère le numéro de version de Microsoft Windows Media Services dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-154">Retrieves the version number of Microsoft Windows Media Services in the profile.</span></span><br/> |
| [<span data-ttu-id="d85ac-155">**ReconfigStream**</span><span class="sxs-lookup"><span data-stu-id="d85ac-155">**ReconfigStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | <span data-ttu-id="d85ac-156">Permet d’inclure les modifications apportées à une configuration de flux dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-156">Enables changes made to a stream configuration to be included in the profile.</span></span><br/>    |
| [<span data-ttu-id="d85ac-157">**RemoveMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="d85ac-157">**RemoveMutualExclusion**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | <span data-ttu-id="d85ac-158">Supprime un objet d’exclusion mutuelle du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-158">Removes a mutual exclusion object from the profile.</span></span><br/>                              |
| [<span data-ttu-id="d85ac-159">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="d85ac-159">**RemoveStream**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | <span data-ttu-id="d85ac-160">Supprime un flux du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-160">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="d85ac-161">**RemoveStreamByNumber**</span><span class="sxs-lookup"><span data-stu-id="d85ac-161">**RemoveStreamByNumber**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | <span data-ttu-id="d85ac-162">Supprime un flux du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-162">Removes a stream from the profile.</span></span><br/>                                               |
| [<span data-ttu-id="d85ac-163">**SetDescription**</span><span class="sxs-lookup"><span data-stu-id="d85ac-163">**SetDescription**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | <span data-ttu-id="d85ac-164">Spécifie la description du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-164">Specifies the description of the profile.</span></span><br/>                                        |
| [<span data-ttu-id="d85ac-165">**SetName**</span><span class="sxs-lookup"><span data-stu-id="d85ac-165">**SetName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | <span data-ttu-id="d85ac-166">Spécifie le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="d85ac-166">Specifies the name of the profile.</span></span><br/>                                               |



 

<span data-ttu-id="d85ac-167">Pour plus d’informations sur les interfaces pouvant être obtenues à l’aide de la méthode QueryInterface de cette interface, consultez la rubrique relative à l’objet sur lequel cette interface est implémentée.</span><span class="sxs-lookup"><span data-stu-id="d85ac-167">For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.</span></span>

## <a name="see-also"></a><span data-ttu-id="d85ac-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d85ac-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85ac-169">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="d85ac-169">**Interfaces**</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="d85ac-170">**Interface IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="d85ac-170">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="d85ac-171">**Gestionnaire de profils, objet**</span><span class="sxs-lookup"><span data-stu-id="d85ac-171">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="d85ac-172">**Lecteur, objet**</span><span class="sxs-lookup"><span data-stu-id="d85ac-172">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="d85ac-173">**Lecteur synchrone, objet**</span><span class="sxs-lookup"><span data-stu-id="d85ac-173">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> <dt>

[<span data-ttu-id="d85ac-174">**Utilisation des profils**</span><span class="sxs-lookup"><span data-stu-id="d85ac-174">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

