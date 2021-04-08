---
description: Se produit lorsque l’utilisateur dessine un nouvel objet IInkStrokeDisp sur n’importe quel objet IInkTablet.
ms.assetid: fac5104d-d0da-40b1-a4a6-00a34718d09f
title: InkEdit. Stroke, événement (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d21abde9deb565f207a44ddd44b51681f1bfa6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759538"
---
# <a name="inkeditstroke-event"></a><span data-ttu-id="eeabe-103">InkEdit. Stroke (événement)</span><span class="sxs-lookup"><span data-stu-id="eeabe-103">InkEdit.Stroke event</span></span>

<span data-ttu-id="eeabe-104">Se produit lorsque l’utilisateur dessine un nouvel objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) sur n’importe quel objet [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .</span><span class="sxs-lookup"><span data-stu-id="eeabe-104">Occurs when the user draws a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object on any [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeabe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eeabe-105">Syntax</span></span>


```C++
HRESULT Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="eeabe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eeabe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeabe-107">*Curseur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eeabe-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeabe-108">Objet [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="eeabe-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="eeabe-109">*Trait* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eeabe-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeabe-110">Objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) collecté.</span><span class="sxs-lookup"><span data-stu-id="eeabe-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="eeabe-111">*Annuler* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eeabe-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eeabe-112">**Variante \_ TRUE** pour annuler la collection de l’objet [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ; **Variante \_ FALSe** pour collecter l’objet **IInkStrokeDisp** et continuer avec le **trait** même.</span><span class="sxs-lookup"><span data-stu-id="eeabe-112">**VARIANT\_TRUE** to cancel the collection of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object; **VARIANT\_FALSE** to collect the **IInkStrokeDisp** object and continue with the **Stroke** even.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeabe-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eeabe-113">Return value</span></span>

<span data-ttu-id="eeabe-114">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eeabe-114">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eeabe-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eeabe-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeabe-116">Notes</span><span class="sxs-lookup"><span data-stu-id="eeabe-116">Remarks</span></span>

<span data-ttu-id="eeabe-117">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="eeabe-117">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="eeabe-118">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeStroke.</span><span class="sxs-lookup"><span data-stu-id="eeabe-118">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeStroke.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeabe-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeabe-119">Requirements</span></span>



| <span data-ttu-id="eeabe-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeabe-120">Requirement</span></span> | <span data-ttu-id="eeabe-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeabe-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeabe-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeabe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eeabe-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeabe-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eeabe-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeabe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eeabe-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeabe-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eeabe-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="eeabe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeabe-127"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eeabe-127"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eeabe-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eeabe-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="eeabe-129"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeabe-129"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eeabe-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeabe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeabe-131">InkEdit</span><span class="sxs-lookup"><span data-stu-id="eeabe-131">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="eeabe-132">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="eeabe-132">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="eeabe-133">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="eeabe-133">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

