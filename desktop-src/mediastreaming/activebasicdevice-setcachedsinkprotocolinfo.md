---
title: Méthode ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtient les informations de protocole du récepteur mis en cache pour l’appareil. | Méthode ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API de diffusion multimédia en continu de méthode SetCachedSinkProtocolInfo
- API de diffusion multimédia en continu de méthode SetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106545251"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="80b90-107">ActiveBasicDevice :: SetCachedSinkProtocolInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="80b90-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="80b90-108">Obtient les informations de protocole du récepteur mis en cache pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="80b90-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b90-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80b90-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="80b90-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80b90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b90-111">*physicalNetworkInterface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80b90-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b90-112">Spécifie l’interface réseau physique.</span><span class="sxs-lookup"><span data-stu-id="80b90-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="80b90-113">*débit binaire* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80b90-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80b90-114">Valeur de la vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="80b90-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80b90-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80b90-115">Return value</span></span>

<span data-ttu-id="80b90-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80b90-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80b90-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80b90-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b90-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80b90-118">Requirements</span></span>



| <span data-ttu-id="80b90-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80b90-119">Requirement</span></span> | <span data-ttu-id="80b90-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="80b90-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b90-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80b90-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80b90-122">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80b90-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80b90-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80b90-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80b90-124">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80b90-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="80b90-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="80b90-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b90-126"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b90-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="80b90-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="80b90-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80b90-128"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80b90-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="80b90-129">DLL</span><span class="sxs-lookup"><span data-stu-id="80b90-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80b90-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80b90-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b90-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b90-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="80b90-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80b90-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

