---
description: Se produit après la suppression des objets IInkStrokeDisp de la propriété Ink.
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: InkPicture. StrokesDeleted, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521383"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="7655b-103">InkPicture. StrokesDeleted, événement</span><span class="sxs-lookup"><span data-stu-id="7655b-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="7655b-104">Se produit après la suppression des objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="7655b-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="7655b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7655b-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="7655b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7655b-106">Parameters</span></span>

<span data-ttu-id="7655b-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7655b-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7655b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7655b-108">Return value</span></span>

<span data-ttu-id="7655b-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7655b-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7655b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7655b-110">Remarks</span></span>

<span data-ttu-id="7655b-111">Il n’y a aucune donnée d’événement.</span><span class="sxs-lookup"><span data-stu-id="7655b-111">There is no event data.</span></span>

<span data-ttu-id="7655b-112">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOEStrokesDeleted.</span><span class="sxs-lookup"><span data-stu-id="7655b-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="7655b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7655b-113">Requirements</span></span>



| <span data-ttu-id="7655b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7655b-114">Requirement</span></span> | <span data-ttu-id="7655b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7655b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7655b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7655b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7655b-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7655b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7655b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7655b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7655b-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7655b-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7655b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7655b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7655b-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7655b-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7655b-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7655b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="7655b-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7655b-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7655b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7655b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7655b-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="7655b-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




