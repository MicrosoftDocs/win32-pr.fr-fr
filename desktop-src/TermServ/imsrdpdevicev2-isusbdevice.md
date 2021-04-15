---
title: IMsRdpDeviceV2 propriété IsUSBDevice
description: Spécifie si l’appareil est destiné à la redirection USB.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IsUSBDevice
- Services Bureau à distance de la propriété IsUSBDevice, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété IsUSBDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3741972fdd81887713e75ed5b596e0ba1a10fd3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383876"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a><span data-ttu-id="648ee-106">IMsRdpDeviceV2 :: IsUSBDevice, propriété</span><span class="sxs-lookup"><span data-stu-id="648ee-106">IMsRdpDeviceV2::IsUSBDevice property</span></span>

<span data-ttu-id="648ee-107">Spécifie si l’appareil est destiné à la redirection USB.</span><span class="sxs-lookup"><span data-stu-id="648ee-107">Specifies if the device is for USB redirection.</span></span>

<span data-ttu-id="648ee-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="648ee-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="648ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="648ee-109">Syntax</span></span>


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a><span data-ttu-id="648ee-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="648ee-110">Property value</span></span>

<span data-ttu-id="648ee-111">**true** si l’appareil est destiné à la redirection USB ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="648ee-111">**true** if the device is for USB redirection; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="648ee-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="648ee-112">Requirements</span></span>



| <span data-ttu-id="648ee-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="648ee-113">Requirement</span></span> | <span data-ttu-id="648ee-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="648ee-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="648ee-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="648ee-115">Minimum supported client</span></span><br/> | <span data-ttu-id="648ee-116">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="648ee-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="648ee-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="648ee-117">Minimum supported server</span></span><br/> | <span data-ttu-id="648ee-118">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="648ee-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="648ee-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="648ee-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="648ee-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="648ee-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="648ee-121">DLL</span><span class="sxs-lookup"><span data-stu-id="648ee-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="648ee-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="648ee-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="648ee-123">IID</span><span class="sxs-lookup"><span data-stu-id="648ee-123">IID</span></span><br/>                      | <span data-ttu-id="648ee-124">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="648ee-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="648ee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="648ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="648ee-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="648ee-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





