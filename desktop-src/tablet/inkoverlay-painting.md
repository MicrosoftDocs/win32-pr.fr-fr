---
description: Se produit avant que l’objet InkOverlay ou InkPicture ne soit entièrement redessiné.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: InkOverlay. Painting, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529902"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="da88c-103">InkOverlay. Paint, événement</span><span class="sxs-lookup"><span data-stu-id="da88c-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="da88c-104">Se produit avant que l’objet [**InkOverlay**](inkoverlay-class.md) ou [InkPicture](inkpicture-control-reference.md) ne soit entièrement redessiné.</span><span class="sxs-lookup"><span data-stu-id="da88c-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="da88c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da88c-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="da88c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da88c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da88c-107">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da88c-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da88c-108">Contexte de périphérique sur lequel la peinture aura lieu.</span><span class="sxs-lookup"><span data-stu-id="da88c-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="da88c-109">*Rect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da88c-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da88c-110">Rectangle qui doit être repeint.</span><span class="sxs-lookup"><span data-stu-id="da88c-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="da88c-111">*Autoriser* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="da88c-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da88c-112">Indique si le redessin est effectué.</span><span class="sxs-lookup"><span data-stu-id="da88c-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da88c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da88c-113">Return value</span></span>

<span data-ttu-id="da88c-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="da88c-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da88c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="da88c-115">Remarks</span></span>

<span data-ttu-id="da88c-116">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="da88c-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="da88c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da88c-117">Requirements</span></span>



| <span data-ttu-id="da88c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da88c-118">Requirement</span></span> | <span data-ttu-id="da88c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="da88c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da88c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da88c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da88c-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da88c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="da88c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da88c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da88c-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="da88c-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="da88c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="da88c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="da88c-125"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="da88c-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da88c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da88c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="da88c-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da88c-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="da88c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da88c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da88c-129">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="da88c-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




