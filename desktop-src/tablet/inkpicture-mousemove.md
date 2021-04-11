---
description: Se produit lorsque le pointeur de la souris est déplacé au-dessus du contrôle InkPicture.
ms.assetid: b4c703da-0e4a-4d4c-9a6c-0e002344fb2f
title: InkPicture. MouseMove, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5540831594674dd279fc14e822d6b3240b014c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203428"
---
# <a name="inkpicturemousemove-event"></a><span data-ttu-id="12f16-103">InkPicture. MouseMove, événement</span><span class="sxs-lookup"><span data-stu-id="12f16-103">InkPicture.MouseMove event</span></span>

<span data-ttu-id="12f16-104">Se produit lorsque le pointeur de la souris est déplacé au-dessus du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="12f16-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="12f16-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12f16-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="12f16-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12f16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f16-107">*Bouton* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12f16-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f16-108">Bouton qui a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="12f16-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="12f16-109">*MAJ* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12f16-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f16-110">État de la touche Maj.</span><span class="sxs-lookup"><span data-stu-id="12f16-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="12f16-111">*PX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12f16-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f16-112">Coordonnée x, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="12f16-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="12f16-113">*py* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12f16-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12f16-114">Coordonnée y, en pixels, de l’objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="12f16-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="12f16-115">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="12f16-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12f16-116">**Variante \_ TRUE** pour annuler cet événement pour le contrôle parent ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="12f16-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f16-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12f16-117">Return value</span></span>

<span data-ttu-id="12f16-118">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="12f16-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12f16-119">Notes</span><span class="sxs-lookup"><span data-stu-id="12f16-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12f16-120">Les paramètres *PX* et *py* sont en pixels, et non pas les unités HIMETRIC associées au système de coordonnées de l’espace d’encre.</span><span class="sxs-lookup"><span data-stu-id="12f16-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="12f16-121">Cela est dû au fait que cet événement remplace l’événement de souris associé d’une application qui ne prend pas en charge le stylet et que ce type d’application fait uniquement référence aux pixels.</span><span class="sxs-lookup"><span data-stu-id="12f16-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="12f16-122">Certains contrôles s’appuient sur une relation spécifique entre les événements [**MouseDown**](inkpicture-mousedown.md), **MouseMove** et [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="12f16-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), **MouseMove**, and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="12f16-123">L’annulation de certains de ces événements peut avoir des résultats imprévus.</span><span class="sxs-lookup"><span data-stu-id="12f16-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="12f16-124">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="12f16-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="12f16-125">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="12f16-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f16-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12f16-126">Requirements</span></span>



| <span data-ttu-id="12f16-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12f16-127">Requirement</span></span> | <span data-ttu-id="12f16-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="12f16-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f16-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f16-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12f16-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12f16-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="12f16-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f16-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12f16-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="12f16-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="12f16-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="12f16-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="12f16-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="12f16-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="12f16-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12f16-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="12f16-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12f16-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="12f16-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12f16-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f16-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="12f16-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

