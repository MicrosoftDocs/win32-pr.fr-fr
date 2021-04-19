---
description: Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Événement InkCollector. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd009c5f42e6a26cdaf493e97532be7716381c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515229"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="311b9-103">Événement InkCollector. CursorDown</span><span class="sxs-lookup"><span data-stu-id="311b9-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="311b9-104">Se produit lorsque l’info-bulle de curseur contacte la surface de tablette numérique.</span><span class="sxs-lookup"><span data-stu-id="311b9-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="311b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="311b9-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="311b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="311b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311b9-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="311b9-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311b9-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="311b9-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="311b9-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="311b9-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="311b9-110">Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) qui a été démarré lorsque l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) a provoqué le déclenchement de l’événement **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="311b9-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311b9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="311b9-111">Return value</span></span>

<span data-ttu-id="311b9-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="311b9-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="311b9-113">Notes</span><span class="sxs-lookup"><span data-stu-id="311b9-113">Remarks</span></span>

<span data-ttu-id="311b9-114">Cette méthode d’événement est définie dans \_ IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="311b9-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="311b9-115">les \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents implémentent l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="311b9-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="311b9-116">Utilisez cet événement avec précaution, car cela peut avoir un effet néfaste sur les performances de l’encre si un trop grand nombre de code est exécuté dans les gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="311b9-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="311b9-117">Pour améliorer les performances de l’encre en temps réel, masquez ou affichez le curseur de la souris dans les gestionnaires d’événements [**MouseDown**](inkcollector-mousedown.md) et [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="311b9-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="311b9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="311b9-118">Requirements</span></span>



| <span data-ttu-id="311b9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="311b9-119">Requirement</span></span> | <span data-ttu-id="311b9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="311b9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="311b9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="311b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="311b9-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="311b9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="311b9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="311b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="311b9-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="311b9-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="311b9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="311b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="311b9-126"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="311b9-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="311b9-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="311b9-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="311b9-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="311b9-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="311b9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="311b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="311b9-130">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="311b9-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="311b9-131">**Événement CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="311b9-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="311b9-132">**Événement CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="311b9-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="311b9-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="311b9-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="311b9-134">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="311b9-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

