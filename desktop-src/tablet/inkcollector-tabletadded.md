---
description: Se produit lorsqu’un IInkTablet est ajouté au système.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Événement InkCollector. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18f66a45570b269d36efc012f543a8b25e23f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951006"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="ba3fb-103">Événement InkCollector. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="ba3fb-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="ba3fb-104">Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba3fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba3fb-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="ba3fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba3fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba3fb-107">*Tablette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba3fb-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba3fb-108">Objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba3fb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba3fb-109">Return value</span></span>

<span data-ttu-id="ba3fb-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba3fb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ba3fb-111">Remarks</span></span>

<span data-ttu-id="ba3fb-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="ba3fb-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3fb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba3fb-113">Requirements</span></span>



| <span data-ttu-id="ba3fb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba3fb-114">Requirement</span></span> | <span data-ttu-id="ba3fb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba3fb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3fb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba3fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3fb-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba3fb-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ba3fb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba3fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3fb-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba3fb-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ba3fb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba3fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba3fb-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ba3fb-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ba3fb-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba3fb-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba3fb-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba3fb-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ba3fb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba3fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3fb-125">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="ba3fb-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="ba3fb-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="ba3fb-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




