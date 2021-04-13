---
description: Se produit lors d’un double-clic sur le contrôle InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: InkPicture. DblClick, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320130"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="df1bb-103">InkPicture. DblClick, événement</span><span class="sxs-lookup"><span data-stu-id="df1bb-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="df1bb-104">Se produit lors d’un double-clic sur le contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="df1bb-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df1bb-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="df1bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df1bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df1bb-107">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="df1bb-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="df1bb-108">Indique si l’événement doit être annulé pour le contrôle parent.</span><span class="sxs-lookup"><span data-stu-id="df1bb-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df1bb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df1bb-109">Return value</span></span>

<span data-ttu-id="df1bb-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="df1bb-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1bb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="df1bb-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="df1bb-112">Pour faire la distinction entre les boutons gauche, droit et central de la souris, utilisez les événements [**MouseDown**](inkpicture-mousedown.md) et [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="df1bb-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="df1bb-113">Si l’événement [**Click**](inkpicture-click.md) contient du code, l’événement **DblClick** ne se déclenchera jamais.</span><span class="sxs-lookup"><span data-stu-id="df1bb-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="df1bb-114">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="df1bb-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="df1bb-115">L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEDblClick**.</span><span class="sxs-lookup"><span data-stu-id="df1bb-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="df1bb-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df1bb-116">Requirements</span></span>



| <span data-ttu-id="df1bb-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df1bb-117">Requirement</span></span> | <span data-ttu-id="df1bb-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="df1bb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df1bb-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df1bb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="df1bb-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df1bb-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="df1bb-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df1bb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="df1bb-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="df1bb-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="df1bb-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="df1bb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="df1bb-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="df1bb-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="df1bb-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df1bb-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="df1bb-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df1bb-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="df1bb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df1bb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df1bb-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="df1bb-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




