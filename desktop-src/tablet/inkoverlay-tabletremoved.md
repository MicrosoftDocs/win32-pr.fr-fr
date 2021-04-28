---
description: L’événement InkOverlay. TabletRemoved-se produit lorsqu’un IInkTablet est supprimé du système.
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: InkOverlay. TabletRemoved, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5572ec4c8afd664ef96534e93c402ec2141f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086647"
---
# <a name="inkoverlaytabletremoved-event"></a><span data-ttu-id="fd217-103">Événement InkOverlay. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="fd217-103">InkOverlay.TabletRemoved event</span></span>

<span data-ttu-id="fd217-104">Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="fd217-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd217-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd217-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="fd217-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fd217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd217-107">*TabletId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fd217-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd217-108">Valeur de type long qui a été utilisée comme ID de l’objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="fd217-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd217-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fd217-109">Return value</span></span>

<span data-ttu-id="fd217-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fd217-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd217-111">Notes </span><span class="sxs-lookup"><span data-stu-id="fd217-111">Remarks</span></span>

<span data-ttu-id="fd217-112">Cette méthode d’événement est définie dans les \_ dispinterfaces IInkCollectorEvents, \_ IInkOverlayEvents et \_ IInkPictureEvents (dispinterfaces) avec l’ID DISPID \_ ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="fd217-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd217-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fd217-113">Requirements</span></span>



| <span data-ttu-id="fd217-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fd217-114">Requirement</span></span> | <span data-ttu-id="fd217-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd217-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd217-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd217-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd217-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fd217-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fd217-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd217-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd217-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fd217-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fd217-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd217-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd217-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fd217-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fd217-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fd217-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="fd217-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd217-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fd217-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd217-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd217-125">**InkOverlay, classe**</span><span class="sxs-lookup"><span data-stu-id="fd217-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="fd217-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="fd217-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




