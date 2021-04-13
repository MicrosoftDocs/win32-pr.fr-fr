---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel change entre des dispositions.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Événement PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320125"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="24ef7-104">Événement PenInputPanel. PanelChanged</span><span class="sxs-lookup"><span data-stu-id="24ef7-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="24ef7-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="24ef7-105">Deprecated.</span></span> <span data-ttu-id="24ef7-106">Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="24ef7-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="24ef7-107">Se produit lorsque l’objet [**PenInputPanel**](peninputpanel-class.md) change entre des dispositions.</span><span class="sxs-lookup"><span data-stu-id="24ef7-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ef7-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24ef7-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="24ef7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24ef7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ef7-110">*NewPanelType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="24ef7-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24ef7-111">Nouveau type de panneau utilisé pour l’entrée dans l’objet [**PenInputPanel**](peninputpanel-class.md) , après le déclenchement de l’événement **PanelChanged** .</span><span class="sxs-lookup"><span data-stu-id="24ef7-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ef7-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24ef7-112">Return value</span></span>

<span data-ttu-id="24ef7-113">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="24ef7-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="24ef7-114">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24ef7-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="24ef7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="24ef7-115">Remarks</span></span>

<span data-ttu-id="24ef7-116">Lors de la création d’un objet [**PenInputPanel**](peninputpanel-class.md) , l' [**écriture manuscrite**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) est le **PanelType** par défaut.</span><span class="sxs-lookup"><span data-stu-id="24ef7-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="24ef7-117">Si vous modifiez le panneau en définissant la propriété [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) avant que le panneau de saisie du stylet ne devienne actif pour la première fois, un événement **PanelChanged** se produit.</span><span class="sxs-lookup"><span data-stu-id="24ef7-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="24ef7-118">L’événement **PanelChanged** n’est pas déclenché lorsque l’utilisateur change de pavé d’écriture encadrée et boxed.</span><span class="sxs-lookup"><span data-stu-id="24ef7-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="24ef7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24ef7-119">Requirements</span></span>



| <span data-ttu-id="24ef7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24ef7-120">Requirement</span></span> | <span data-ttu-id="24ef7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="24ef7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24ef7-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24ef7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="24ef7-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24ef7-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="24ef7-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24ef7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="24ef7-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="24ef7-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="24ef7-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="24ef7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ef7-127"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="24ef7-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="24ef7-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="24ef7-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="24ef7-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24ef7-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="24ef7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24ef7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ef7-131">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="24ef7-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 
