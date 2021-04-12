---
description: Se produit lorsque la roulette de la souris se déplace alors que le contrôle InkPicture a le focus.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: InkPicture. MouseWheel, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319421"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="cbac5-103">InkPicture. MouseWheel, événement</span><span class="sxs-lookup"><span data-stu-id="cbac5-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="cbac5-104">Se produit lorsque la roulette de la souris se déplace alors que le contrôle [InkPicture](inkpicture-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="cbac5-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbac5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbac5-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="cbac5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbac5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbac5-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-108">Bouton qui a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="cbac5-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="cbac5-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-111">*Delta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-112">Distance de rotation de la roulette de la souris.</span><span class="sxs-lookup"><span data-stu-id="cbac5-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-113">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-114">Coordonnée x, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="cbac5-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-115">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-116">Coordonnée y, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="cbac5-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-117">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-118">VARIANTE \_ true pour annuler l’événement **MouseWheel** pour le contrôle parent ; sinon, variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="cbac5-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbac5-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbac5-119">Return value</span></span>

<span data-ttu-id="cbac5-120">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cbac5-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbac5-121">Notes</span><span class="sxs-lookup"><span data-stu-id="cbac5-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbac5-122">Les paramètres *x* et *y* sont en pixels, et non pas les unités HIMETRIC associées au système de coordonnées de l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="cbac5-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="cbac5-123">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application qui ne prend pas en charge le stylet et que ce type d’application fait uniquement référence aux pixels.</span><span class="sxs-lookup"><span data-stu-id="cbac5-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="cbac5-124">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="cbac5-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="cbac5-125">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="cbac5-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbac5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbac5-126">Requirements</span></span>



| <span data-ttu-id="cbac5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbac5-127">Requirement</span></span> | <span data-ttu-id="cbac5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbac5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbac5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbac5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cbac5-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbac5-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cbac5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbac5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cbac5-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbac5-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cbac5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbac5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbac5-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cbac5-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cbac5-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cbac5-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbac5-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbac5-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cbac5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbac5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbac5-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="cbac5-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

