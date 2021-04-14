---
title: Méthode ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Définit le débit binaire mis en cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API de diffusion multimédia en continu de méthode SetCachedBitrateMeasurement
- API de diffusion multimédia en continu de méthode SetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466814"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="3e875-106">ActiveBasicDevice :: SetCachedBitrateMeasurement, méthode</span><span class="sxs-lookup"><span data-stu-id="3e875-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="3e875-107">Définit le débit binaire mis en cache.</span><span class="sxs-lookup"><span data-stu-id="3e875-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e875-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e875-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="3e875-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e875-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e875-110">*physicalNetworkInterface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e875-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e875-111">Spécifie l’interface réseau physique.</span><span class="sxs-lookup"><span data-stu-id="3e875-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="3e875-112">*débit binaire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e875-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e875-113">Valeur sur laquelle définir le débit binaire.</span><span class="sxs-lookup"><span data-stu-id="3e875-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e875-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e875-114">Return value</span></span>

<span data-ttu-id="3e875-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3e875-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e875-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e875-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e875-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e875-117">Requirements</span></span>



| <span data-ttu-id="3e875-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e875-118">Requirement</span></span> | <span data-ttu-id="3e875-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e875-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e875-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e875-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e875-121">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e875-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3e875-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e875-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e875-123">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e875-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3e875-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e875-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e875-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e875-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e875-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="3e875-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e875-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e875-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="3e875-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3e875-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e875-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e875-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e875-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e875-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e875-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3e875-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

