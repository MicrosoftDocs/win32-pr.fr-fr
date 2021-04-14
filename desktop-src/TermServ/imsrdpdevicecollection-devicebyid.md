---
title: IMsRdpDeviceCollection propriété DeviceById
description: Récupère l’appareil avec l’identificateur spécifié.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceById
- Services Bureau à distance de la propriété DeviceById, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, propriété DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465130"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a><span data-ttu-id="730ee-106">IMsRdpDeviceCollection ::D propriété eviceById</span><span class="sxs-lookup"><span data-stu-id="730ee-106">IMsRdpDeviceCollection::DeviceById property</span></span>

<span data-ttu-id="730ee-107">Récupère l’appareil avec l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="730ee-107">Retrieves the device with the specified identifier.</span></span>

<span data-ttu-id="730ee-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="730ee-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="730ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="730ee-109">Syntax</span></span>


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="730ee-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="730ee-110">Property value</span></span>

<span data-ttu-id="730ee-111">Pointeur d’interface [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="730ee-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="730ee-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="730ee-112">Error codes</span></span>

<span data-ttu-id="730ee-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="730ee-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="730ee-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="730ee-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="730ee-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="730ee-115">Requirements</span></span>



| <span data-ttu-id="730ee-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="730ee-116">Requirement</span></span> | <span data-ttu-id="730ee-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="730ee-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="730ee-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="730ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="730ee-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="730ee-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="730ee-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="730ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="730ee-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="730ee-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="730ee-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="730ee-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="730ee-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="730ee-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="730ee-124">DLL</span><span class="sxs-lookup"><span data-stu-id="730ee-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="730ee-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="730ee-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="730ee-126">IID</span><span class="sxs-lookup"><span data-stu-id="730ee-126">IID</span></span><br/>                      | <span data-ttu-id="730ee-127">IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="730ee-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="730ee-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="730ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730ee-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="730ee-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





