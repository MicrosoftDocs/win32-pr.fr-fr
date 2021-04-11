---
description: Se produit avant que le contrôle InkPicture ne se redessine lui-même.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: InkPicture. Painting, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203426"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="3b826-103">InkPicture. Paint, événement</span><span class="sxs-lookup"><span data-stu-id="3b826-103">InkPicture.Painting event</span></span>

<span data-ttu-id="3b826-104">Se produit avant que le contrôle [InkPicture](inkpicture-control-reference.md) ne se redessine lui-même.</span><span class="sxs-lookup"><span data-stu-id="3b826-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b826-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b826-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="3b826-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b826-107">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b826-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b826-108">Contexte de périphérique sur lequel la peinture aura lieu.</span><span class="sxs-lookup"><span data-stu-id="3b826-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="3b826-109">*Rect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b826-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b826-110">Rectangle d’encre à repeindre.</span><span class="sxs-lookup"><span data-stu-id="3b826-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="3b826-111">*Autoriser* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3b826-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b826-112">Indique si le redessin est effectué.</span><span class="sxs-lookup"><span data-stu-id="3b826-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b826-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b826-113">Return value</span></span>

<span data-ttu-id="3b826-114">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3b826-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b826-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3b826-115">Remarks</span></span>

<span data-ttu-id="3b826-116">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="3b826-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b826-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b826-117">Requirements</span></span>



| <span data-ttu-id="3b826-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b826-118">Requirement</span></span> | <span data-ttu-id="3b826-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b826-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b826-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b826-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3b826-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b826-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3b826-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b826-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3b826-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b826-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3b826-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b826-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b826-125"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3b826-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3b826-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3b826-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b826-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b826-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3b826-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b826-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b826-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3b826-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




