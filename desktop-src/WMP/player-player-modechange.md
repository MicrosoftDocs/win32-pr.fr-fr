---
title: Événement Player. ModeChange
description: L’événement ModeChange se produit lorsqu’un mode du lecteur Windows Media est modifié. | Événement Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Événement ModeChange lecteur Windows Media
- Événement ModeChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528667"
---
# <a name="playermodechange-event"></a><span data-ttu-id="f4f55-107">Événement Player. ModeChange</span><span class="sxs-lookup"><span data-stu-id="f4f55-107">Player.ModeChange event</span></span>

<span data-ttu-id="f4f55-108">L’événement **ModeChange** se produit lorsqu’un mode du lecteur Windows Media est modifié.</span><span class="sxs-lookup"><span data-stu-id="f4f55-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f55-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4f55-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="f4f55-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4f55-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f55-111">*ModeName*</span><span class="sxs-lookup"><span data-stu-id="f4f55-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="f4f55-112">**Chaîne** indiquant le mode qui a été modifié.</span><span class="sxs-lookup"><span data-stu-id="f4f55-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="f4f55-113">Contient l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4f55-113">Contains one of the following values.</span></span>



| <span data-ttu-id="f4f55-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f55-114">Value</span></span>   | <span data-ttu-id="f4f55-115">Description</span><span class="sxs-lookup"><span data-stu-id="f4f55-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="f4f55-116">lecture aléatoire</span><span class="sxs-lookup"><span data-stu-id="f4f55-116">shuffle</span></span> | <span data-ttu-id="f4f55-117">Les pistes sont lues dans un ordre aléatoire.</span><span class="sxs-lookup"><span data-stu-id="f4f55-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="f4f55-118">loop</span><span class="sxs-lookup"><span data-stu-id="f4f55-118">loop</span></span>    | <span data-ttu-id="f4f55-119">L’intégralité de la séquence de pistes est lue à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="f4f55-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f4f55-120">*NewValue*</span><span class="sxs-lookup"><span data-stu-id="f4f55-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="f4f55-121">**Valeur booléenne** indiquant le nouvel État du mode spécifié.</span><span class="sxs-lookup"><span data-stu-id="f4f55-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f55-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4f55-122">Return value</span></span>

<span data-ttu-id="f4f55-123">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f4f55-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4f55-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f4f55-124">Remarks</span></span>

<span data-ttu-id="f4f55-125">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="f4f55-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="f4f55-126">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="f4f55-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f55-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4f55-127">Requirements</span></span>



| <span data-ttu-id="f4f55-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4f55-128">Requirement</span></span> | <span data-ttu-id="f4f55-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f55-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f55-130">Version</span><span class="sxs-lookup"><span data-stu-id="f4f55-130">Version</span></span><br/> | <span data-ttu-id="f4f55-131">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f4f55-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f4f55-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f4f55-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="f4f55-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f55-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f55-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4f55-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f55-135">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="f4f55-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f4f55-136">**Paramètres. getMode**</span><span class="sxs-lookup"><span data-stu-id="f4f55-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="f4f55-137">**Paramètres. setMode**</span><span class="sxs-lookup"><span data-stu-id="f4f55-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





