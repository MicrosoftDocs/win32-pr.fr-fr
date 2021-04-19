---
description: Se produit lorsqu’un IInkTablet est ajouté au système.
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: InkOverlay. TabletAdded, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c2faadcbf87e0772afb8f417c97a4be546e08b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541986"
---
# <a name="inkoverlaytabletadded-event"></a><span data-ttu-id="a437a-103">Événement InkOverlay. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="a437a-103">InkOverlay.TabletAdded event</span></span>

<span data-ttu-id="a437a-104">Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="a437a-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a437a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a437a-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="a437a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a437a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a437a-107">*Tablette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a437a-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a437a-108">Objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="a437a-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a437a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a437a-109">Return value</span></span>

<span data-ttu-id="a437a-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a437a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a437a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a437a-111">Remarks</span></span>

<span data-ttu-id="a437a-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="a437a-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="a437a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a437a-113">Requirements</span></span>



| <span data-ttu-id="a437a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a437a-114">Requirement</span></span> | <span data-ttu-id="a437a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a437a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a437a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a437a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a437a-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a437a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a437a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a437a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a437a-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a437a-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a437a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a437a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a437a-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a437a-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a437a-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a437a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a437a-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a437a-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a437a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a437a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a437a-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="a437a-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="a437a-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="a437a-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




