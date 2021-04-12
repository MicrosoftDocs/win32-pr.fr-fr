---
description: Retourne l’ID de l’appareil.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'IScanProfile :: GetDeviceID, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318582"
---
# <a name="iscanprofilegetdeviceid-method"></a><span data-ttu-id="cdbf8-103">IScanProfile :: GetDeviceID, méthode</span><span class="sxs-lookup"><span data-stu-id="cdbf8-103">IScanProfile::GetDeviceID method</span></span>

<span data-ttu-id="cdbf8-104">Retourne l’ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cdbf8-104">Returns the ID of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdbf8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdbf8-105">Syntax</span></span>


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="cdbf8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdbf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdbf8-107">*pbstrDeviceID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cdbf8-107">*pbstrDeviceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdbf8-108">Type : \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="cdbf8-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="cdbf8-109">Pointeur vers l’ID de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cdbf8-109">A pointer to the device ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdbf8-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cdbf8-110">Return value</span></span>

<span data-ttu-id="cdbf8-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="cdbf8-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="cdbf8-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cdbf8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cdbf8-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cdbf8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdbf8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdbf8-114">Requirements</span></span>



| <span data-ttu-id="cdbf8-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdbf8-115">Requirement</span></span> | <span data-ttu-id="cdbf8-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdbf8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbf8-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdbf8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cdbf8-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdbf8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cdbf8-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdbf8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cdbf8-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdbf8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdbf8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdbf8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdbf8-122"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf8-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="cdbf8-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="cdbf8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cdbf8-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf8-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdbf8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdbf8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdbf8-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="cdbf8-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="cdbf8-127">Analyser le schéma de profil</span><span class="sxs-lookup"><span data-stu-id="cdbf8-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




