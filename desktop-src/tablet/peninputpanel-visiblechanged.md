---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel est affiché ou masqué.
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: Événement PenInputPanel. VisibleChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538377"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="18403-104">Événement PenInputPanel. VisibleChanged</span><span class="sxs-lookup"><span data-stu-id="18403-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="18403-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="18403-105">Deprecated.</span></span> <span data-ttu-id="18403-106">Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="18403-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="18403-107">Se produit lorsque l’objet [**PenInputPanel**](peninputpanel-class.md) est affiché ou masqué.</span><span class="sxs-lookup"><span data-stu-id="18403-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="18403-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18403-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="18403-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18403-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18403-110">*NewVisibility* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="18403-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18403-111">**Variante \_ TRUE** pour faire en sorte que l’objet [**PenInputPanel**](peninputpanel-class.md) devienne visible ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="18403-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18403-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18403-112">Return value</span></span>

<span data-ttu-id="18403-113">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="18403-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="18403-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="18403-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18403-115">Notes</span><span class="sxs-lookup"><span data-stu-id="18403-115">Remarks</span></span>

<span data-ttu-id="18403-116">L’événement **VisibleChanged** s’applique à la cible de pointage du panneau de saisie Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="18403-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="18403-117">Toutefois, il n’est pas déclenché lorsque la cible de survol se développe pour afficher le panneau de saisie complet du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="18403-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="18403-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18403-118">Requirements</span></span>



| <span data-ttu-id="18403-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18403-119">Requirement</span></span> | <span data-ttu-id="18403-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="18403-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18403-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18403-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18403-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18403-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="18403-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18403-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18403-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="18403-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="18403-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="18403-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="18403-126"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="18403-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="18403-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="18403-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="18403-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18403-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="18403-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18403-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18403-130">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="18403-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




