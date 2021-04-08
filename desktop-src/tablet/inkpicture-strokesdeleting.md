---
description: Se produit avant la suppression des objets IInkStrokeDisp de la propriété Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: InkPicture. StrokesDeleting, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034970"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="e716f-103">InkPicture. StrokesDeleting, événement</span><span class="sxs-lookup"><span data-stu-id="e716f-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="e716f-104">Se produit avant la suppression des objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la propriété [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="e716f-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e716f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e716f-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="e716f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e716f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e716f-107">*Traits* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e716f-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e716f-108">Collection [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) supprimée lorsque l’événement **StrokesDeleting** est déclenché.</span><span class="sxs-lookup"><span data-stu-id="e716f-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e716f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e716f-109">Return value</span></span>

<span data-ttu-id="e716f-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e716f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e716f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e716f-111">Remarks</span></span>

<span data-ttu-id="e716f-112">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOEStrokesDeleting.</span><span class="sxs-lookup"><span data-stu-id="e716f-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="e716f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e716f-113">Requirements</span></span>



| <span data-ttu-id="e716f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e716f-114">Requirement</span></span> | <span data-ttu-id="e716f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e716f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e716f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e716f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e716f-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e716f-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e716f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e716f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e716f-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e716f-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e716f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e716f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e716f-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e716f-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e716f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e716f-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="e716f-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e716f-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e716f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e716f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e716f-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e716f-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

