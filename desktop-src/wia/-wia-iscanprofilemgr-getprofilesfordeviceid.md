---
description: Obtient tous les profils d’analyse associés à un appareil.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'IScanProfileMgr :: GetProfilesforDeviceID, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524491"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="c9d90-103">IScanProfileMgr :: GetProfilesforDeviceID, méthode</span><span class="sxs-lookup"><span data-stu-id="c9d90-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="c9d90-104">Obtient tous les profils d’analyse associés à un appareil.</span><span class="sxs-lookup"><span data-stu-id="c9d90-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9d90-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="c9d90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9d90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d90-107">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9d90-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d90-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c9d90-108">Type: **BSTR**</span></span>

<span data-ttu-id="c9d90-109">ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9d90-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="c9d90-110">*pulNumProfiles* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c9d90-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d90-111">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="c9d90-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="c9d90-112">En cas de réussite, pointeur vers le nombre maximal de profils à retourner.</span><span class="sxs-lookup"><span data-stu-id="c9d90-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="c9d90-113">En cas de retour, pointeur vers le nombre de profils retournés.</span><span class="sxs-lookup"><span data-stu-id="c9d90-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="c9d90-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9d90-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d90-115">Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c9d90-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="c9d90-116">Adresse d’un pointeur vers un tableau de profils.</span><span class="sxs-lookup"><span data-stu-id="c9d90-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d90-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9d90-117">Return value</span></span>

<span data-ttu-id="c9d90-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c9d90-118">Type: **HRESULT**</span></span>

<span data-ttu-id="c9d90-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9d90-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9d90-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9d90-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9d90-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c9d90-121">Remarks</span></span>

<span data-ttu-id="c9d90-122">Si le nombre total de profils associés à l’appareil est inférieur à la valeur transmise à *pulNumProfiles*, *pulNumProfiles* retourne ce total.</span><span class="sxs-lookup"><span data-stu-id="c9d90-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="c9d90-123">Sinon, elle retourne la même valeur que celle qui lui a été passée.</span><span class="sxs-lookup"><span data-stu-id="c9d90-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9d90-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9d90-124">Requirements</span></span>



| <span data-ttu-id="c9d90-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9d90-125">Requirement</span></span> | <span data-ttu-id="c9d90-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9d90-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d90-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d90-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d90-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9d90-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c9d90-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d90-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d90-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9d90-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c9d90-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9d90-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9d90-132"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d90-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="c9d90-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="c9d90-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9d90-134"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9d90-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d90-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9d90-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d90-136">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="c9d90-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="c9d90-137">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="c9d90-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




