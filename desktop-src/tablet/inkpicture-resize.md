---
description: Se produit lorsque le contrôle InkPicture est redimensionné (lorsque les valeurs de propriété Width et/ou Height changent).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: InkPicture. Resize, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034972"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="d1761-103">InkPicture. Resize, événement</span><span class="sxs-lookup"><span data-stu-id="d1761-103">InkPicture.Resize event</span></span>

<span data-ttu-id="d1761-104">Se produit lorsque le contrôle [InkPicture](inkpicture-control-reference.md) est redimensionné (lorsque les valeurs de propriété Width et/ou Height changent).</span><span class="sxs-lookup"><span data-stu-id="d1761-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1761-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1761-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="d1761-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1761-107">*Left*</span><span class="sxs-lookup"><span data-stu-id="d1761-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="d1761-108">Nombre de pixels entre le côté gauche de la fenêtre qui contient le contrôle et le côté gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d1761-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d1761-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="d1761-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="d1761-110">Nombre de pixels à partir du haut de la fenêtre qui contient le contrôle en haut du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d1761-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d1761-111">*Right*</span><span class="sxs-lookup"><span data-stu-id="d1761-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="d1761-112">Nombre de pixels à partir du côté gauche de la fenêtre qui contient le contrôle situé à droite du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d1761-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d1761-113">*Bas*</span><span class="sxs-lookup"><span data-stu-id="d1761-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="d1761-114">Nombre de pixels à partir du haut de la fenêtre qui contient le contrôle en bas du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d1761-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1761-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1761-115">Return value</span></span>

<span data-ttu-id="d1761-116">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1761-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1761-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d1761-117">Remarks</span></span>

<span data-ttu-id="d1761-118">La nouvelle largeur du contrôle en pixels est égale à la différence entre les paramètres de *droite* et de *gauche* .</span><span class="sxs-lookup"><span data-stu-id="d1761-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="d1761-119">De même, la nouvelle hauteur sera égale à la différence entre le *bas* et le *haut*.</span><span class="sxs-lookup"><span data-stu-id="d1761-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="d1761-120">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="d1761-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="d1761-121">L’interface **\_ IInkPictureEvents** implémente l’interface IDispatch avec un identificateur de **DISPID \_ IPEResize**.</span><span class="sxs-lookup"><span data-stu-id="d1761-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1761-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1761-122">Requirements</span></span>



| <span data-ttu-id="d1761-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1761-123">Requirement</span></span> | <span data-ttu-id="d1761-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1761-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1761-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1761-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d1761-126">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1761-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d1761-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1761-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d1761-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1761-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d1761-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1761-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1761-130"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d1761-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d1761-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d1761-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1761-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1761-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d1761-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1761-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1761-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d1761-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




