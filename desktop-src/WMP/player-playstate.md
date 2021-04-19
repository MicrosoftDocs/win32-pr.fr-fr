---
title: Player. lecture
description: La propriété lecture récupère une valeur indiquant l’état de l’opération du lecteur Windows Media.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Lecteur Windows Media Player. lecture
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542347"
---
# <a name="playerplaystate"></a><span data-ttu-id="3b1f8-104">Player. lecture</span><span class="sxs-lookup"><span data-stu-id="3b1f8-104">Player.playState</span></span>

<span data-ttu-id="3b1f8-105">La propriété **lecture** récupère une valeur indiquant l’état de l’opération du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1f8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b1f8-106">Syntax</span></span>

<span data-ttu-id="3b1f8-107">*lecteur* . **lecture**</span><span class="sxs-lookup"><span data-stu-id="3b1f8-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3b1f8-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3b1f8-108">Possible Values</span></span>

<span data-ttu-id="3b1f8-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="3b1f8-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="3b1f8-110">La constante d’énumération de style C peut être dérivée en préfixant la valeur d’État avec « wmpps ».</span><span class="sxs-lookup"><span data-stu-id="3b1f8-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="3b1f8-111">Par exemple, la constante pour l’état de jeu est **wmppsPlaying**.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="3b1f8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b1f8-112">Value</span></span> | <span data-ttu-id="3b1f8-113">State</span><span class="sxs-lookup"><span data-stu-id="3b1f8-113">State</span></span>         | <span data-ttu-id="3b1f8-114">Description</span><span class="sxs-lookup"><span data-stu-id="3b1f8-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1f8-115">0</span><span class="sxs-lookup"><span data-stu-id="3b1f8-115">0</span></span>     | <span data-ttu-id="3b1f8-116">Indéfini</span><span class="sxs-lookup"><span data-stu-id="3b1f8-116">Undefined</span></span>     | <span data-ttu-id="3b1f8-117">Le lecteur Windows Media est dans un État non défini.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="3b1f8-118">1</span><span class="sxs-lookup"><span data-stu-id="3b1f8-118">1</span></span>     | <span data-ttu-id="3b1f8-119">Arrêté</span><span class="sxs-lookup"><span data-stu-id="3b1f8-119">Stopped</span></span>       | <span data-ttu-id="3b1f8-120">La lecture de l’élément multimédia en cours est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="3b1f8-121">2</span><span class="sxs-lookup"><span data-stu-id="3b1f8-121">2</span></span>     | <span data-ttu-id="3b1f8-122">Suspendu</span><span class="sxs-lookup"><span data-stu-id="3b1f8-122">Paused</span></span>        | <span data-ttu-id="3b1f8-123">La lecture de l’élément multimédia actuel est suspendue.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="3b1f8-124">Lorsqu’un élément multimédia est suspendu, la reprise de la lecture commence à partir du même emplacement.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="3b1f8-125">3</span><span class="sxs-lookup"><span data-stu-id="3b1f8-125">3</span></span>     | <span data-ttu-id="3b1f8-126">Lecture en cours</span><span class="sxs-lookup"><span data-stu-id="3b1f8-126">Playing</span></span>       | <span data-ttu-id="3b1f8-127">L’élément multimédia actuel est en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="3b1f8-128">4</span><span class="sxs-lookup"><span data-stu-id="3b1f8-128">4</span></span>     | <span data-ttu-id="3b1f8-129">ScanForward</span><span class="sxs-lookup"><span data-stu-id="3b1f8-129">ScanForward</span></span>   | <span data-ttu-id="3b1f8-130">L’élément multimédia actuel est un transfert rapide.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="3b1f8-131">5</span><span class="sxs-lookup"><span data-stu-id="3b1f8-131">5</span></span>     | <span data-ttu-id="3b1f8-132">ScanReverse</span><span class="sxs-lookup"><span data-stu-id="3b1f8-132">ScanReverse</span></span>   | <span data-ttu-id="3b1f8-133">L’élément multimédia actuel est un rembobinage rapide.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="3b1f8-134">6</span><span class="sxs-lookup"><span data-stu-id="3b1f8-134">6</span></span>     | <span data-ttu-id="3b1f8-135">des réponses</span><span class="sxs-lookup"><span data-stu-id="3b1f8-135">Buffering</span></span>     | <span data-ttu-id="3b1f8-136">L’élément multimédia actuel reçoit des données supplémentaires à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="3b1f8-137">7</span><span class="sxs-lookup"><span data-stu-id="3b1f8-137">7</span></span>     | <span data-ttu-id="3b1f8-138">En attente</span><span class="sxs-lookup"><span data-stu-id="3b1f8-138">Waiting</span></span>       | <span data-ttu-id="3b1f8-139">La connexion est établie, mais le serveur n’envoie pas de données.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="3b1f8-140">En attente du début de la session.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="3b1f8-141">8</span><span class="sxs-lookup"><span data-stu-id="3b1f8-141">8</span></span>     | <span data-ttu-id="3b1f8-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="3b1f8-142">MediaEnded</span></span>    | <span data-ttu-id="3b1f8-143">La lecture de l’élément multimédia est terminée.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="3b1f8-144">9</span><span class="sxs-lookup"><span data-stu-id="3b1f8-144">9</span></span>     | <span data-ttu-id="3b1f8-145">Transition</span><span class="sxs-lookup"><span data-stu-id="3b1f8-145">Transitioning</span></span> | <span data-ttu-id="3b1f8-146">Préparation du nouvel élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="3b1f8-147">10</span><span class="sxs-lookup"><span data-stu-id="3b1f8-147">10</span></span>    | <span data-ttu-id="3b1f8-148">Ready</span><span class="sxs-lookup"><span data-stu-id="3b1f8-148">Ready</span></span>         | <span data-ttu-id="3b1f8-149">Prêt à commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="3b1f8-150">11</span><span class="sxs-lookup"><span data-stu-id="3b1f8-150">11</span></span>    | <span data-ttu-id="3b1f8-151">La reconnexion</span><span class="sxs-lookup"><span data-stu-id="3b1f8-151">Reconnecting</span></span>  | <span data-ttu-id="3b1f8-152">Reconnexion au flux.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="3b1f8-153">Notes</span><span class="sxs-lookup"><span data-stu-id="3b1f8-153">Remarks</span></span>

<span data-ttu-id="3b1f8-154">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="3b1f8-155">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="3b1f8-156">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="3b1f8-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="3b1f8-157">Examples</span></span>

<span data-ttu-id="3b1f8-158">Le code JScript suivant illustre l’utilisation du *lecteur*. propriété **lecture** .</span><span class="sxs-lookup"><span data-stu-id="3b1f8-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="3b1f8-159">Un élément de texte HTML, nommé « myText », affiche l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="3b1f8-160">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3b1f8-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="3b1f8-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b1f8-161">Requirements</span></span>



| <span data-ttu-id="3b1f8-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b1f8-162">Requirement</span></span> | <span data-ttu-id="3b1f8-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b1f8-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1f8-164">Version</span><span class="sxs-lookup"><span data-stu-id="3b1f8-164">Version</span></span><br/> | <span data-ttu-id="3b1f8-165">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3b1f8-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3b1f8-166">DLL</span><span class="sxs-lookup"><span data-stu-id="3b1f8-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b1f8-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b1f8-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b1f8-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b1f8-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1f8-169">**Objet Player**</span><span class="sxs-lookup"><span data-stu-id="3b1f8-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="3b1f8-170">**Événement Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="3b1f8-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





