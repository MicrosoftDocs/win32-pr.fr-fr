---
description: Se produit lors d’un double-clic sur le contrôle InkEdit.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: Événement InkEdit. DblClick (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528339"
---
# <a name="inkeditdblclick-event"></a><span data-ttu-id="149cd-103">InkEdit. DblClick, événement</span><span class="sxs-lookup"><span data-stu-id="149cd-103">InkEdit.DblClick event</span></span>

<span data-ttu-id="149cd-104">Se produit lors d’un double-clic sur le contrôle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="149cd-104">Occurs when the [InkEdit](inkedit-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="149cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="149cd-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="149cd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="149cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="149cd-107">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="149cd-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="149cd-108">**Variante \_ TRUE** pour annuler l’événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="149cd-108">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="149cd-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="149cd-109">Return value</span></span>

<span data-ttu-id="149cd-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="149cd-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="149cd-111">Notes</span><span class="sxs-lookup"><span data-stu-id="149cd-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="149cd-112">Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkedit-mousedown.md) et [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="149cd-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkedit-mousedown.md) and [**MouseUp**](inkedit-mouseup.md) events.</span></span> <span data-ttu-id="149cd-113">Si l’événement [**Click**](inkedit-click.md) contient du code, l’événement **DblClick** ne se déclenchera jamais.</span><span class="sxs-lookup"><span data-stu-id="149cd-113">If there is code in the [**Click**](inkedit-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="149cd-114">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="149cd-114">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="149cd-115">L’interface **\_ IInkEditEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IeeDblClick**.</span><span class="sxs-lookup"><span data-stu-id="149cd-115">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="149cd-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="149cd-116">Requirements</span></span>



| <span data-ttu-id="149cd-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="149cd-117">Requirement</span></span> | <span data-ttu-id="149cd-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="149cd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="149cd-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="149cd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="149cd-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="149cd-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="149cd-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="149cd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="149cd-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="149cd-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="149cd-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="149cd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="149cd-124"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="149cd-124"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="149cd-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="149cd-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="149cd-126"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="149cd-126"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="149cd-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="149cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="149cd-128">InkEdit</span><span class="sxs-lookup"><span data-stu-id="149cd-128">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




