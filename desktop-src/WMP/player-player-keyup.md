---
title: Player. KeyUp (événement)
description: L’événement KeyUp se produit lorsqu’une touche est relâchée. | Player. KeyUp (événement)
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Événement KeyUp lecteur Windows Media
- Événement KeyUp lecteur Windows Media, classe Player
- Classe de lecteur lecteur Windows Media, événement KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545403"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="7112e-107">Player. KeyUp (événement)</span><span class="sxs-lookup"><span data-stu-id="7112e-107">Player.KeyUp event</span></span>

<span data-ttu-id="7112e-108">L’événement **KeyUp** se produit lorsqu’une touche est relâchée.</span><span class="sxs-lookup"><span data-stu-id="7112e-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="7112e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7112e-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="7112e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7112e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7112e-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="7112e-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="7112e-112">**Nombre** (**int**) spécifiant la touche physique qui est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="7112e-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="7112e-113">Pour connaître les valeurs possibles, consultez [événement Player.](player-player-keydown.md)KeyOut.</span><span class="sxs-lookup"><span data-stu-id="7112e-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="7112e-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="7112e-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="7112e-115">**Nombre** (**int**) spécifiant un champ de bits avec les bits les moins significatifs correspondant à la touche Maj (bit 0), la touche Ctrl (bit 1) et la touche Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="7112e-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="7112e-116">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="7112e-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="7112e-117">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="7112e-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="7112e-118">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="7112e-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7112e-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7112e-119">Return value</span></span>

<span data-ttu-id="7112e-120">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7112e-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7112e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="7112e-121">Remarks</span></span>

<span data-ttu-id="7112e-122">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="7112e-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="7112e-123">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="7112e-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="7112e-124">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7112e-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7112e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7112e-125">Requirements</span></span>



| <span data-ttu-id="7112e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7112e-126">Requirement</span></span> | <span data-ttu-id="7112e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7112e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7112e-128">Version</span><span class="sxs-lookup"><span data-stu-id="7112e-128">Version</span></span><br/> | <span data-ttu-id="7112e-129">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7112e-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="7112e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7112e-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="7112e-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7112e-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7112e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7112e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7112e-133">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="7112e-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





