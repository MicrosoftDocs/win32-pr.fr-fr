---
title: Méthode ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Obtient la bande passante effective actuelle pour l’appareil.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API de diffusion multimédia en continu de méthode GetEffectiveBandwidth
- API de diffusion multimédia en continu de méthode GetEffectiveBandwidth, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033211"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="c9477-106">ActiveBasicDevice :: GetEffectiveBandwidth, méthode</span><span class="sxs-lookup"><span data-stu-id="c9477-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="c9477-107">Obtient la bande passante effective actuelle pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c9477-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9477-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9477-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="c9477-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9477-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9477-110">*transmitSpeed* \[ dans, retval\]</span><span class="sxs-lookup"><span data-stu-id="c9477-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c9477-111">Spécifie si la vitesse de transmission est récupérée ou si la vitesse de réception est récupérée.</span><span class="sxs-lookup"><span data-stu-id="c9477-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="c9477-112">**true** pour récupérer la vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="c9477-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="c9477-113">**false** pour récupérer la vitesse de réception.</span><span class="sxs-lookup"><span data-stu-id="c9477-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="c9477-114">*currentSpeed* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9477-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9477-115">Reçoit la bande passante effective actuelle.</span><span class="sxs-lookup"><span data-stu-id="c9477-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9477-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9477-116">Return value</span></span>

<span data-ttu-id="c9477-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c9477-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c9477-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9477-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9477-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9477-119">Requirements</span></span>



| <span data-ttu-id="c9477-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9477-120">Requirement</span></span> | <span data-ttu-id="c9477-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9477-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9477-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9477-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9477-123">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9477-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9477-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9477-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9477-125">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9477-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9477-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9477-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9477-127"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9477-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9477-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="c9477-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9477-129"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9477-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9477-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c9477-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9477-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9477-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9477-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9477-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9477-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9477-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

