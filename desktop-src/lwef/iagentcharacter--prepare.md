---
title: Préparer IAgentCharacter
description: Préparer IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119874"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="c4a2d-103">IAgentCharacter ::P la même parenthèse</span><span class="sxs-lookup"><span data-stu-id="c4a2d-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="c4a2d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4a2d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="c4a2d-105">Récupère les données d’animation d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="c4a2d-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="c4a2d-107">Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="c4a2d-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="c4a2d-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="c4a2d-109">Valeur qui indique le type de données d’animation à charger qui doit être l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c4a2d-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="c4a2d-110">Value</span><span class="sxs-lookup"><span data-stu-id="c4a2d-110">Value</span></span>                                                           | <span data-ttu-id="c4a2d-111">Description</span><span class="sxs-lookup"><span data-stu-id="c4a2d-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="c4a2d-112">**const non signed Short** **Prepare \_ animation = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="c4a2d-113">Données d’animation d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="c4a2d-114">**const non signé Short** **Prepare \_ State = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="c4a2d-115">Données d’état d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="c4a2d-116">**const non signé Short** **Prepare \_ Wave = 2**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="c4a2d-117">Fichier son d’un caractère (. WAV ou. LWV) pour la sortie parlée.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c4a2d-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="c4a2d-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="c4a2d-119">Nom de l’animation ou de l’État.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-119">The name of the animation or state.</span></span>

<span data-ttu-id="c4a2d-120">Le nom de l’animation est basé sur celui défini pour le caractère lorsqu’il a été enregistré à l’aide de l’éditeur de caractères Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="c4a2d-121">Pour les États, la valeur peut être l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4a2d-121">For states, the value can be one of the following:</span></span>



|                      | <span data-ttu-id="c4a2d-122">Description</span><span class="sxs-lookup"><span data-stu-id="c4a2d-122">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="c4a2d-123">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-123">**"Gesturing"**</span></span>      | <span data-ttu-id="c4a2d-124">Pour récupérer toutes les animations d’état **gesturing** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-124">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="c4a2d-125">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-125">**"GesturingDown"**</span></span>  | <span data-ttu-id="c4a2d-126">Pour récupérer les animations **GesturingDown** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-126">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="c4a2d-127">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-127">**"GesturingLeft"**</span></span>  | <span data-ttu-id="c4a2d-128">Pour récupérer les animations **GesturingLeft** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-128">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="c4a2d-129">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-129">**"GesturingRight"**</span></span> | <span data-ttu-id="c4a2d-130">Pour récupérer les animations **GesturingRight** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-130">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="c4a2d-131">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-131">**"GesturingUp"**</span></span>    | <span data-ttu-id="c4a2d-132">Pour récupérer les animations **GesturingUp** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-132">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="c4a2d-133">**Masquage**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-133">**"Hiding"**</span></span>         | <span data-ttu-id="c4a2d-134">Pour récupérer les animations d’état de **masquage** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-134">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="c4a2d-135">**Entendre**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-135">**"Hearing"**</span></span>        | <span data-ttu-id="c4a2d-136">Pour récupérer les animations d’état **auditif** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-136">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="c4a2d-137">**Tournant**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-137">**"Idling"**</span></span>         | <span data-ttu-id="c4a2d-138">Pour récupérer toutes les animations d’état de **ralenti** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-138">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="c4a2d-139">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-139">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="c4a2d-140">Pour récupérer toutes les animations **IdlingLevel1** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-140">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="c4a2d-141">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-141">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="c4a2d-142">Pour récupérer toutes les animations **IdlingLevel2** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-142">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="c4a2d-143">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-143">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="c4a2d-144">Pour récupérer toutes les animations **IdlingLevel3** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-144">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="c4a2d-145">**Listen**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-145">**"Listening"**</span></span>      | <span data-ttu-id="c4a2d-146">Pour récupérer les animations d’état d' **écoute** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-146">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="c4a2d-147">**Passer**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-147">**"Moving"**</span></span>         | <span data-ttu-id="c4a2d-148">Pour récupérer toutes les animations d’état de **déplacement** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-148">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="c4a2d-149">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-149">**"MovingDown"**</span></span>     | <span data-ttu-id="c4a2d-150">Pour récupérer toutes les animations **mobiles** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-150">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="c4a2d-151">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-151">**"MovingLeft"**</span></span>     | <span data-ttu-id="c4a2d-152">Pour récupérer toutes les animations **MovingLeft** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-152">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="c4a2d-153">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-153">**"MovingRight"**</span></span>    | <span data-ttu-id="c4a2d-154">Pour récupérer toutes les animations **MovingRight** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-154">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="c4a2d-155">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-155">**"MovingUp"**</span></span>       | <span data-ttu-id="c4a2d-156">Pour récupérer toutes les animations **MovingUp** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-156">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="c4a2d-157">**Proposant**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-157">**"Showing"**</span></span>        | <span data-ttu-id="c4a2d-158">Pour récupérer les animations d’état d' **émission** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-158">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="c4a2d-159">**Parlez**</span><span class="sxs-lookup"><span data-stu-id="c4a2d-159">**"Speaking"**</span></span>       | <span data-ttu-id="c4a2d-160">Pour récupérer les animations d’état de **conversation** .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-160">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="c4a2d-161">Pour. Fichiers WAV, définissez *bszName* sur l’URL ou la spécification de fichier pour le. Fichier WAV.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-161">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="c4a2d-162">Si la spécification n’est pas terminée, elle est interprétée comme étant relative à la spécification utilisée dans la méthode [**Load**](https://www.bing.com/search?q=**Load**) .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-162">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="c4a2d-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="c4a2d-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="c4a2d-164">Valeur booléenne qui spécifie si le serveur met en file d’attente la demande de [**préparation**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-164">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="c4a2d-165">**True** met la demande en file d’attente et provoque le chargement des requêtes d’animation qui le suivent jusqu’à ce que les données d’animation qu’elle spécifient soient chargées.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-165">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="c4a2d-166">**False** récupère les données d’animation de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-166">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="c4a2d-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="c4a2d-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c4a2d-168">Adresse d’une variable qui reçoit l’ID de la demande de [**préparation**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-168">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="c4a2d-169">Si vous chargez un caractère à l’aide du protocole HTTP (. Fichier ACF), vous devez utiliser la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour récupérer des données d’animation avant de pouvoir lire l’animation.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-169">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="c4a2d-170">Vous ne pouvez pas utiliser cette méthode si vous avez chargé le caractère à l’aide du protocole UNC (un. Fichier ACS).</span><span class="sxs-lookup"><span data-stu-id="c4a2d-170">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="c4a2d-171">Vous ne pouvez pas non plus récupérer les données HTTP d’un caractère à l’aide de **Prepare** si vous avez chargé ce caractère à l’aide du protocole UNC (. Fichier de caractères ACS).</span><span class="sxs-lookup"><span data-stu-id="c4a2d-171">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="c4a2d-172">Les données audio ou d’animation récupérées avec la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) sont stockées dans le cache du navigateur.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-172">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="c4a2d-173">Les appels suivants vérifient le cache et, si les données d’animation y sont déjà, le contrôle charge les données directement à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-173">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="c4a2d-174">Une fois chargées, les données de l’animation ou du son peuvent être lues avec les méthodes [**Play**](/windows/desktop/lwef/iagentcharacter--play) ou [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-174">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="c4a2d-175">Vous pouvez spécifier plusieurs animations et États en les séparant par des virgules.</span><span class="sxs-lookup"><span data-stu-id="c4a2d-175">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="c4a2d-176">Toutefois, vous ne pouvez pas mélanger des types dans la même instruction [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="c4a2d-176">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

