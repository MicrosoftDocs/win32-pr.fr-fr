---
title: Player. MouseMove (événement)
description: L’événement MouseMove se produit lorsque le pointeur de la souris est déplacé. | Player. MouseMove (événement)
ms.assetid: 026928a3-25a6-4e67-837a-df71c05e49ee
keywords:
- Événement MouseMove lecteur Windows Media
- Événement MouseMove lecteur Windows Media, classe Player
- Classe de lecteur lecteur Windows Media, événement MouseMove
topic_type:
- apiref
api_name:
- Player.MouseMove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a536609ba5e3095fed9826b071084491a81b385f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539606"
---
# <a name="playermousemove-event"></a><span data-ttu-id="71e80-107">Player. MouseMove (événement)</span><span class="sxs-lookup"><span data-stu-id="71e80-107">Player.MouseMove event</span></span>

<span data-ttu-id="71e80-108">L’événement **MouseMove** se produit lorsque le pointeur de la souris est déplacé.</span><span class="sxs-lookup"><span data-stu-id="71e80-108">The **MouseMove** event occurs when the mouse pointer is moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e80-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71e80-109">Syntax</span></span>


```JScript
Player.MouseMove(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="71e80-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71e80-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e80-111">*Nbouton*</span><span class="sxs-lookup"><span data-stu-id="71e80-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="71e80-112">**Nombre** (**int**) spécifiant un champ de bits avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="71e80-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="71e80-113">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="71e80-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="71e80-114">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, l’ensemble ou aucun des boutons est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="71e80-114">Some, all, or none of the bits can be set, indicating that some, all, or none of the buttons are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="71e80-115">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="71e80-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="71e80-116">**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="71e80-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="71e80-117">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="71e80-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="71e80-118">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="71e80-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="71e80-119">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="71e80-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="71e80-120">*Rotation*</span><span class="sxs-lookup"><span data-stu-id="71e80-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="71e80-121">**Nombre** (**long**) spécifiant la coordonnée x du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="71e80-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="71e80-122">*Années*</span><span class="sxs-lookup"><span data-stu-id="71e80-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="71e80-123">**Nombre** (**long**) spécifiant la coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="71e80-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e80-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71e80-124">Return value</span></span>

<span data-ttu-id="71e80-125">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="71e80-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71e80-126">Notes</span><span class="sxs-lookup"><span data-stu-id="71e80-126">Remarks</span></span>

<span data-ttu-id="71e80-127">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="71e80-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="71e80-128">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="71e80-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="71e80-129">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="71e80-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="71e80-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71e80-130">Requirements</span></span>



| <span data-ttu-id="71e80-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71e80-131">Requirement</span></span> | <span data-ttu-id="71e80-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="71e80-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71e80-133">Version</span><span class="sxs-lookup"><span data-stu-id="71e80-133">Version</span></span><br/> | <span data-ttu-id="71e80-134">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="71e80-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="71e80-135">DLL</span><span class="sxs-lookup"><span data-stu-id="71e80-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="71e80-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71e80-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e80-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71e80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e80-138">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="71e80-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





