---
title: IMsRdpDeviceV2 propriété DeviceText
description: Contient le texte de l’appareil.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceText
- Services Bureau à distance de la propriété DeviceText, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété DeviceText
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200544"
---
# <a name="imsrdpdevicev2devicetext-property"></a><span data-ttu-id="2b77e-106">IMsRdpDeviceV2 ::D propriété eviceText</span><span class="sxs-lookup"><span data-stu-id="2b77e-106">IMsRdpDeviceV2::DeviceText property</span></span>

<span data-ttu-id="2b77e-107">Contient le texte de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b77e-107">Contains the device text.</span></span> <span data-ttu-id="2b77e-108">Il s’agit du nom que Windows affiche à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2b77e-108">This is the name that Windows displays to the user.</span></span>

<span data-ttu-id="2b77e-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2b77e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b77e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b77e-110">Syntax</span></span>


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a><span data-ttu-id="2b77e-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2b77e-111">Property value</span></span>

<span data-ttu-id="2b77e-112">Nom complet du périphérique.</span><span class="sxs-lookup"><span data-stu-id="2b77e-112">The display name for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b77e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b77e-113">Requirements</span></span>



| <span data-ttu-id="2b77e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b77e-114">Requirement</span></span> | <span data-ttu-id="2b77e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b77e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b77e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b77e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b77e-117">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="2b77e-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="2b77e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b77e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b77e-119">Windows Server 2008 R2 avec SP1</span><span class="sxs-lookup"><span data-stu-id="2b77e-119">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="2b77e-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2b77e-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b77e-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b77e-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b77e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2b77e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b77e-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b77e-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b77e-124">IID</span><span class="sxs-lookup"><span data-stu-id="2b77e-124">IID</span></span><br/>                      | <span data-ttu-id="2b77e-125">IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="2b77e-125">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="2b77e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b77e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b77e-127">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="2b77e-127">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





