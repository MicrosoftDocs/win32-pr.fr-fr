---
title: Méthode ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice. h)
description: Obtient des informations supplémentaires sur le protocole récepteur mis en cache pour l’appareil.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API de diffusion multimédia en continu de méthode GetCachedExtraSinkProtocolInfo
- API de diffusion multimédia en continu de méthode GetCachedExtraSinkProtocolInfo, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetCachedExtraSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384851"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="78e2a-106">ActiveBasicDevice :: GetCachedExtraSinkProtocolInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="78e2a-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="78e2a-107">Obtient des informations supplémentaires sur le protocole récepteur mis en cache pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="78e2a-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e2a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78e2a-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="78e2a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78e2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78e2a-110">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="78e2a-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="78e2a-111">Informations supplémentaires sur le protocole récepteur mis en cache pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="78e2a-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78e2a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78e2a-112">Return value</span></span>

<span data-ttu-id="78e2a-113">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="78e2a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78e2a-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78e2a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e2a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78e2a-115">Requirements</span></span>



| <span data-ttu-id="78e2a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78e2a-116">Requirement</span></span> | <span data-ttu-id="78e2a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="78e2a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e2a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78e2a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78e2a-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78e2a-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="78e2a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78e2a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78e2a-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78e2a-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="78e2a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="78e2a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78e2a-123"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="78e2a-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="78e2a-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="78e2a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78e2a-125"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78e2a-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="78e2a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="78e2a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78e2a-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e2a-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78e2a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78e2a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="78e2a-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="78e2a-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

