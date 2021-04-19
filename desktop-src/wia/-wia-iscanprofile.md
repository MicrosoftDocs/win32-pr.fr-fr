---
description: L’interface IScanProfile représente un profil de numérisation unique et permet aux applications de définir et d’obtenir les propriétés du profil.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interface IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524666"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="eeb7b-103">Interface IScanProfile</span><span class="sxs-lookup"><span data-stu-id="eeb7b-103">IScanProfile interface</span></span>

<span data-ttu-id="eeb7b-104">L’interface **IScanProfile** représente un profil de numérisation unique et permet aux applications de définir et d’obtenir les propriétés du profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="eeb7b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="eeb7b-105">Members</span></span>

<span data-ttu-id="eeb7b-106">L’interface **IScanProfile** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="eeb7b-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eeb7b-107">**IScanProfile** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eeb7b-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="eeb7b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eeb7b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eeb7b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eeb7b-109">Methods</span></span>

<span data-ttu-id="eeb7b-110">L’interface **IScanProfile** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="eeb7b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="eeb7b-111">Method</span></span>                                                     | <span data-ttu-id="eeb7b-112">Description</span><span class="sxs-lookup"><span data-stu-id="eeb7b-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeb7b-113">**GetAllPropIDs**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="eeb7b-114">Obtient tous les ID de propriété disponibles dans un profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eeb7b-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="eeb7b-116">Retourne l’ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="eeb7b-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="eeb7b-118">Retourne le GUID du profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="eeb7b-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="eeb7b-120">Obtient le GUID de la catégorie de l’élément WIA 2,0 auquel le profil est associé.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="eeb7b-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="eeb7b-122">Obtient le nom convivial du profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="eeb7b-123">**GetNumPropIDS**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="eeb7b-124">Obtient le nombre d’ID de propriété dans un profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eeb7b-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="eeb7b-126">Obtient la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="eeb7b-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="eeb7b-128">Obtient une valeur qui indique si le profil est le profil de numérisation par défaut d’un appareil [**IWiaItem2**](-wia-iwiaitem2.md) associé.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="eeb7b-129">**RemoveProperty**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="eeb7b-130">Supprime une liste spécifiée de propriétés enfants dans l' `<Properties>` élément d’un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="eeb7b-131">**Enregistrer**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="eeb7b-132">Enregistre les modifications apportées à un profil sur le disque.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="eeb7b-133">**SetItem**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="eeb7b-134">Définit le GUID de la catégorie de l’élément WIA 2,0 auquel le profil est associé.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="eeb7b-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="eeb7b-136">Définit le nom convivial du profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="eeb7b-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="eeb7b-138">Définit la valeur des propriétés enfants spécifiées dans l' `<Properties>` élément d’un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="eeb7b-139">Notes</span><span class="sxs-lookup"><span data-stu-id="eeb7b-139">Remarks</span></span>

<span data-ttu-id="eeb7b-140">Tout appareil [**IWiaItem2**](-wia-iwiaitem2.md) peut avoir un profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="eeb7b-141">Toutefois, les éléments **IWiaItem2** de type WIA la \_ catégorie \_ \_ fichier fini et la racine de catégorie WIA \_ \_ ne peuvent pas avoir de profils.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="eeb7b-142">Si un profil de numérisation est enregistré à l’aide de la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) , il est stocké sous la forme d’un fichier XML dans% UserProfile%, \\ données d’application \\ Microsoft \\ document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="eeb7b-143">Pour créer une instance d’un objet **IScanProfile** , utilisez la méthode [**IScanProfileMgr :: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="eeb7b-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="eeb7b-144">Pour obtenir une référence à un profil de numérisation qui a déjà été enregistré sur le disque, utilisez la méthode [**IScanProfileMgr :: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="eeb7b-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="eeb7b-145">Tous les profils d’analyse comportent les éléments suivants : `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` et `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="eeb7b-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="eeb7b-146">Le profil par défaut d’un appareil possède également un `<Default>` élément.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="eeb7b-147">Les `<ProfileGUID>` `<DeviceID>` éléments et ne peuvent pas être modifiés une fois le profil créé.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="eeb7b-148">Les valeurs de l' `<ProfileName>` élément et de l' `<WiaItem>` élément peuvent être modifiées après la création du profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="eeb7b-149">L' `<Default>` élément peut être ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="eeb7b-150">Cela peut être effectué par programmation avec les méthodes [**IScanProfile :: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile :: SetItem**](-wia-iscanprofile-setitem.md)et [**IScanProfileMgr :: SetDefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="eeb7b-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="eeb7b-151">Ces propriétés peuvent également être modifiées par les utilisateurs par le biais de la méthode [**IScanProfileUI :: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="eeb7b-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="eeb7b-152">L' `<Properties>` élément contient des `<Property>` enfants.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="eeb7b-153">Utilisez-les pour ajouter n’importe quel élément ou propriété d’appareil WIA 2,0 au profil.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="eeb7b-154">Vous pouvez également développer votre propre image acquisition `<Property>` Children.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="eeb7b-155">Cela rend le schéma de profil d’analyse extensible.</span><span class="sxs-lookup"><span data-stu-id="eeb7b-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="eeb7b-156">(Pour plus d’informations sur l’extension du schéma, consultez [définition des propriétés personnalisées](-wia-defining-custom-properties.md), [**IScanProfile :: GetProperty**](-wia-iscanprofile-getproperty.md)et [**IScanProfile :: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="eeb7b-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb7b-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeb7b-157">Requirements</span></span>



| <span data-ttu-id="eeb7b-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeb7b-158">Requirement</span></span> | <span data-ttu-id="eeb7b-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeb7b-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb7b-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb7b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb7b-161">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeb7b-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eeb7b-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb7b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb7b-163">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeb7b-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eeb7b-164">MIDL</span><span class="sxs-lookup"><span data-stu-id="eeb7b-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eeb7b-165"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eeb7b-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb7b-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeb7b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb7b-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="eeb7b-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="eeb7b-168">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="eeb7b-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
