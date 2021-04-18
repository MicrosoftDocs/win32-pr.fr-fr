---
description: Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: InkPicture. CursorOutOfRange, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6a3eb09ca54fcfc4df3135896ea14f9bf56570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519493"
---
# <a name="inkpicturecursoroutofrange-event"></a><span data-ttu-id="52b0f-103">InkPicture. CursorOutOfRange, événement</span><span class="sxs-lookup"><span data-stu-id="52b0f-103">InkPicture.CursorOutOfRange event</span></span>

<span data-ttu-id="52b0f-104">Se produit lorsque le curseur quitte la plage de détection physique (proximité) du contexte de la tablette.</span><span class="sxs-lookup"><span data-stu-id="52b0f-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="52b0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52b0f-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="52b0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52b0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52b0f-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52b0f-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52b0f-108">Objet d' [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) qui a généré l’événement **CursorOutOfRange** .</span><span class="sxs-lookup"><span data-stu-id="52b0f-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52b0f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52b0f-109">Return value</span></span>

<span data-ttu-id="52b0f-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="52b0f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52b0f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="52b0f-111">Remarks</span></span>

<span data-ttu-id="52b0f-112">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="52b0f-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="52b0f-113">L’événement **CursorOutOfRange** est déclenché même en mode SELECT ou Erase, pas seulement en mode Ink.</span><span class="sxs-lookup"><span data-stu-id="52b0f-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="52b0f-114">Pour cela, vous devez surveiller le mode d’édition (que vous êtes chargé de définir) et connaître le mode avant d’interpréter l’événement.</span><span class="sxs-lookup"><span data-stu-id="52b0f-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="52b0f-115">L’avantage de cette exigence est une plus grande liberté d’innover sur la plate-forme grâce à une meilleure connaissance des événements de plateforme.</span><span class="sxs-lookup"><span data-stu-id="52b0f-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="52b0f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52b0f-116">Requirements</span></span>



| <span data-ttu-id="52b0f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52b0f-117">Requirement</span></span> | <span data-ttu-id="52b0f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="52b0f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b0f-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52b0f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52b0f-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52b0f-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="52b0f-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52b0f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52b0f-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="52b0f-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="52b0f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="52b0f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52b0f-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="52b0f-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="52b0f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52b0f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="52b0f-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52b0f-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="52b0f-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52b0f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52b0f-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="52b0f-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="52b0f-129">**Événement CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="52b0f-129">**CursorInRange Event**</span></span>](inkpicture-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="52b0f-130">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="52b0f-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




