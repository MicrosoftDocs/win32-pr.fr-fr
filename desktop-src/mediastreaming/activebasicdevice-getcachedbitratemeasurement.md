---
title: Méthode ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Obtient le débit binaire mis en cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API de diffusion multimédia en continu de méthode GetCachedBitrateMeasurement
- API de diffusion multimédia en continu de méthode GetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509190"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="daf22-106">ActiveBasicDevice :: GetCachedBitrateMeasurement, méthode</span><span class="sxs-lookup"><span data-stu-id="daf22-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="daf22-107">Obtient le débit binaire mis en cache.</span><span class="sxs-lookup"><span data-stu-id="daf22-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf22-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daf22-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="daf22-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daf22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf22-110">*physicalNetworkInterface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="daf22-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daf22-111">Spécifie l’interface réseau physique.</span><span class="sxs-lookup"><span data-stu-id="daf22-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="daf22-112">*débit binaire* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="daf22-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="daf22-113">Reçoit la valeur de débit binaire.</span><span class="sxs-lookup"><span data-stu-id="daf22-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf22-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="daf22-114">Return value</span></span>

<span data-ttu-id="daf22-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="daf22-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="daf22-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="daf22-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf22-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daf22-117">Requirements</span></span>



| <span data-ttu-id="daf22-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daf22-118">Requirement</span></span> | <span data-ttu-id="daf22-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="daf22-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf22-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daf22-120">Minimum supported client</span></span><br/> | <span data-ttu-id="daf22-121">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daf22-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="daf22-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="daf22-122">Minimum supported server</span></span><br/> | <span data-ttu-id="daf22-123">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="daf22-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="daf22-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="daf22-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="daf22-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="daf22-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="daf22-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="daf22-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="daf22-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="daf22-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="daf22-128">DLL</span><span class="sxs-lookup"><span data-stu-id="daf22-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daf22-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daf22-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf22-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daf22-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="daf22-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="daf22-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

