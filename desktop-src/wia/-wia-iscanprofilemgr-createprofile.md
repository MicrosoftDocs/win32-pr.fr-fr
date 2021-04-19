---
description: Crée un profil de numérisation vide et l’associe à un scanneur ou à un autre élément 2,0 de l’acquisition d’images Windows (WIA).
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'IScanProfileMgr :: CreateProfile, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485296"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="6fe0c-103">IScanProfileMgr :: CreateProfile, méthode</span><span class="sxs-lookup"><span data-stu-id="6fe0c-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="6fe0c-104">Crée un profil de numérisation vide et l’associe à un scanneur ou à un autre élément 2,0 de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="6fe0c-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe0c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fe0c-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="6fe0c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe0c-107">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe0c-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe0c-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6fe0c-108">Type: **BSTR**</span></span>

<span data-ttu-id="6fe0c-109">ID de l’appareil ou de l’élément WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0c-110">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe0c-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe0c-111">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6fe0c-111">Type: **BSTR**</span></span>

<span data-ttu-id="6fe0c-112">Nom convivial du nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0c-113">*guidCategory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe0c-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe0c-114">Type : **GUID**</span><span class="sxs-lookup"><span data-stu-id="6fe0c-114">Type: **GUID**</span></span>

<span data-ttu-id="6fe0c-115">GUID de la catégorie de l’appareil ou de l’élément WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="6fe0c-116">Il doit s’agir de l’une \_ des \_ constantes de catégorie d’élément WIA de la loi WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="6fe0c-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="6fe0c-117">*ppScanProfile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6fe0c-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe0c-118">Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6fe0c-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="6fe0c-119">Adresse d’un pointeur vers le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe0c-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fe0c-120">Return value</span></span>

<span data-ttu-id="6fe0c-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6fe0c-121">Type: **HRESULT**</span></span>

<span data-ttu-id="6fe0c-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fe0c-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fe0c-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe0c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6fe0c-124">Remarks</span></span>

<span data-ttu-id="6fe0c-125">**IScanProfileMgr :: CreateProfile** associe le périphérique spécifié au nouveau profil de numérisation.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="6fe0c-126">**IScanProfileMgr :: CreateProfile** génère automatiquement un GUID pour le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="6fe0c-127">Obtient le GUID avec [**GetGuid**](-wia-iscanprofile-getguid.md).</span><span class="sxs-lookup"><span data-stu-id="6fe0c-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="6fe0c-128">Utilisez la méthode [**IScanProfileMgr :: Refresh**](-wia-iscanprofilemgr-refresh.md) quand plusieurs objets [**IScanProfileMgr**](-wia-iscanprofilemgr.md) peuvent créer ou supprimer des profils en même temps.</span><span class="sxs-lookup"><span data-stu-id="6fe0c-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe0c-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fe0c-129">Requirements</span></span>



| <span data-ttu-id="6fe0c-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fe0c-130">Requirement</span></span> | <span data-ttu-id="6fe0c-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fe0c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe0c-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe0c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe0c-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe0c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="6fe0c-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe0c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe0c-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe0c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fe0c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fe0c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fe0c-137"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fe0c-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="6fe0c-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="6fe0c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6fe0c-139"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fe0c-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe0c-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe0c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe0c-141">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="6fe0c-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="6fe0c-142">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="6fe0c-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




