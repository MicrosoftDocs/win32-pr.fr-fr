---
title: IMsRdpDeviceV2 propriété CmDeviceInstance
description: Contient l’instance d’appareil Configuration Manager de l’appareil.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CmDeviceInstance
- Services Bureau à distance de la propriété CmDeviceInstance, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété CmDeviceInstance
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510115"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a><span data-ttu-id="3b945-106">IMsRdpDeviceV2 :: CmDeviceInstance, propriété</span><span class="sxs-lookup"><span data-stu-id="3b945-106">IMsRdpDeviceV2::CmDeviceInstance property</span></span>

<span data-ttu-id="3b945-107">Contient l’instance d’appareil Configuration Manager de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3b945-107">Contains the configuration manager device instance of the device.</span></span>

<span data-ttu-id="3b945-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3b945-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b945-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b945-109">Syntax</span></span>


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a><span data-ttu-id="3b945-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3b945-110">Property value</span></span>

<span data-ttu-id="3b945-111">Instance de périphérique Configuration Manager de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3b945-111">The configuration manager device instance of the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b945-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b945-112">Requirements</span></span>



| <span data-ttu-id="3b945-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b945-113">Requirement</span></span> | <span data-ttu-id="3b945-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b945-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b945-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b945-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b945-116">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="3b945-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="3b945-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b945-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b945-118">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="3b945-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="3b945-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3b945-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b945-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b945-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b945-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3b945-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b945-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b945-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b945-123">IID</span><span class="sxs-lookup"><span data-stu-id="3b945-123">IID</span></span><br/>                      | <span data-ttu-id="3b945-124">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="3b945-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="3b945-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b945-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b945-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="3b945-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





