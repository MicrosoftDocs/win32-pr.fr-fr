---
description: Obtient le nombre de profils de numérisation pour l’appareil.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'IScanProfileMgr :: GetNumProfilesforDeviceID, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201668"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="c4e04-103">IScanProfileMgr :: GetNumProfilesforDeviceID, méthode</span><span class="sxs-lookup"><span data-stu-id="c4e04-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="c4e04-104">Obtient le nombre de profils de numérisation pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c4e04-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4e04-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4e04-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="c4e04-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4e04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e04-107">*bstrDeviceID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4e04-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e04-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c4e04-108">Type: **BSTR**</span></span>

<span data-ttu-id="c4e04-109">ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c4e04-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="c4e04-110">*pulNumProfiles* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c4e04-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e04-111">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="c4e04-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="c4e04-112">Pointeur vers le nombre de profils disponibles pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c4e04-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e04-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4e04-113">Return value</span></span>

<span data-ttu-id="c4e04-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c4e04-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c4e04-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4e04-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4e04-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4e04-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4e04-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4e04-117">Requirements</span></span>



| <span data-ttu-id="c4e04-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4e04-118">Requirement</span></span> | <span data-ttu-id="c4e04-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4e04-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e04-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4e04-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e04-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4e04-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c4e04-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4e04-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e04-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4e04-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4e04-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4e04-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4e04-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e04-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="c4e04-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="c4e04-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4e04-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4e04-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4e04-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4e04-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e04-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="c4e04-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="c4e04-130">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="c4e04-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




