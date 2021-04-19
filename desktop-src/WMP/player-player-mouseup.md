---
title: Player. MouseUp, événement
description: L’événement MouseUp se produit lorsque l’utilisateur relâche un bouton de la souris. | Player. MouseUp, événement
ms.assetid: 0f209fc4-2aad-46b1-84ba-2bfbecbe2930
keywords:
- Événement MouseUp lecteur Windows Media
- Événement MouseUp lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement MouseUp
topic_type:
- apiref
api_name:
- Player.MouseUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50883ed8e5ea5696bd3aef1c5170959814de3026
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538092"
---
# <a name="playermouseup-event"></a><span data-ttu-id="24de6-107">Player. MouseUp, événement</span><span class="sxs-lookup"><span data-stu-id="24de6-107">Player.MouseUp event</span></span>

<span data-ttu-id="24de6-108">L’événement **MouseUp** se produit lorsque l’utilisateur relâche un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="24de6-108">The **MouseUp** event occurs when the user releases a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="24de6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24de6-109">Syntax</span></span>


```JScript
Player.MouseUp(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="24de6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24de6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24de6-111">*Nbouton*</span><span class="sxs-lookup"><span data-stu-id="24de6-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="24de6-112">**Nombre** (**int**) spécifiant un champ de bits avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="24de6-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="24de6-113">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="24de6-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="24de6-114">Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="24de6-114">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="24de6-115">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="24de6-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="24de6-116">**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="24de6-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="24de6-117">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="24de6-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="24de6-118">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="24de6-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="24de6-119">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="24de6-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="24de6-120">*Rotation*</span><span class="sxs-lookup"><span data-stu-id="24de6-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="24de6-121">**Nombre** (**long**) spécifiant la coordonnée x du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="24de6-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="24de6-122">*Années*</span><span class="sxs-lookup"><span data-stu-id="24de6-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="24de6-123">**Nombre** (**long**) spécifiant la coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="24de6-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24de6-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24de6-124">Return value</span></span>

<span data-ttu-id="24de6-125">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="24de6-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24de6-126">Notes</span><span class="sxs-lookup"><span data-stu-id="24de6-126">Remarks</span></span>

<span data-ttu-id="24de6-127">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="24de6-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="24de6-128">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="24de6-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="24de6-129">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="24de6-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="24de6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24de6-130">Requirements</span></span>



| <span data-ttu-id="24de6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24de6-131">Requirement</span></span> | <span data-ttu-id="24de6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="24de6-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24de6-133">Version</span><span class="sxs-lookup"><span data-stu-id="24de6-133">Version</span></span><br/> | <span data-ttu-id="24de6-134">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="24de6-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="24de6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="24de6-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="24de6-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24de6-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24de6-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24de6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24de6-138">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="24de6-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





