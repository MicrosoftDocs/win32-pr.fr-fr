---
title: Méthode ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtient les informations de protocole du récepteur mis en cache pour l’appareil. | Méthode ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API de diffusion multimédia en continu de méthode GetCachedSinkProtocolInfo
- API de diffusion multimédia en continu de méthode GetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, méthode GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106538297"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="b00ee-107">ActiveBasicDevice :: GetCachedSinkProtocolInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="b00ee-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="b00ee-108">Obtient les informations de protocole du récepteur mis en cache pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b00ee-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b00ee-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="b00ee-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b00ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b00ee-111">*valeur* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b00ee-112">Informations de protocole du récepteur mis en cache pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b00ee-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b00ee-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b00ee-113">Return value</span></span>

<span data-ttu-id="b00ee-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b00ee-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b00ee-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b00ee-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b00ee-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b00ee-116">Requirements</span></span>



| <span data-ttu-id="b00ee-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b00ee-117">Requirement</span></span> | <span data-ttu-id="b00ee-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b00ee-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b00ee-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b00ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b00ee-120">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b00ee-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b00ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b00ee-122">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b00ee-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b00ee-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b00ee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b00ee-124"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b00ee-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="b00ee-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="b00ee-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b00ee-126"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b00ee-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="b00ee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b00ee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b00ee-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b00ee-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b00ee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b00ee-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="b00ee-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b00ee-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

