---
title: ActiveBasicDevice IsSearchSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge la recherche.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- API de diffusion multimédia en continu des propriétés IsSearchSupported
- API de diffusion multimédia en continu des propriétés IsSearchSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff97b20697388b1e3079f6993b97b948fa12091e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385207"
---
# <a name="activebasicdeviceissearchsupported-property"></a><span data-ttu-id="6a989-106">ActiveBasicDevice :: IsSearchSupported, propriété</span><span class="sxs-lookup"><span data-stu-id="6a989-106">ActiveBasicDevice::IsSearchSupported property</span></span>

<span data-ttu-id="6a989-107">Obtient une valeur qui indique si l’appareil prend en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="6a989-107">Gets a value that indicates if the device supports search.</span></span>

<span data-ttu-id="6a989-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a989-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a989-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a989-109">Syntax</span></span>


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="6a989-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6a989-110">Property value</span></span>

<span data-ttu-id="6a989-111">Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge la recherche.</span><span class="sxs-lookup"><span data-stu-id="6a989-111">A pointer to a **boolean** that indicates if the device supports search.</span></span>

<span data-ttu-id="6a989-112">**true** si l’appareil prend en charge la recherche ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="6a989-112">**true** if the device supports search; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a989-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a989-113">Requirements</span></span>



| <span data-ttu-id="6a989-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a989-114">Requirement</span></span> | <span data-ttu-id="6a989-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a989-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a989-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a989-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a989-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a989-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6a989-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a989-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a989-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a989-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a989-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a989-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a989-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a989-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a989-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="6a989-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a989-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a989-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="6a989-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6a989-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a989-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a989-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a989-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a989-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a989-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a989-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

