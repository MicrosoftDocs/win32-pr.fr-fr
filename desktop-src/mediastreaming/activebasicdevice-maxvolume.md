---
title: ActiveBasicDevice MaxVolume, propriété (PlayToDevice. h)
description: Obtient le volume maximal pris en charge par l’appareil.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- API de diffusion multimédia en continu des propriétés MaxVolume
- API de diffusion multimédia en continu des propriétés MaxVolume, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48c25ef6c0e25c35ba07914c00fb063b4e8dc79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466890"
---
# <a name="activebasicdevicemaxvolume-property"></a><span data-ttu-id="87fbf-106">ActiveBasicDevice :: MaxVolume, propriété</span><span class="sxs-lookup"><span data-stu-id="87fbf-106">ActiveBasicDevice::MaxVolume property</span></span>

<span data-ttu-id="87fbf-107">Obtient le volume maximal pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="87fbf-107">Gets the maximum volume supported by the device.</span></span>

<span data-ttu-id="87fbf-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="87fbf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fbf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87fbf-109">Syntax</span></span>


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a><span data-ttu-id="87fbf-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="87fbf-110">Property value</span></span>

<span data-ttu-id="87fbf-111">Pointeur vers une valeur **UInt32** qui spécifie le volume maximal pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="87fbf-111">A pointer to a **UINT32** that specifies the maximum volume supported by the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fbf-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87fbf-112">Requirements</span></span>



| <span data-ttu-id="87fbf-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87fbf-113">Requirement</span></span> | <span data-ttu-id="87fbf-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="87fbf-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="87fbf-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87fbf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="87fbf-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87fbf-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="87fbf-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87fbf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="87fbf-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87fbf-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87fbf-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="87fbf-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="87fbf-120"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="87fbf-120"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="87fbf-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="87fbf-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87fbf-122"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87fbf-122"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="87fbf-123">DLL</span><span class="sxs-lookup"><span data-stu-id="87fbf-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87fbf-124"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87fbf-124"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87fbf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87fbf-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="87fbf-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87fbf-126">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

