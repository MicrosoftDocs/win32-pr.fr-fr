---
description: Se produit lorsqu’un utilisateur clique sur le contrôle InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: InkPicture. Click, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867729"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="92def-103">InkPicture. Click, événement</span><span class="sxs-lookup"><span data-stu-id="92def-103">InkPicture.Click event</span></span>

<span data-ttu-id="92def-104">Se produit lorsqu’un utilisateur clique sur le contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="92def-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="92def-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92def-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="92def-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92def-106">Parameters</span></span>

<span data-ttu-id="92def-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="92def-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92def-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92def-108">Return value</span></span>

<span data-ttu-id="92def-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="92def-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92def-110">Notes</span><span class="sxs-lookup"><span data-stu-id="92def-110">Remarks</span></span>

<span data-ttu-id="92def-111">Le clic sur un contrôle génère des événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) en plus de l’événement Click.</span><span class="sxs-lookup"><span data-stu-id="92def-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="92def-112">Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="92def-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="92def-113">Si l’événement **Click** contient du code, l’événement [**DblClick**](inkpicture-dblclick.md) ne se déclenchera jamais, car l’événement **Click** est le premier événement déclenché entre les deux.</span><span class="sxs-lookup"><span data-stu-id="92def-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="92def-114">Par conséquent, le clic de souris est intercepté par l’événement **Click** , si bien que l’événement **DblClick** ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="92def-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="92def-115">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="92def-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="92def-116">L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEClick**.</span><span class="sxs-lookup"><span data-stu-id="92def-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92def-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92def-117">Requirements</span></span>



| <span data-ttu-id="92def-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92def-118">Requirement</span></span> | <span data-ttu-id="92def-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="92def-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92def-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92def-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92def-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92def-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="92def-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92def-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92def-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="92def-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="92def-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="92def-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92def-125"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="92def-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="92def-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="92def-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="92def-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92def-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="92def-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92def-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92def-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="92def-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




