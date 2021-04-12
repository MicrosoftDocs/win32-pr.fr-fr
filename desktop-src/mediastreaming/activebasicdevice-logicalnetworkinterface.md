---
title: ActiveBasicDevice LogicalNetworkInterface, propriété (PlayToDevice. h)
description: Obtient l’ID de l’interface de réseau logique.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- API de diffusion multimédia en continu des propriétés LogicalNetworkInterface
- API de diffusion multimédia en continu des propriétés LogicalNetworkInterface, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété LogicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384508"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a><span data-ttu-id="a47b7-106">ActiveBasicDevice :: LogicalNetworkInterface, propriété</span><span class="sxs-lookup"><span data-stu-id="a47b7-106">ActiveBasicDevice::LogicalNetworkInterface property</span></span>

<span data-ttu-id="a47b7-107">Obtient l’ID de l’interface de réseau logique.</span><span class="sxs-lookup"><span data-stu-id="a47b7-107">Gets the id of the logical network interface.</span></span>

<span data-ttu-id="a47b7-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a47b7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a47b7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a47b7-109">Syntax</span></span>


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a><span data-ttu-id="a47b7-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a47b7-110">Property value</span></span>

<span data-ttu-id="a47b7-111">Pointeur vers un **GUID** qui spécifie l’ID de l’interface de réseau logique.</span><span class="sxs-lookup"><span data-stu-id="a47b7-111">A pointer to a **GUID** that specifies the id of the logical network interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a47b7-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a47b7-112">Requirements</span></span>



| <span data-ttu-id="a47b7-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a47b7-113">Requirement</span></span> | <span data-ttu-id="a47b7-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a47b7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a47b7-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a47b7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a47b7-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a47b7-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a47b7-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a47b7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a47b7-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a47b7-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a47b7-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a47b7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a47b7-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a47b7-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="a47b7-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="a47b7-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a47b7-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a47b7-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="a47b7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a47b7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a47b7-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a47b7-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a47b7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a47b7-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a47b7-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a47b7-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

