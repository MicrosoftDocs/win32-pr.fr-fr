---
title: ActiveBasicDevice IsSetNextSourceSupported, propriété (PlayToDevice. h)
description: Obtient une valeur qui indique si la définition de la source suivante est prise en charge.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- API de diffusion multimédia en continu des propriétés IsSetNextSourceSupported
- API de diffusion multimédia en continu des propriétés IsSetNextSourceSupported, interface ActiveBasicDevice
- API de diffusion multimédia en continu de l’interface ActiveBasicDevice, propriété IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516094"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a><span data-ttu-id="be9e8-106">ActiveBasicDevice :: IsSetNextSourceSupported, propriété</span><span class="sxs-lookup"><span data-stu-id="be9e8-106">ActiveBasicDevice::IsSetNextSourceSupported property</span></span>

<span data-ttu-id="be9e8-107">Obtient une valeur qui indique si la définition de la source suivante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="be9e8-107">Gets a value that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="be9e8-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="be9e8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9e8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be9e8-109">Syntax</span></span>


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a><span data-ttu-id="be9e8-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="be9e8-110">Property value</span></span>

<span data-ttu-id="be9e8-111">Pointeur vers une **valeur booléenne** qui indique si la définition de la source suivante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="be9e8-111">A pointer to a **boolean** that indicates if setting the next source is supported.</span></span>

<span data-ttu-id="be9e8-112">**true** si la définition de la source suivante est prise en charge ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="be9e8-112">**true** if setting the next source is supported; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9e8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be9e8-113">Requirements</span></span>



| <span data-ttu-id="be9e8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be9e8-114">Requirement</span></span> | <span data-ttu-id="be9e8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="be9e8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9e8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be9e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="be9e8-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be9e8-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be9e8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be9e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="be9e8-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be9e8-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="be9e8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="be9e8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="be9e8-121"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9e8-121"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="be9e8-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="be9e8-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be9e8-123"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be9e8-123"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="be9e8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="be9e8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be9e8-125"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be9e8-125"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9e8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be9e8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="be9e8-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be9e8-127">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

