---
description: Se produit lorsqu’un utilisateur clique sur le contrôle InkEdit.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit. Click, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519495"
---
# <a name="inkeditclick-event"></a><span data-ttu-id="36034-103">InkEdit. Click, événement</span><span class="sxs-lookup"><span data-stu-id="36034-103">InkEdit.Click event</span></span>

<span data-ttu-id="36034-104">Se produit lorsqu’un utilisateur clique sur le contrôle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="36034-104">Occurs when a user clicks the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="36034-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36034-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="36034-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36034-106">Parameters</span></span>

<span data-ttu-id="36034-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="36034-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36034-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36034-108">Return value</span></span>

<span data-ttu-id="36034-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="36034-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36034-110">Notes</span><span class="sxs-lookup"><span data-stu-id="36034-110">Remarks</span></span>

<span data-ttu-id="36034-111">Le clic sur un contrôle génère des événements [**MouseDown**](inkedit-mousedown.md) et [**MouseUp**](inkedit-mouseup.md) en plus de l’événement Click.</span><span class="sxs-lookup"><span data-stu-id="36034-111">Clicking a control generates [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="36034-112">Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkedit-mousedown.md) et [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="36034-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span>

 

<span data-ttu-id="36034-113">Si l’événement **Click** contient du code, l’événement [**DblClick**](inkedit-dblclick.md) ne se déclenchera jamais, car l’événement **Click** est le premier événement déclenché entre les deux.</span><span class="sxs-lookup"><span data-stu-id="36034-113">If there is code in the **Click** event, the [**DblClick**](inkedit-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="36034-114">Par conséquent, le clic de souris est intercepté par l’événement **Click** , si bien que l’événement **DblClick** ne se produit pas.</span><span class="sxs-lookup"><span data-stu-id="36034-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="36034-115">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="36034-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="36034-116">L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IeeClick**.</span><span class="sxs-lookup"><span data-stu-id="36034-116">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36034-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36034-117">Requirements</span></span>



| <span data-ttu-id="36034-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36034-118">Requirement</span></span> | <span data-ttu-id="36034-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="36034-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36034-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36034-120">Minimum supported client</span></span><br/> | <span data-ttu-id="36034-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36034-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36034-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36034-122">Minimum supported server</span></span><br/> | <span data-ttu-id="36034-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="36034-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="36034-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="36034-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="36034-125"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="36034-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="36034-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="36034-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="36034-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36034-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="36034-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36034-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36034-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="36034-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




