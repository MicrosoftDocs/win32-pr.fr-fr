---
title: IMsRdpDeviceV2 propriété IsCompositeDevice
description: Spécifie si l’appareil est un appareil composite.
ms.assetid: cc54f3f0-de0b-4f75-b5a1-4f061ac95ab5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IsCompositeDevice
- Services Bureau à distance de la propriété IsCompositeDevice, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété IsCompositeDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsCompositeDevice
- IMsRdpDeviceV2.get_IsCompositeDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2341544543f436272486a839ffdd3ee68a4a4478
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464310"
---
# <a name="imsrdpdevicev2iscompositedevice-property"></a><span data-ttu-id="c00dc-106">IMsRdpDeviceV2 :: IsCompositeDevice, propriété</span><span class="sxs-lookup"><span data-stu-id="c00dc-106">IMsRdpDeviceV2::IsCompositeDevice property</span></span>

<span data-ttu-id="c00dc-107">Spécifie si l’appareil est un appareil composite.</span><span class="sxs-lookup"><span data-stu-id="c00dc-107">Specifies if the device is a composite device.</span></span>

<span data-ttu-id="c00dc-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c00dc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c00dc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c00dc-109">Syntax</span></span>


```C++
HRESULT get_IsCompositeDevice(
  [out, retval] VARIANT_BOOL *pvboolCompositeDevice
);
```



## <a name="property-value"></a><span data-ttu-id="c00dc-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c00dc-110">Property value</span></span>

<span data-ttu-id="c00dc-111">**true** si l’appareil est un appareil composite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="c00dc-111">**true** if the device is a composite device; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c00dc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c00dc-112">Requirements</span></span>



| <span data-ttu-id="c00dc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c00dc-113">Requirement</span></span> | <span data-ttu-id="c00dc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c00dc-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c00dc-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c00dc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c00dc-116">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="c00dc-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="c00dc-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c00dc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c00dc-118">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="c00dc-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="c00dc-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c00dc-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="c00dc-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c00dc-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c00dc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c00dc-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c00dc-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c00dc-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c00dc-123">IID</span><span class="sxs-lookup"><span data-stu-id="c00dc-123">IID</span></span><br/>                      | <span data-ttu-id="c00dc-124">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="c00dc-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c00dc-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c00dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00dc-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="c00dc-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





