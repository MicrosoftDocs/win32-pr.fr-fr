---
title: IAgentCharacter activer
description: IAgentCharacter activer
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507471"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="9a018-103">IAgentCharacter :: Activate</span><span class="sxs-lookup"><span data-stu-id="9a018-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="9a018-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a018-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="9a018-105">Définit si un client est actif ou si un caractère est le plus haut.</span><span class="sxs-lookup"><span data-stu-id="9a018-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="9a018-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="9a018-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="9a018-107">Retourne S \_ false pour indiquer que l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="9a018-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="9a018-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span><span class="sxs-lookup"><span data-stu-id="9a018-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="9a018-109">Vous pouvez spécifier les valeurs suivantes pour ce paramètre :</span><span class="sxs-lookup"><span data-stu-id="9a018-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="9a018-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a018-110">Value</span></span> | <span data-ttu-id="9a018-111">Description</span><span class="sxs-lookup"><span data-stu-id="9a018-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="9a018-112">0</span><span class="sxs-lookup"><span data-stu-id="9a018-112">0</span></span>     | <span data-ttu-id="9a018-113">Défini comme n’étant pas le client actif.</span><span class="sxs-lookup"><span data-stu-id="9a018-113">Set as not the active client.</span></span> |
| <span data-ttu-id="9a018-114">1</span><span class="sxs-lookup"><span data-stu-id="9a018-114">1</span></span>     | <span data-ttu-id="9a018-115">Défini en tant que client actif.</span><span class="sxs-lookup"><span data-stu-id="9a018-115">Set as the active client.</span></span>     |
| <span data-ttu-id="9a018-116">2</span><span class="sxs-lookup"><span data-stu-id="9a018-116">2</span></span>     | <span data-ttu-id="9a018-117">Créez le premier caractère.</span><span class="sxs-lookup"><span data-stu-id="9a018-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="9a018-118">Lorsque plusieurs caractères sont visibles, un seul des caractères reçoit les entrées vocales à la fois.</span><span class="sxs-lookup"><span data-stu-id="9a018-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="9a018-119">De même, lorsque plusieurs applications clientes partagent le même caractère, un seul des clients reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent) à la fois.</span><span class="sxs-lookup"><span data-stu-id="9a018-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="9a018-120">Le jeu de caractères pour recevoir l’entrée de la souris et de la parole est le caractère le plus élevé et le client qui reçoit l’entrée est le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9a018-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="9a018-121">(La fenêtre du caractère supérieur s’affiche également en haut de l’ordre de plan de la fenêtre de caractères.) En règle générale, l’utilisateur détermine le caractère le plus élevé en le sélectionnant explicitement.</span><span class="sxs-lookup"><span data-stu-id="9a018-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="9a018-122">Toutefois, l’activation de niveau supérieur change également lorsqu’un caractère est affiché ou masqué (le caractère devient ou n’est plus le premier niveau, respectivement).</span><span class="sxs-lookup"><span data-stu-id="9a018-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="9a018-123">Vous pouvez également utiliser cette méthode pour gérer explicitement quand votre client reçoit une entrée dirigée vers le caractère, par exemple quand votre application est elle-même active.</span><span class="sxs-lookup"><span data-stu-id="9a018-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="9a018-124">Par exemple, la définition de l' **État** sur 2 rend le caractère le plus haut, et votre client reçoit tous les événements d’entrée de la souris et de la parole générés par l’interaction de l’utilisateur avec le caractère.</span><span class="sxs-lookup"><span data-stu-id="9a018-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="9a018-125">Par conséquent, il rend également votre client le client d’entrée-actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9a018-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="9a018-126">Toutefois, vous pouvez également définir le client actif pour un caractère sans rendre le caractère le plus haut, en définissant l' **État** sur 1.</span><span class="sxs-lookup"><span data-stu-id="9a018-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="9a018-127">Cela permet à votre client de recevoir l’entrée dirigée vers ce caractère lorsque le caractère devient le plus haut.</span><span class="sxs-lookup"><span data-stu-id="9a018-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="9a018-128">De même, vous pouvez configurer votre client pour qu’il ne soit pas le client actif (pour ne pas recevoir d’entrée) lorsque le caractère est le plus haut, en définissant l' **État** sur 0.</span><span class="sxs-lookup"><span data-stu-id="9a018-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="9a018-129">Vous pouvez déterminer si un caractère a d’autres clients actuels à l’aide de [**IAgentCharacter :: HasOtherClients**](iagentcharacter--hasotherclients.md).</span><span class="sxs-lookup"><span data-stu-id="9a018-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="9a018-130">Évitez d’appeler cette méthode directement après une méthode [**Show**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="9a018-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="9a018-131">**Afficher** définit automatiquement le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="9a018-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="9a018-132">Lorsque le caractère est masqué, l’appel d' **activation** peut échouer s’il est traité avant la fin de la méthode **Show** .</span><span class="sxs-lookup"><span data-stu-id="9a018-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="9a018-133">Toute tentative d’appel à cette méthode avec le paramètre d' **État** défini sur 2 (lorsque le caractère spécifié est masqué) échoue.</span><span class="sxs-lookup"><span data-stu-id="9a018-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="9a018-134">De même, si vous affectez à l' **État** la valeur 0 et que votre application est le seul client, cet appel échoue.</span><span class="sxs-lookup"><span data-stu-id="9a018-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="9a018-135">Un caractère doit toujours avoir un client de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="9a018-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="9a018-136">L’appel de cette méthode avec un **État** défini sur 1 ne génère généralement pas d’événement [**AgentNotifySink :: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) , sauf si aucun autre caractère n’est chargé ou si votre application est déjà en entrée-active.</span><span class="sxs-lookup"><span data-stu-id="9a018-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="9a018-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a018-137">See Also</span></span>

[<span data-ttu-id="9a018-138">**IAgentCharacter::HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="9a018-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 




