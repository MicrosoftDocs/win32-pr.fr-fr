---
title: PLAYLIST. rightStatus
description: L’attribut rightStatus spécifie ou récupère le texte d’état affiché sur le côté droit et le bas de l’élément PLAYLIST.
ms.assetid: 82861572-ee8d-4780-a890-f018662499ff
keywords:
- Lecteur Windows Media PLAYLIST. rightStatus
topic_type:
- apiref
api_name:
- PLAYLIST.rightStatus
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47b382da4ae214c9a830cc64fb1aa0d0edadbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528071"
---
# <a name="playlistrightstatus"></a><span data-ttu-id="53228-104">PLAYLIST. rightStatus</span><span class="sxs-lookup"><span data-stu-id="53228-104">PLAYLIST.rightStatus</span></span>

<span data-ttu-id="53228-105">L’attribut **rightStatus** spécifie ou récupère le texte d’état affiché sur le côté droit et le bas de l’élément **playlist** .</span><span class="sxs-lookup"><span data-stu-id="53228-105">The **rightStatus** attribute specifies or retrieves the status text that is displayed on the right side and bottom of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.rightStatus
```

## <a name="possible-values"></a><span data-ttu-id="53228-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="53228-106">Possible Values</span></span>

<span data-ttu-id="53228-107">Cet attribut est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="53228-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="53228-108">Notes</span><span class="sxs-lookup"><span data-stu-id="53228-108">Remarks</span></span>

<span data-ttu-id="53228-109">Cet attribut peut combiner tout texte avec des mots clés spécifiques qui affichent les informations souhaitées, telles que la durée totale de la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-109">This attribute can combine any text with specific keywords that will display the desired information, such as the total duration of the playlist.</span></span> <span data-ttu-id="53228-110">Les mots clés sont entourés de symboles de pourcentage (%) pour les distinguer du texte ordinaire.</span><span class="sxs-lookup"><span data-stu-id="53228-110">The keywords are surrounded by percentage symbols (%) to keep them distinct from the ordinary text.</span></span>

<span data-ttu-id="53228-111">Les mots clés suivants peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="53228-111">The following keywords can be used.</span></span>



| <span data-ttu-id="53228-112">Mot clé</span><span class="sxs-lookup"><span data-stu-id="53228-112">Keyword</span></span>               | <span data-ttu-id="53228-113">Description</span><span class="sxs-lookup"><span data-stu-id="53228-113">Description</span></span>                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53228-114">count</span><span class="sxs-lookup"><span data-stu-id="53228-114">count</span></span>                 | <span data-ttu-id="53228-115">Nombre d’éléments dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-115">Number of items in the playlist.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="53228-116">est</span><span class="sxs-lookup"><span data-stu-id="53228-116">size</span></span>                  | <span data-ttu-id="53228-117">Taille totale de la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-117">Total size of the playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="53228-118">duration</span><span class="sxs-lookup"><span data-stu-id="53228-118">duration</span></span>              | <span data-ttu-id="53228-119">Durée totale de la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-119">Total duration of the playlist.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="53228-120">*INCONNU*</span><span class="sxs-lookup"><span data-stu-id="53228-120">*XXX*</span></span>                 | <span data-ttu-id="53228-121">Effectue un **getItemInfo** sur la playlist avec *xxx* qui est l’élément à recevoir.</span><span class="sxs-lookup"><span data-stu-id="53228-121">Does a **getItemInfo** on the playlist with *XXX* being the item to receive.</span></span>                                                                                                                                 |
| <span data-ttu-id="53228-122">SelectedSize</span><span class="sxs-lookup"><span data-stu-id="53228-122">SelectedSize</span></span>          | <span data-ttu-id="53228-123">Taille totale des entrées sélectionnées dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-123">Total size of the selected entries in the playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="53228-124">SelectedCount</span><span class="sxs-lookup"><span data-stu-id="53228-124">SelectedCount</span></span>         | <span data-ttu-id="53228-125">Nombre total d’entrées sélectionnées dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-125">Total number of selected entries in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="53228-126">SelectedDuration</span><span class="sxs-lookup"><span data-stu-id="53228-126">SelectedDuration</span></span>      | <span data-ttu-id="53228-127">Durée totale des entrées sélectionnées dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-127">Total duration of the selected entries in the playlist.</span></span>                                                                                                                                                      |
| <span data-ttu-id="53228-128">CheckedCount</span><span class="sxs-lookup"><span data-stu-id="53228-128">CheckedCount</span></span>          | <span data-ttu-id="53228-129">Nombre total de pistes activées dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-129">Total number of checked tracks in the playlist.</span></span>                                                                                                                                                              |
| <span data-ttu-id="53228-130">CheckedDuration</span><span class="sxs-lookup"><span data-stu-id="53228-130">CheckedDuration</span></span>       | <span data-ttu-id="53228-131">Durée totale des pistes cochées dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-131">Total duration of the checked tracks in the playlist.</span></span>                                                                                                                                                        |
| <span data-ttu-id="53228-132">CheckedSize</span><span class="sxs-lookup"><span data-stu-id="53228-132">CheckedSize</span></span>           | <span data-ttu-id="53228-133">Taille totale des pistes cochées dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="53228-133">Total size of the checked tracks in the playlist.</span></span>                                                                                                                                                            |
| <span data-ttu-id="53228-134">DurationString</span><span class="sxs-lookup"><span data-stu-id="53228-134">DurationString</span></span>        | <span data-ttu-id="53228-135">Affiche du texte qui décrit la durée sous la forme « temps total » ou « temps estimé », selon que les valeurs totales sont connues ou non.</span><span class="sxs-lookup"><span data-stu-id="53228-135">Displays text that describes the duration as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="53228-136">Ce texte est suivi de « % Duration% ».</span><span class="sxs-lookup"><span data-stu-id="53228-136">This text is followed by "%duration%".</span></span>                                       |
| <span data-ttu-id="53228-137">CheckedDurationString</span><span class="sxs-lookup"><span data-stu-id="53228-137">CheckedDurationString</span></span> | <span data-ttu-id="53228-138">Affiche le texte qui décrit la durée de tous les éléments activés dans la liste de lecture en tant que « durée totale » ou « durée estimée », selon que les valeurs totales sont connues ou non.</span><span class="sxs-lookup"><span data-stu-id="53228-138">Displays text that describes the duration for all checked items in the playlist as "Total Time" or "Estimated Time", depending on whether the total values are known.</span></span> <span data-ttu-id="53228-139">Ce texte est suivi de « % Duration% ».</span><span class="sxs-lookup"><span data-stu-id="53228-139">This text is followed by "%duration%".</span></span> |



 

<span data-ttu-id="53228-140">La valeur « temps total :% Duration% » pour une sélection qui contient une durée totale de sept minutes affiche « temps total : 07:00 ».</span><span class="sxs-lookup"><span data-stu-id="53228-140">The value "Total Time: %duration%" for a playlist that contains a total duration of seven minutes will display "Total Time: 07:00".</span></span>

## <a name="requirements"></a><span data-ttu-id="53228-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53228-141">Requirements</span></span>



| <span data-ttu-id="53228-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53228-142">Requirement</span></span> | <span data-ttu-id="53228-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="53228-143">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="53228-144">Version</span><span class="sxs-lookup"><span data-stu-id="53228-144">Version</span></span><br/> | <span data-ttu-id="53228-145">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="53228-145">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53228-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53228-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53228-147">**Élément PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="53228-147">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





