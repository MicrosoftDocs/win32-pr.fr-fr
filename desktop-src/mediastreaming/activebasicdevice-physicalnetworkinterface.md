---
title: ActiveBasicDevice PhysicalNetworkInterface, propriété (PlayToDevice. h)
description: Obtient l’ID de l’interface réseau physique.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API de diffusion multimédia en continu des propriétés PhysicalNetworkInterface
- API de diffusion multimédia en continu des propriétés PhysicalNetworkInterface, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465742"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a><span data-ttu-id="3b52b-106">ActiveBasicDevice ::P propriété hysicalNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="3b52b-106">ActiveBasicDevice::PhysicalNetworkInterface property</span></span>

<span data-ttu-id="3b52b-107">Obtient l’ID de l’interface réseau physique.</span><span class="sxs-lookup"><span data-stu-id="3b52b-107">Gets the id of the physical network interface.</span></span>

<span data-ttu-id="3b52b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3b52b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b52b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b52b-109">Syntax</span></span>


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="3b52b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3b52b-110">Property value</span></span>

<span data-ttu-id="3b52b-111">Pointeur vers un **GUID** qui spécifie l’ID de l’interface réseau physique.</span><span class="sxs-lookup"><span data-stu-id="3b52b-111">A pointer to a **GUID** that specifies the id of the physical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b52b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b52b-112">Requirements</span></span>



| <span data-ttu-id="3b52b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b52b-113">Requirement</span></span> | <span data-ttu-id="3b52b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b52b-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b52b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b52b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3b52b-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b52b-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3b52b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b52b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3b52b-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b52b-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3b52b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b52b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b52b-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b52b-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b52b-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="3b52b-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b52b-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b52b-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="3b52b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3b52b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b52b-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b52b-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b52b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b52b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b52b-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3b52b-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

