---
description: L’interface IScanProfileMgr fournit des méthodes pour créer, ouvrir, supprimer et gérer des profils d’analyse.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interface IScanProfileMgr (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514227"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="46ffe-103">Interface IScanProfileMgr</span><span class="sxs-lookup"><span data-stu-id="46ffe-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="46ffe-104">L’interface **IScanProfileMgr** fournit des méthodes pour créer, ouvrir, supprimer et gérer des profils d’analyse.</span><span class="sxs-lookup"><span data-stu-id="46ffe-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="46ffe-105">Membres</span><span class="sxs-lookup"><span data-stu-id="46ffe-105">Members</span></span>

<span data-ttu-id="46ffe-106">L’interface **IScanProfileMgr** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="46ffe-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="46ffe-107">**IScanProfileMgr** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46ffe-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="46ffe-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46ffe-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="46ffe-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="46ffe-109">Methods</span></span>

<span data-ttu-id="46ffe-110">L’interface **IScanProfileMgr** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="46ffe-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="46ffe-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="46ffe-111">Method</span></span>                                                                              | <span data-ttu-id="46ffe-112">Description</span><span class="sxs-lookup"><span data-stu-id="46ffe-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46ffe-113">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="46ffe-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="46ffe-114">Crée un profil de numérisation vide et l’associe à un scanneur ou à un autre élément WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="46ffe-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="46ffe-115">**DeleteAllProfiles**</span><span class="sxs-lookup"><span data-stu-id="46ffe-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="46ffe-116">Supprime tous les profils d’analyse associés à l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="46ffe-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="46ffe-117">**DeleteAllProfilesForUser**</span><span class="sxs-lookup"><span data-stu-id="46ffe-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="46ffe-118">Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="46ffe-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="46ffe-119">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="46ffe-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="46ffe-120">Supprime le profil de numérisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="46ffe-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="46ffe-121">**GetDefaultProfile**</span><span class="sxs-lookup"><span data-stu-id="46ffe-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="46ffe-122">Obtient le profil de numérisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="46ffe-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="46ffe-123">**GetNumProfiles**</span><span class="sxs-lookup"><span data-stu-id="46ffe-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="46ffe-124">Obtient le nombre de profils d’analyse créés pour l’utilisateur dans le système sous lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="46ffe-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="46ffe-125">**GetNumProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="46ffe-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="46ffe-126">Obtient le nombre de profils de numérisation pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46ffe-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="46ffe-127">**GetProfiles**</span><span class="sxs-lookup"><span data-stu-id="46ffe-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="46ffe-128">Obtient tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.</span><span class="sxs-lookup"><span data-stu-id="46ffe-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="46ffe-129">**GetProfilesforDeviceID**</span><span class="sxs-lookup"><span data-stu-id="46ffe-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="46ffe-130">Obtient tous les profils d’analyse associés à un appareil.</span><span class="sxs-lookup"><span data-stu-id="46ffe-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="46ffe-131">**OpenProfile**</span><span class="sxs-lookup"><span data-stu-id="46ffe-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="46ffe-132">Ouvre un profil de numérisation enregistré sur le disque sous la forme d’un fichier XML.</span><span class="sxs-lookup"><span data-stu-id="46ffe-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="46ffe-133">**Générer**</span><span class="sxs-lookup"><span data-stu-id="46ffe-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="46ffe-134">Énumère à nouveau tous les profils d’analyse dans le système.</span><span class="sxs-lookup"><span data-stu-id="46ffe-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="46ffe-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="46ffe-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="46ffe-136">Définit le profil d’analyse spécifié comme profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="46ffe-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="46ffe-137">Notes</span><span class="sxs-lookup"><span data-stu-id="46ffe-137">Remarks</span></span>

<span data-ttu-id="46ffe-138">Pour créer un objet **IScanProfileMgr** , utilisez la méthode [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="46ffe-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="46ffe-139">Si un profil de numérisation est enregistré à l’aide de la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) , il est stocké sous la forme d’un fichier XML dans% UserProfile%, \\ données d’application \\ Microsoft \\ document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="46ffe-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ffe-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46ffe-140">Requirements</span></span>



| <span data-ttu-id="46ffe-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46ffe-141">Requirement</span></span> | <span data-ttu-id="46ffe-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="46ffe-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ffe-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46ffe-143">Minimum supported client</span></span><br/> | <span data-ttu-id="46ffe-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46ffe-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="46ffe-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46ffe-145">Minimum supported server</span></span><br/> | <span data-ttu-id="46ffe-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46ffe-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46ffe-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="46ffe-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="46ffe-148"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ffe-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="46ffe-149">MIDL</span><span class="sxs-lookup"><span data-stu-id="46ffe-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46ffe-150"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46ffe-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ffe-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46ffe-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ffe-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="46ffe-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="46ffe-153">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="46ffe-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
