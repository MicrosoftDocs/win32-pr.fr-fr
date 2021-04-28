---
description: L’événement InkOverlay. DoubleClick se produit lors d’un double-clic sur l’objet InkCollector ou InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Événement InkOverlay. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c358a6c44ccda9be9dc4d0dd1d3e81e4a983ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086827"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="6caca-103">InkOverlay. DoubleClick, événement</span><span class="sxs-lookup"><span data-stu-id="6caca-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="6caca-104">Se produit lors d’un double-clic sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="6caca-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6caca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6caca-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6caca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6caca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6caca-107">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6caca-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6caca-108">Indique si l’événement doit être annulé pour le contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="6caca-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6caca-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6caca-109">Return value</span></span>

<span data-ttu-id="6caca-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6caca-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6caca-111">Notes </span><span class="sxs-lookup"><span data-stu-id="6caca-111">Remarks</span></span>

<span data-ttu-id="6caca-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="6caca-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="6caca-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6caca-113">Requirements</span></span>



| <span data-ttu-id="6caca-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6caca-114">Requirement</span></span> | <span data-ttu-id="6caca-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6caca-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6caca-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6caca-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6caca-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6caca-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6caca-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6caca-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6caca-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6caca-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6caca-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6caca-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6caca-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6caca-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6caca-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6caca-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6caca-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6caca-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6caca-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6caca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6caca-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="6caca-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




