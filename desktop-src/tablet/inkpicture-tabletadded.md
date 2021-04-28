---
description: L’événement InkPicture. TabletAdded se produit lorsqu’un IInkTablet est ajouté au système.
ms.assetid: 5df10efd-7055-43fa-881f-67eb5fd6adcf
title: InkPicture. TabletAdded, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c5121b668f27034a04230311ee88ebb7564802
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113657"
---
# <a name="inkpicturetabletadded-event"></a><span data-ttu-id="8ea5e-103">InkPicture. TabletAdded, événement</span><span class="sxs-lookup"><span data-stu-id="8ea5e-103">InkPicture.TabletAdded event</span></span>

<span data-ttu-id="8ea5e-104">Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea5e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ea5e-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="8ea5e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ea5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea5e-107">*Tablette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ea5e-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea5e-108">Objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea5e-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8ea5e-109">Return value</span></span>

<span data-ttu-id="8ea5e-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea5e-111">Notes </span><span class="sxs-lookup"><span data-stu-id="8ea5e-111">Remarks</span></span>

<span data-ttu-id="8ea5e-112">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="8ea5e-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea5e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ea5e-113">Requirements</span></span>



| <span data-ttu-id="8ea5e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ea5e-114">Requirement</span></span> | <span data-ttu-id="8ea5e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ea5e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea5e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ea5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea5e-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ea5e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8ea5e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ea5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea5e-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ea5e-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8ea5e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ea5e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ea5e-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea5e-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8ea5e-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8ea5e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ea5e-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ea5e-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8ea5e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ea5e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea5e-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="8ea5e-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="8ea5e-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="8ea5e-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




