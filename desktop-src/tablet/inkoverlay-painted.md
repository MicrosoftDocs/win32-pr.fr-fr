---
description: Se produit lorsque l’objet InkOverlay ou le contrôle InkPicture s’est correctement redessiné.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Événement InkOverlay. peint (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485761"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="46438-103">InkOverlay. peint, événement</span><span class="sxs-lookup"><span data-stu-id="46438-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="46438-104">Se produit lorsque l’objet [**InkOverlay**](inkoverlay-class.md) ou le contrôle [InkPicture](inkpicture-control-reference.md) s’est correctement redessiné.</span><span class="sxs-lookup"><span data-stu-id="46438-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="46438-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46438-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="46438-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46438-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46438-107">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46438-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46438-108">Contexte de périphérique sur lequel l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="46438-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="46438-109">*Rect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46438-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46438-110">[**InkRectangle**](inkrectangle-class.md) qui a été redessiné.</span><span class="sxs-lookup"><span data-stu-id="46438-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46438-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46438-111">Return value</span></span>

<span data-ttu-id="46438-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="46438-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46438-113">Notes</span><span class="sxs-lookup"><span data-stu-id="46438-113">Remarks</span></span>

<span data-ttu-id="46438-114">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="46438-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="46438-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46438-115">Requirements</span></span>



| <span data-ttu-id="46438-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46438-116">Requirement</span></span> | <span data-ttu-id="46438-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="46438-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46438-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46438-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46438-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46438-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="46438-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46438-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46438-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="46438-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="46438-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="46438-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="46438-123"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="46438-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="46438-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="46438-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="46438-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46438-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="46438-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46438-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46438-127">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="46438-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




