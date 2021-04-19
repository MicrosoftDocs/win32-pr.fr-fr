---
description: Se produit lorsqu’une touche est relâchée alors que le contrôle InkPicture a le focus.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: InkPicture. KeyUp, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536746"
---
# <a name="inkpicturekeyup-event"></a><span data-ttu-id="63fde-103">InkPicture. KeyUp (événement)</span><span class="sxs-lookup"><span data-stu-id="63fde-103">InkPicture.KeyUp event</span></span>

<span data-ttu-id="63fde-104">Se produit lorsqu’une touche est relâchée alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="63fde-104">Occurs when a key is released while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="63fde-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63fde-105">Syntax</span></span>


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="63fde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63fde-107">*KeyCode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="63fde-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63fde-108">Valeur ASCII de la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="63fde-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="63fde-109">*MAJ* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="63fde-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63fde-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="63fde-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63fde-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63fde-111">Return value</span></span>

<span data-ttu-id="63fde-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="63fde-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63fde-113">Notes</span><span class="sxs-lookup"><span data-stu-id="63fde-113">Remarks</span></span>

<span data-ttu-id="63fde-114">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="63fde-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="63fde-115">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEKeyUp.</span><span class="sxs-lookup"><span data-stu-id="63fde-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="63fde-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63fde-116">Requirements</span></span>



| <span data-ttu-id="63fde-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63fde-117">Requirement</span></span> | <span data-ttu-id="63fde-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="63fde-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63fde-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63fde-119">Minimum supported client</span></span><br/> | <span data-ttu-id="63fde-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63fde-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="63fde-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63fde-121">Minimum supported server</span></span><br/> | <span data-ttu-id="63fde-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="63fde-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="63fde-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="63fde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="63fde-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="63fde-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="63fde-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="63fde-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="63fde-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63fde-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="63fde-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63fde-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63fde-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="63fde-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

