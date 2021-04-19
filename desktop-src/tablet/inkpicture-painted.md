---
description: Se produit lorsque le contrôle InkPicture s’est correctement redessiné.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: InkPicture. peint, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534597"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="6aa0b-103">InkPicture. peint (événement)</span><span class="sxs-lookup"><span data-stu-id="6aa0b-103">InkPicture.Painted event</span></span>

<span data-ttu-id="6aa0b-104">Se produit lorsque le contrôle [InkPicture](inkpicture-control-reference.md) s’est correctement redessiné.</span><span class="sxs-lookup"><span data-stu-id="6aa0b-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aa0b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6aa0b-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="6aa0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6aa0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aa0b-107">*HDC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6aa0b-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa0b-108">Contexte de périphérique sur lequel l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="6aa0b-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6aa0b-109">*Rect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6aa0b-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aa0b-110">[**InkRectangle**](inkrectangle-class.md) qui a été redessiné.</span><span class="sxs-lookup"><span data-stu-id="6aa0b-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aa0b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6aa0b-111">Return value</span></span>

<span data-ttu-id="6aa0b-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6aa0b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aa0b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6aa0b-113">Remarks</span></span>

<span data-ttu-id="6aa0b-114">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** avec l’ID DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="6aa0b-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aa0b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6aa0b-115">Requirements</span></span>



| <span data-ttu-id="6aa0b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6aa0b-116">Requirement</span></span> | <span data-ttu-id="6aa0b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6aa0b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa0b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa0b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa0b-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6aa0b-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6aa0b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa0b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa0b-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6aa0b-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6aa0b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6aa0b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aa0b-123"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6aa0b-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6aa0b-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6aa0b-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="6aa0b-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6aa0b-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6aa0b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aa0b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aa0b-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6aa0b-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




