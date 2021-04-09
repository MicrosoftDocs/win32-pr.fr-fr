---
title: IMsRdpDevice propriété DeviceInstanceId
description: Récupère l’identificateur d’instance d’appareil de l’appareil.
ms.assetid: 54bdda17-39da-4821-9ac3-2ce80f5015f4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceInstanceId
- Services Bureau à distance de la propriété DeviceInstanceId, interface IMsRdpDevice
- Services Bureau à distance de l’interface IMsRdpDevice, propriété DeviceInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDevice.DeviceInstanceId
- IMsRdpDevice.get_DeviceInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a159911e4294e2207ad4ae989d4ef9e390384c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942883"
---
# <a name="imsrdpdevicedeviceinstanceid-property"></a><span data-ttu-id="2b0bb-106">IMsRdpDevice ::D propriété eviceInstanceId</span><span class="sxs-lookup"><span data-stu-id="2b0bb-106">IMsRdpDevice::DeviceInstanceId property</span></span>

<span data-ttu-id="2b0bb-107">Récupère l’identificateur d’instance d’appareil de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b0bb-107">Retrieves the device instance identifier of the device.</span></span>

<span data-ttu-id="2b0bb-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2b0bb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b0bb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b0bb-109">Syntax</span></span>


```C++
HRESULT get_DeviceInstanceId(
  [out] BSTR *pDevInstanceId
);
```



## <a name="property-value"></a><span data-ttu-id="2b0bb-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2b0bb-110">Property value</span></span>

<span data-ttu-id="2b0bb-111">Identificateur de l’instance de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2b0bb-111">The device instance identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2b0bb-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2b0bb-112">Error codes</span></span>

<span data-ttu-id="2b0bb-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="2b0bb-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="2b0bb-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="2b0bb-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b0bb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b0bb-115">Requirements</span></span>



| <span data-ttu-id="2b0bb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b0bb-116">Requirement</span></span> | <span data-ttu-id="2b0bb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b0bb-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0bb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b0bb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0bb-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b0bb-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2b0bb-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b0bb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0bb-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b0bb-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2b0bb-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="2b0bb-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="2b0bb-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b0bb-123"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b0bb-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2b0bb-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b0bb-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b0bb-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2b0bb-126">IID</span><span class="sxs-lookup"><span data-stu-id="2b0bb-126">IID</span></span><br/>                      | <span data-ttu-id="2b0bb-127">IID \_ IMsRdpDevice est défini en tant que 60c3b9c8-9E92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="2b0bb-127">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="2b0bb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b0bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0bb-129">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="2b0bb-129">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

 





