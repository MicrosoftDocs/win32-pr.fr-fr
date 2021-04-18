---
title: Player. DoubleClick (événement)
description: L’événement DoubleClick se produit lorsque l’utilisateur double-clique sur un bouton de la souris.
ms.assetid: e2055cff-e4b0-49e3-a93a-7084789b6842
keywords:
- Événement DoubleClick lecteur Windows Media
- Événement DoubleClick lecteur Windows Media, classe Player
- Classe player lecteur Windows Media, événement DoubleClick
topic_type:
- apiref
api_name:
- Player.DoubleClick
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3670bfbf3b72fad64f8fb515f5151920b34f52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543214"
---
# <a name="playerdoubleclick-event"></a><span data-ttu-id="81bce-106">Player. DoubleClick (événement)</span><span class="sxs-lookup"><span data-stu-id="81bce-106">Player.DoubleClick event</span></span>

<span data-ttu-id="81bce-107">L’événement **DoubleClick** se produit lorsque l’utilisateur double-clique sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="81bce-107">The **DoubleClick** event occurs when the user double-clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="81bce-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81bce-108">Syntax</span></span>


```JScript
Player.DoubleClick(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="81bce-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81bce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81bce-110">*Nbouton*</span><span class="sxs-lookup"><span data-stu-id="81bce-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="81bce-111">**Nombre** (**int**) spécifiant un champ de bits avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="81bce-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="81bce-112">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="81bce-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="81bce-113">Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="81bce-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="81bce-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="81bce-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="81bce-115">**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="81bce-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="81bce-116">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="81bce-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="81bce-117">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="81bce-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="81bce-118">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="81bce-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="81bce-119">*Rotation*</span><span class="sxs-lookup"><span data-stu-id="81bce-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="81bce-120">**Nombre** (**long**) spécifiant la coordonnée x du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="81bce-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="81bce-121">*Années*</span><span class="sxs-lookup"><span data-stu-id="81bce-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="81bce-122">**Nombre** (**long**) spécifiant la coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="81bce-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81bce-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81bce-123">Return value</span></span>

<span data-ttu-id="81bce-124">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="81bce-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81bce-125">Notes</span><span class="sxs-lookup"><span data-stu-id="81bce-125">Remarks</span></span>

<span data-ttu-id="81bce-126">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="81bce-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="81bce-127">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="81bce-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="81bce-128">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="81bce-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="81bce-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81bce-129">Requirements</span></span>



| <span data-ttu-id="81bce-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81bce-130">Requirement</span></span> | <span data-ttu-id="81bce-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="81bce-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81bce-132">Version</span><span class="sxs-lookup"><span data-stu-id="81bce-132">Version</span></span><br/> | <span data-ttu-id="81bce-133">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="81bce-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="81bce-134">DLL</span><span class="sxs-lookup"><span data-stu-id="81bce-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="81bce-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81bce-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81bce-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81bce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bce-137">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="81bce-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





