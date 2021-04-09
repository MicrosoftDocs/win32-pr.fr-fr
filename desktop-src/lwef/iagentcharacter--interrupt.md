---
title: Interruption IAgentCharacter
description: Interruption IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940854"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="3b943-103">IAgentCharacter :: Interrupt</span><span class="sxs-lookup"><span data-stu-id="3b943-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="3b943-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b943-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="3b943-105">Interrompt l’animation (demande) spécifiée d’un autre caractère.</span><span class="sxs-lookup"><span data-stu-id="3b943-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="3b943-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3b943-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="3b943-107">Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.</span><span class="sxs-lookup"><span data-stu-id="3b943-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="3b943-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="3b943-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="3b943-109">ID de la demande à interrompre.</span><span class="sxs-lookup"><span data-stu-id="3b943-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="3b943-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="3b943-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="3b943-111">Adresse d’une variable qui reçoit l’ID de demande d' **interruption** .</span><span class="sxs-lookup"><span data-stu-id="3b943-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="3b943-112">Si vous chargez plusieurs caractères, vous pouvez utiliser cette méthode pour synchroniser les animations entre les caractères.</span><span class="sxs-lookup"><span data-stu-id="3b943-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="3b943-113">Par exemple, si un autre caractère se trouve dans une animation de bouclage, cette méthode arrête l’animation de bouclage et démarre l’animation suivante dans la file d’attente du caractère.</span><span class="sxs-lookup"><span data-stu-id="3b943-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="3b943-114">L' **interruption** interrompt l’animation existante, mais n’efface pas la file d’attente d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="3b943-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="3b943-115">Il démarre l’animation suivante dans la file d’attente du caractère.</span><span class="sxs-lookup"><span data-stu-id="3b943-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="3b943-116">Pour arrêter et vider la file d’attente d’un caractère, utilisez la méthode [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .</span><span class="sxs-lookup"><span data-stu-id="3b943-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="3b943-117">Vous ne pouvez pas utiliser cette méthode pour avoir une interruption de caractère proprement dite car le serveur Microsoft agent met en file d’attente la méthode d' **interruption** dans la file d’attente d’animation du caractère.</span><span class="sxs-lookup"><span data-stu-id="3b943-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="3b943-118">Par conséquent, vous ne pouvez utiliser l' **interruption** que pour arrêter l’animation d’un autre caractère que vous avez chargé.</span><span class="sxs-lookup"><span data-stu-id="3b943-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 