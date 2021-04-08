---
title: ActiveBasicDevice IsAudioSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge l’audio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API de diffusion multimédia en continu des propriétés IsAudioSupported
- API de diffusion multimédia en continu des propriétés IsAudioSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66058da9dcdbac0ed1100b0ef21a4ed530d45a68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033235"
---
# <a name="activebasicdeviceisaudiosupported-property"></a><span data-ttu-id="85c45-106">ActiveBasicDevice :: IsAudioSupported, propriété</span><span class="sxs-lookup"><span data-stu-id="85c45-106">ActiveBasicDevice::IsAudioSupported property</span></span>

<span data-ttu-id="85c45-107">Obtient une valeur qui indique si l’appareil prend en charge l’audio.</span><span class="sxs-lookup"><span data-stu-id="85c45-107">Gets a value that indicates if the device supports audio.</span></span>

<span data-ttu-id="85c45-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85c45-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c45-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85c45-109">Syntax</span></span>


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="85c45-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="85c45-110">Property value</span></span>

<span data-ttu-id="85c45-111">Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge l’audio.</span><span class="sxs-lookup"><span data-stu-id="85c45-111">A pointer to a **boolean** that indicates if the device supports audio.</span></span>

<span data-ttu-id="85c45-112">**true** si l’appareil prend en charge l’audio ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="85c45-112">**true** if the device supports audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c45-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85c45-113">Requirements</span></span>



| <span data-ttu-id="85c45-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85c45-114">Requirement</span></span> | <span data-ttu-id="85c45-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="85c45-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c45-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85c45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="85c45-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85c45-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="85c45-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85c45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="85c45-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85c45-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85c45-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="85c45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c45-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c45-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="85c45-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="85c45-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85c45-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85c45-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="85c45-124">DLL</span><span class="sxs-lookup"><span data-stu-id="85c45-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85c45-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85c45-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c45-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85c45-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="85c45-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85c45-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

