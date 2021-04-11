---
description: Se produit lorsqu’une touche est enfoncée et en position inférieure alors que le contrôle InkPicture a le focus.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: InkPicture. KeyOut, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042830"
---
# <a name="inkpicturekeydown-event"></a><span data-ttu-id="e3dd3-103">InkPicture. KeyOut, événement</span><span class="sxs-lookup"><span data-stu-id="e3dd3-103">InkPicture.KeyDown event</span></span>

<span data-ttu-id="e3dd3-104">Se produit lorsqu’une touche est enfoncée et en position inférieure alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="e3dd3-104">Occurs when a key is pressed and in the down position while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dd3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3dd3-105">Syntax</span></span>


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="e3dd3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3dd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3dd3-107">*KeyCode* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3dd3-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dd3-108">Valeur ASCII de la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="e3dd3-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="e3dd3-109">*MAJ* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3dd3-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3dd3-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="e3dd3-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3dd3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e3dd3-111">Return value</span></span>

<span data-ttu-id="e3dd3-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="e3dd3-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dd3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e3dd3-113">Remarks</span></span>

<span data-ttu-id="e3dd3-114">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="e3dd3-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="e3dd3-115">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEKeyDown.</span><span class="sxs-lookup"><span data-stu-id="e3dd3-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dd3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3dd3-116">Requirements</span></span>



| <span data-ttu-id="e3dd3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3dd3-117">Requirement</span></span> | <span data-ttu-id="e3dd3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3dd3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dd3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dd3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dd3-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3dd3-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e3dd3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dd3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dd3-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3dd3-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e3dd3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3dd3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3dd3-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e3dd3-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e3dd3-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3dd3-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3dd3-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3dd3-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e3dd3-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3dd3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dd3-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e3dd3-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

