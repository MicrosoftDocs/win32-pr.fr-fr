---
title: Événement Player. Click
description: L’événement Click se produit lorsque l’utilisateur clique sur un bouton de la souris.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Événement de clic sur le lecteur Windows Media
- Événement Click lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement Click
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545482"
---
# <a name="playerclick-event"></a><span data-ttu-id="d7e2e-106">Événement Player. Click</span><span class="sxs-lookup"><span data-stu-id="d7e2e-106">Player.Click event</span></span>

<span data-ttu-id="d7e2e-107">L’événement **Click** se produit lorsque l’utilisateur clique sur un bouton de la souris.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-107">The **Click** event occurs when the user clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e2e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7e2e-108">Syntax</span></span>


```JScript
Player.Click(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="d7e2e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7e2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e2e-110">*Nbouton*</span><span class="sxs-lookup"><span data-stu-id="d7e2e-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e2e-111">**Nombre** (**int**) spécifiant un champ de bits avec bits correspondant au bouton gauche (bit 0), bouton droit (bit 1) et bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="d7e2e-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="d7e2e-112">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="d7e2e-113">Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="d7e2e-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="d7e2e-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e2e-115">**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="d7e2e-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="d7e2e-116">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="d7e2e-117">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="d7e2e-118">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d7e2e-119">*Rotation*</span><span class="sxs-lookup"><span data-stu-id="d7e2e-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e2e-120">**Nombre** (**long**) spécifiant la coordonnée x du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d7e2e-121">*Années*</span><span class="sxs-lookup"><span data-stu-id="d7e2e-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="d7e2e-122">**Nombre** (**long**) spécifiant la coordonnée y du pointeur de la souris par rapport au coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e2e-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7e2e-123">Return value</span></span>

<span data-ttu-id="d7e2e-124">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7e2e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="d7e2e-125">Remarks</span></span>

<span data-ttu-id="d7e2e-126">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="d7e2e-127">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="d7e2e-128">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e2e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7e2e-129">Requirements</span></span>



| <span data-ttu-id="d7e2e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7e2e-130">Requirement</span></span> | <span data-ttu-id="d7e2e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7e2e-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e2e-132">Version</span><span class="sxs-lookup"><span data-stu-id="d7e2e-132">Version</span></span><br/> | <span data-ttu-id="d7e2e-133">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d7e2e-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d7e2e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d7e2e-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="d7e2e-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7e2e-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7e2e-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7e2e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e2e-137">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="d7e2e-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





