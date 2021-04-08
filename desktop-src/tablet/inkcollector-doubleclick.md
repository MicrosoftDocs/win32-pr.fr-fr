---
description: Se produit lors d’un double-clic sur l’objet InkCollector ou InkOverlay.
ms.assetid: 48c3a695-0ec4-46ea-b1ea-a846e39d53ec
title: Événement InkCollector. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17faa459e207cd8891a13cf90f587b277d404772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862094"
---
# <a name="inkcollectordoubleclick-event"></a><span data-ttu-id="5a2b9-103">Événement InkCollector. DoubleClick</span><span class="sxs-lookup"><span data-stu-id="5a2b9-103">InkCollector.DoubleClick event</span></span>

<span data-ttu-id="5a2b9-104">Se produit lors d’un double-clic sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5a2b9-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a2b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a2b9-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="5a2b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a2b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a2b9-107">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5a2b9-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a2b9-108">**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="5a2b9-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a2b9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a2b9-109">Return value</span></span>

<span data-ttu-id="5a2b9-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="5a2b9-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a2b9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="5a2b9-111">Remarks</span></span>

<span data-ttu-id="5a2b9-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="5a2b9-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a2b9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a2b9-113">Requirements</span></span>



| <span data-ttu-id="5a2b9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a2b9-114">Requirement</span></span> | <span data-ttu-id="5a2b9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a2b9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a2b9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a2b9-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5a2b9-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5a2b9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a2b9-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a2b9-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="5a2b9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a2b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a2b9-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5a2b9-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5a2b9-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a2b9-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a2b9-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a2b9-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="5a2b9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a2b9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a2b9-125">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="5a2b9-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> </dl>

 

 




