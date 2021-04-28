---
description: Événement InkCollector. CursorOutOfRange-se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: a3a570ed-570b-4579-b120-ed5457630bc2
title: Événement InkCollector. CursorOutOfRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e14e674d5cb7c3da7f2a1e684a0e916e637106e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110277"
---
# <a name="inkcollectorcursoroutofrange-event"></a><span data-ttu-id="4bf85-103">Événement InkCollector. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="4bf85-103">InkCollector.CursorOutOfRange event</span></span>

<span data-ttu-id="4bf85-104">Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.</span><span class="sxs-lookup"><span data-stu-id="4bf85-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf85-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bf85-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="4bf85-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bf85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf85-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4bf85-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf85-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="4bf85-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf85-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4bf85-109">Return value</span></span>

<span data-ttu-id="4bf85-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4bf85-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bf85-111">Notes </span><span class="sxs-lookup"><span data-stu-id="4bf85-111">Remarks</span></span>

<span data-ttu-id="4bf85-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="4bf85-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="4bf85-113">L’événement **CursorOutOfRange** est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink.</span><span class="sxs-lookup"><span data-stu-id="4bf85-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="4bf85-114">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="4bf85-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="4bf85-115">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="4bf85-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf85-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bf85-116">Requirements</span></span>



| <span data-ttu-id="4bf85-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bf85-117">Requirement</span></span> | <span data-ttu-id="4bf85-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bf85-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf85-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bf85-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4bf85-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bf85-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4bf85-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bf85-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4bf85-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bf85-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4bf85-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bf85-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bf85-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4bf85-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4bf85-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4bf85-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="4bf85-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bf85-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4bf85-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bf85-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf85-128">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="4bf85-128">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="4bf85-129">**Événement CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="4bf85-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="4bf85-130">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="4bf85-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




