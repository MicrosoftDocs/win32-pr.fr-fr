---
description: Se produit lorsqu’un IInkTablet est supprimé du système.
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: InkPicture. TabletRemoved, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05b097b4dcf15c618e3316066be962b52803e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210623"
---
# <a name="inkpicturetabletremoved-event"></a><span data-ttu-id="b659c-103">InkPicture. TabletRemoved, événement</span><span class="sxs-lookup"><span data-stu-id="b659c-103">InkPicture.TabletRemoved event</span></span>

<span data-ttu-id="b659c-104">Se produit lorsqu’un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) est supprimé du système.</span><span class="sxs-lookup"><span data-stu-id="b659c-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b659c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b659c-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="b659c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b659c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b659c-107">*TabletId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b659c-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b659c-108">Valeur de type long qui a été utilisée comme ID de l’objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) qui a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="b659c-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b659c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b659c-109">Return value</span></span>

<span data-ttu-id="b659c-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b659c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b659c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b659c-111">Remarks</span></span>

<span data-ttu-id="b659c-112">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="b659c-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="b659c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b659c-113">Requirements</span></span>



| <span data-ttu-id="b659c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b659c-114">Requirement</span></span> | <span data-ttu-id="b659c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b659c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b659c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b659c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b659c-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b659c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b659c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b659c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b659c-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b659c-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b659c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b659c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b659c-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b659c-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b659c-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b659c-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b659c-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b659c-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b659c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b659c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b659c-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b659c-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b659c-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="b659c-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




