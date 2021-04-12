---
description: Se produit lors d’un double-clic sur l’objet InkCollector ou InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Événement InkOverlay. DoubleClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4baddc89e309b7d64ba2294827b58956b3e6c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209928"
---
# <a name="inkoverlaydoubleclick-event"></a><span data-ttu-id="7410a-103">InkOverlay. DoubleClick, événement</span><span class="sxs-lookup"><span data-stu-id="7410a-103">InkOverlay.DoubleClick event</span></span>

<span data-ttu-id="7410a-104">Se produit lors d’un double-clic sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7410a-104">Occurs when the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="7410a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7410a-105">Syntax</span></span>


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="7410a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7410a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7410a-107">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7410a-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7410a-108">Indique si l’événement doit être annulé pour le contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="7410a-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7410a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7410a-109">Return value</span></span>

<span data-ttu-id="7410a-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7410a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7410a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7410a-111">Remarks</span></span>

<span data-ttu-id="7410a-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ IPEDblClick.</span><span class="sxs-lookup"><span data-stu-id="7410a-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEDblClick.</span></span>

## <a name="requirements"></a><span data-ttu-id="7410a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7410a-113">Requirements</span></span>



| <span data-ttu-id="7410a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7410a-114">Requirement</span></span> | <span data-ttu-id="7410a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7410a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7410a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7410a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7410a-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7410a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7410a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7410a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7410a-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7410a-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7410a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7410a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7410a-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7410a-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7410a-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7410a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="7410a-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7410a-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7410a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7410a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7410a-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="7410a-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




