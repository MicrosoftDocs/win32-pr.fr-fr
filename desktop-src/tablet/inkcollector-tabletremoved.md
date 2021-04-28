---
description: Événement InkCollector. TabletRemoved-se produit lorsqu’un IInkTablet est supprimé du système.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Événement InkCollector. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df76c27b1a0d47e456f69a789d17ef6343706284
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109997"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="23f69-103">Événement InkCollector. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="23f69-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="23f69-104">Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="23f69-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="23f69-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23f69-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="23f69-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23f69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f69-107">*TabletId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23f69-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23f69-108">Valeur de type long qui a été utilisée comme ID de l’objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="23f69-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f69-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="23f69-109">Return value</span></span>

<span data-ttu-id="23f69-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="23f69-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f69-111">Notes </span><span class="sxs-lookup"><span data-stu-id="23f69-111">Remarks</span></span>

<span data-ttu-id="23f69-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="23f69-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f69-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23f69-113">Requirements</span></span>



| <span data-ttu-id="23f69-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23f69-114">Requirement</span></span> | <span data-ttu-id="23f69-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="23f69-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23f69-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23f69-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23f69-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23f69-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="23f69-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23f69-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23f69-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="23f69-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="23f69-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="23f69-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f69-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="23f69-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="23f69-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23f69-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="23f69-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23f69-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="23f69-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23f69-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f69-125">**InkCollector (classe)**</span><span class="sxs-lookup"><span data-stu-id="23f69-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="23f69-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="23f69-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




