---
title: ActiveBasicDevice IsMuteSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si l’appareil prend en charge le silence de l’audio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- API de diffusion multimédia en continu des propriétés IsMuteSupported
- API de diffusion multimédia en continu des propriétés IsMuteSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsMuteSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcec2e4520bd3b15b715c01e4369da87887355e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465743"
---
# <a name="activebasicdeviceismutesupported-property"></a><span data-ttu-id="10083-106">ActiveBasicDevice :: IsMuteSupported, propriété</span><span class="sxs-lookup"><span data-stu-id="10083-106">ActiveBasicDevice::IsMuteSupported property</span></span>

<span data-ttu-id="10083-107">Obtient une valeur qui indique si l’appareil prend en charge le silence de l’audio.</span><span class="sxs-lookup"><span data-stu-id="10083-107">Gets a value that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="10083-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="10083-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="10083-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10083-109">Syntax</span></span>


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="10083-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="10083-110">Property value</span></span>

<span data-ttu-id="10083-111">Pointeur vers une **valeur booléenne** qui indique si l’appareil prend en charge le silence de l’audio.</span><span class="sxs-lookup"><span data-stu-id="10083-111">A pointer to a **boolean** that indicates if the device supports muting the audio.</span></span>

<span data-ttu-id="10083-112">**true** si l’appareil prend en charge le silence de l’audio ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="10083-112">**true** if the device supports muting the audio; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="10083-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10083-113">Requirements</span></span>



| <span data-ttu-id="10083-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10083-114">Requirement</span></span> | <span data-ttu-id="10083-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="10083-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="10083-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10083-116">Minimum supported client</span></span><br/> | <span data-ttu-id="10083-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10083-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="10083-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10083-118">Minimum supported server</span></span><br/> | <span data-ttu-id="10083-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="10083-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="10083-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="10083-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="10083-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="10083-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="10083-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="10083-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="10083-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10083-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="10083-124">DLL</span><span class="sxs-lookup"><span data-stu-id="10083-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10083-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10083-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10083-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10083-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="10083-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="10083-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

