---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque l’objet PenInputPanel est déplacé.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Événement PenInputPanel. PanelMoving (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543136"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="b8904-104">Événement PenInputPanel. PanelMoving</span><span class="sxs-lookup"><span data-stu-id="b8904-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="b8904-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b8904-105">Deprecated.</span></span> <span data-ttu-id="b8904-106">Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b8904-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="b8904-107">Se produit lorsque l’objet [**PenInputPanel**](peninputpanel-class.md) est déplacé.</span><span class="sxs-lookup"><span data-stu-id="b8904-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8904-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8904-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="b8904-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8904-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8904-110">À *gauche* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b8904-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8904-111">Nouvel axe horizontal, ou axe des x, position du bord gauche de l’objet [**PenInputPanel**](peninputpanel-class.md) , en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="b8904-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b8904-112">En *haut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b8904-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8904-113">Nouvel axe vertical, ou axe y, position du bord gauche de l’objet [**PenInputPanel**](peninputpanel-class.md) , en coordonnées d’écran.</span><span class="sxs-lookup"><span data-stu-id="b8904-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8904-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8904-114">Return value</span></span>

<span data-ttu-id="b8904-115">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b8904-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8904-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8904-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8904-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b8904-117">Remarks</span></span>

<span data-ttu-id="b8904-118">L’événement **PanelMoving** est conçu pour être utilisé pour modifier la position du panneau de saisie du stylet en modifiant les paramètres de *gauche* et du *haut* .</span><span class="sxs-lookup"><span data-stu-id="b8904-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="b8904-119">Les méthodes [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) et [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) forcent l’objet [**PenInputPanel**](peninputpanel-class.md) à appeler son code de positionnement automatique qui déclenche un événement **PanelMoving** .</span><span class="sxs-lookup"><span data-stu-id="b8904-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="b8904-120">Par conséquent, l’appel de ces méthodes à l’intérieur d’un gestionnaire **PanelMoving** peut entraîner une boucle infinie récursive.</span><span class="sxs-lookup"><span data-stu-id="b8904-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8904-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8904-121">Requirements</span></span>



| <span data-ttu-id="b8904-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8904-122">Requirement</span></span> | <span data-ttu-id="b8904-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8904-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8904-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8904-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b8904-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8904-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b8904-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8904-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b8904-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8904-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b8904-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8904-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8904-129"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b8904-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b8904-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8904-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8904-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8904-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b8904-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8904-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8904-133">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="b8904-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




