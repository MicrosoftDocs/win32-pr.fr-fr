---
title: Événement Player. PlaylistChange
description: L’événement PlaylistChange se produit lorsqu’une sélection est modifiée. | Événement Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Événement PlaylistChange lecteur Windows Media
- Événement PlaylistChange lecteur Windows Media, classe Player
- Classe de lecteur Windows Media Player, événement PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542292"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="18ac2-107">Événement Player. PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="18ac2-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="18ac2-108">L’événement **PlaylistChange** se produit lorsqu’une sélection est modifiée.</span><span class="sxs-lookup"><span data-stu-id="18ac2-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ac2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18ac2-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="18ac2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18ac2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ac2-111">*Playlist*</span><span class="sxs-lookup"><span data-stu-id="18ac2-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="18ac2-112">Objet **playlist** modifié.</span><span class="sxs-lookup"><span data-stu-id="18ac2-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="18ac2-113">*change*</span><span class="sxs-lookup"><span data-stu-id="18ac2-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="18ac2-114">**Nombre** (**long**) indiquant le type de modification qui s’est produite dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="18ac2-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="18ac2-115">Contient l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="18ac2-115">Contains one of the following values.</span></span>



| <span data-ttu-id="18ac2-116">Number</span><span class="sxs-lookup"><span data-stu-id="18ac2-116">Number</span></span> | <span data-ttu-id="18ac2-117">Nom</span><span class="sxs-lookup"><span data-stu-id="18ac2-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="18ac2-118">0</span><span class="sxs-lookup"><span data-stu-id="18ac2-118">0</span></span>      | <span data-ttu-id="18ac2-119">Unknown</span><span class="sxs-lookup"><span data-stu-id="18ac2-119">Unknown</span></span>       |
| <span data-ttu-id="18ac2-120">1</span><span class="sxs-lookup"><span data-stu-id="18ac2-120">1</span></span>      | <span data-ttu-id="18ac2-121">Effacer</span><span class="sxs-lookup"><span data-stu-id="18ac2-121">Clear</span></span>         |
| <span data-ttu-id="18ac2-122">2</span><span class="sxs-lookup"><span data-stu-id="18ac2-122">2</span></span>      | <span data-ttu-id="18ac2-123">InfoChange</span><span class="sxs-lookup"><span data-stu-id="18ac2-123">InfoChange</span></span>    |
| <span data-ttu-id="18ac2-124">3</span><span class="sxs-lookup"><span data-stu-id="18ac2-124">3</span></span>      | <span data-ttu-id="18ac2-125">Déplacer</span><span class="sxs-lookup"><span data-stu-id="18ac2-125">Move</span></span>          |
| <span data-ttu-id="18ac2-126">4</span><span class="sxs-lookup"><span data-stu-id="18ac2-126">4</span></span>      | <span data-ttu-id="18ac2-127">DELETE</span><span class="sxs-lookup"><span data-stu-id="18ac2-127">Delete</span></span>        |
| <span data-ttu-id="18ac2-128">5</span><span class="sxs-lookup"><span data-stu-id="18ac2-128">5</span></span>      | <span data-ttu-id="18ac2-129">Insérer</span><span class="sxs-lookup"><span data-stu-id="18ac2-129">Insert</span></span>        |
| <span data-ttu-id="18ac2-130">6</span><span class="sxs-lookup"><span data-stu-id="18ac2-130">6</span></span>      | <span data-ttu-id="18ac2-131">Ajouter (Append)</span><span class="sxs-lookup"><span data-stu-id="18ac2-131">Append</span></span>        |
| <span data-ttu-id="18ac2-132">7</span><span class="sxs-lookup"><span data-stu-id="18ac2-132">7</span></span>      | <span data-ttu-id="18ac2-133">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ac2-133">Not supported</span></span> |
| <span data-ttu-id="18ac2-134">8</span><span class="sxs-lookup"><span data-stu-id="18ac2-134">8</span></span>      | <span data-ttu-id="18ac2-135">NameChange,</span><span class="sxs-lookup"><span data-stu-id="18ac2-135">NameChange</span></span>    |
| <span data-ttu-id="18ac2-136">9</span><span class="sxs-lookup"><span data-stu-id="18ac2-136">9</span></span>      | <span data-ttu-id="18ac2-137">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ac2-137">Not supported</span></span> |
| <span data-ttu-id="18ac2-138">10</span><span class="sxs-lookup"><span data-stu-id="18ac2-138">10</span></span>     | <span data-ttu-id="18ac2-139">Trier</span><span class="sxs-lookup"><span data-stu-id="18ac2-139">Sort</span></span>          |



 

<span data-ttu-id="18ac2-140">La constante d’énumération de style C peut être dérivée en préfixant la valeur de nom avec « wmplc ».</span><span class="sxs-lookup"><span data-stu-id="18ac2-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="18ac2-141">Par exemple, la constante de l’État Move est **wmplcMove**.</span><span class="sxs-lookup"><span data-stu-id="18ac2-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ac2-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="18ac2-142">Return value</span></span>

<span data-ttu-id="18ac2-143">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="18ac2-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18ac2-144">Notes</span><span class="sxs-lookup"><span data-stu-id="18ac2-144">Remarks</span></span>

<span data-ttu-id="18ac2-145">La valeur des paramètres d’événement est spécifiée par le lecteur Windows Media et est accessible ou transmise à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné.</span><span class="sxs-lookup"><span data-stu-id="18ac2-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="18ac2-146">Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.</span><span class="sxs-lookup"><span data-stu-id="18ac2-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="18ac2-147">**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="18ac2-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ac2-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18ac2-148">Requirements</span></span>



| <span data-ttu-id="18ac2-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18ac2-149">Requirement</span></span> | <span data-ttu-id="18ac2-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="18ac2-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18ac2-151">Version</span><span class="sxs-lookup"><span data-stu-id="18ac2-151">Version</span></span><br/> | <span data-ttu-id="18ac2-152">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="18ac2-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="18ac2-153">DLL</span><span class="sxs-lookup"><span data-stu-id="18ac2-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="18ac2-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ac2-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ac2-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18ac2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ac2-156">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="18ac2-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





