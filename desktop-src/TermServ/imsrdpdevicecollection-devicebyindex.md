---
title: IMsRdpDeviceCollection propriété DeviceByIndex
description: Récupère l’appareil au niveau de l’index spécifié.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceByIndex
- Services Bureau à distance de la propriété DeviceByIndex, interface IMsRdpDeviceCollection
- Services Bureau à distance de l’interface IMsRdpDeviceCollection, propriété DeviceByIndex
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12d763d4c147efa26e904a1903149504ee557ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467018"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a><span data-ttu-id="46066-106">IMsRdpDeviceCollection ::D propriété eviceByIndex</span><span class="sxs-lookup"><span data-stu-id="46066-106">IMsRdpDeviceCollection::DeviceByIndex property</span></span>

<span data-ttu-id="46066-107">Récupère l’appareil au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="46066-107">Retrieves the device at the specified index.</span></span>

<span data-ttu-id="46066-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="46066-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46066-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46066-109">Syntax</span></span>


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="46066-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="46066-110">Property value</span></span>

<span data-ttu-id="46066-111">Pointeur d’interface [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="46066-111">An [**IMsRdpDevice**](imsrdpdevice.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="46066-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="46066-112">Error codes</span></span>

<span data-ttu-id="46066-113">Si la méthode est réussie, **S \_ OK** est retourné.</span><span class="sxs-lookup"><span data-stu-id="46066-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="46066-114">Toute autre valeur **HRESULT** indique que l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="46066-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="46066-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46066-115">Requirements</span></span>



| <span data-ttu-id="46066-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46066-116">Requirement</span></span> | <span data-ttu-id="46066-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="46066-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="46066-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46066-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46066-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46066-119">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="46066-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46066-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46066-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46066-121">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="46066-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="46066-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="46066-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46066-123"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="46066-124">DLL</span><span class="sxs-lookup"><span data-stu-id="46066-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46066-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46066-125"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="46066-126">IID</span><span class="sxs-lookup"><span data-stu-id="46066-126">IID</span></span><br/>                      | <span data-ttu-id="46066-127">IID \_ IMsRdpDeviceCollection est défini comme 56540617-D281-488C-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="46066-127">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46066-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46066-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46066-129">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="46066-129">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

 





