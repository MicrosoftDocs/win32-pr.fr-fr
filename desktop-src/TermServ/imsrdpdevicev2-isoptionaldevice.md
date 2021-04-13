---
title: IMsRdpDeviceV2 propriété IsOptionalDevice
description: Spécifie si l’appareil est facultatif pour la redirection USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété IsOptionalDevice
- Services Bureau à distance de la propriété IsOptionalDevice, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété IsOptionalDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465991"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a><span data-ttu-id="97cf9-106">IMsRdpDeviceV2 :: IsOptionalDevice, propriété</span><span class="sxs-lookup"><span data-stu-id="97cf9-106">IMsRdpDeviceV2::IsOptionalDevice property</span></span>

<span data-ttu-id="97cf9-107">Spécifie si l’appareil est facultatif pour la redirection USB.</span><span class="sxs-lookup"><span data-stu-id="97cf9-107">Specifies if the device is optional for USB redirection.</span></span>

<span data-ttu-id="97cf9-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="97cf9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97cf9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97cf9-109">Syntax</span></span>


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a><span data-ttu-id="97cf9-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="97cf9-110">Property value</span></span>

<span data-ttu-id="97cf9-111">**true** si l’appareil est un facultatif ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="97cf9-111">**true** if the device is a optional; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="97cf9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97cf9-112">Requirements</span></span>



| <span data-ttu-id="97cf9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97cf9-113">Requirement</span></span> | <span data-ttu-id="97cf9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="97cf9-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97cf9-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97cf9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="97cf9-116">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="97cf9-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="97cf9-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97cf9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="97cf9-118">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="97cf9-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="97cf9-119">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="97cf9-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="97cf9-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97cf9-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="97cf9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="97cf9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97cf9-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97cf9-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="97cf9-123">IID</span><span class="sxs-lookup"><span data-stu-id="97cf9-123">IID</span></span><br/>                      | <span data-ttu-id="97cf9-124">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="97cf9-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="97cf9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97cf9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97cf9-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="97cf9-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





