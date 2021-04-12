---
description: Se produit lorsque le pointeur de la souris se trouve sur le contrôle InkPicture et qu’un bouton de la souris est enfoncé.
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: InkPicture. MouseDown, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203818"
---
# <a name="inkpicturemousedown-event"></a><span data-ttu-id="83b46-103">InkPicture. MouseDown, événement</span><span class="sxs-lookup"><span data-stu-id="83b46-103">InkPicture.MouseDown event</span></span>

<span data-ttu-id="83b46-104">Se produit lorsque le pointeur de la souris se trouve sur le contrôle [InkPicture](inkpicture-control-reference.md) et qu’un bouton de la souris est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="83b46-104">Occurs when the mouse pointer is over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="83b46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83b46-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="83b46-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83b46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83b46-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83b46-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b46-108">Bouton qui a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="83b46-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="83b46-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83b46-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b46-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="83b46-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="83b46-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83b46-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b46-112">Coordonnée x, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="83b46-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="83b46-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83b46-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83b46-114">Coordonnée y, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="83b46-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="83b46-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83b46-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83b46-116">**Variante \_ TRUE** pour annuler cet événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="83b46-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83b46-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83b46-117">Return value</span></span>

<span data-ttu-id="83b46-118">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="83b46-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83b46-119">Notes</span><span class="sxs-lookup"><span data-stu-id="83b46-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="83b46-120">Les paramètres pX et pY sont en pixels, et non pas les unités HIMETRIC associées au système de coordonnées de l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="83b46-120">The parameters pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="83b46-121">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application qui ne prend pas en charge le stylet et que ce type d’application fait uniquement référence aux pixels.</span><span class="sxs-lookup"><span data-stu-id="83b46-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="83b46-122">Certains contrôles s’appuient sur une relation spécifique entre les événements **MouseDown**, [**MouseMove**](inkpicture-mousemove.md)et [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="83b46-122">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkpicture-mousemove.md), and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="83b46-123">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="83b46-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="83b46-124">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="83b46-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="83b46-125">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="83b46-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="83b46-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83b46-126">Requirements</span></span>



| <span data-ttu-id="83b46-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83b46-127">Requirement</span></span> | <span data-ttu-id="83b46-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="83b46-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83b46-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83b46-129">Minimum supported client</span></span><br/> | <span data-ttu-id="83b46-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83b46-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="83b46-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83b46-131">Minimum supported server</span></span><br/> | <span data-ttu-id="83b46-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="83b46-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="83b46-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="83b46-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="83b46-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="83b46-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="83b46-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="83b46-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="83b46-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83b46-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="83b46-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83b46-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83b46-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="83b46-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

