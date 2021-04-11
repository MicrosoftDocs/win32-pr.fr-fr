---
title: IAgentCharacter masquer
description: IAgentCharacter masquer
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031163"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="2c832-103">IAgentCharacter :: Hide</span><span class="sxs-lookup"><span data-stu-id="2c832-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="2c832-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2c832-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="2c832-105">Masque le caractère.</span><span class="sxs-lookup"><span data-stu-id="2c832-105">Hides the character.</span></span>

-   <span data-ttu-id="2c832-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2c832-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="2c832-107">Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.</span><span class="sxs-lookup"><span data-stu-id="2c832-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="2c832-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="2c832-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="2c832-109">**Masquage** de l’indicateur d’animation d’État.</span><span class="sxs-lookup"><span data-stu-id="2c832-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="2c832-110">Si ce paramètre a la **valeur true**, l’animation de **masquage** ne s’exécute pas avant que le cadre de caractère soit masqué ; Si la **valeur est false**, l’animation est lue.</span><span class="sxs-lookup"><span data-stu-id="2c832-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="2c832-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="2c832-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="2c832-112">Adresse d’une variable qui reçoit l’ID de la demande de **masquage** .</span><span class="sxs-lookup"><span data-stu-id="2c832-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="2c832-113">Le serveur met en file d’attente l’animation associée à la méthode **Hide** dans la file d’attente du caractère.</span><span class="sxs-lookup"><span data-stu-id="2c832-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="2c832-114">Cela vous permet de l’utiliser pour masquer le caractère après une séquence d’autres animations.</span><span class="sxs-lookup"><span data-stu-id="2c832-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="2c832-115">Vous pouvez exécuter l’action immédiatement à l’aide de la méthode [**Stop**](iagentcharacter--stop.md) avant d’appeler la méthode **Hide** .</span><span class="sxs-lookup"><span data-stu-id="2c832-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="2c832-116">Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité de l’animation de l’état de **masquage** avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2c832-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="2c832-117">Le masquage d’un caractère peut également entraîner le déclenchement de l’événement [**IAgentNotifySink :: ActivateInputState**](iagentnotifysink--activateinputstate.md) d’un autre caractère visible.</span><span class="sxs-lookup"><span data-stu-id="2c832-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="2c832-118">Les caractères masqués ne peuvent pas accéder au canal audio.</span><span class="sxs-lookup"><span data-stu-id="2c832-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="2c832-119">Le serveur renvoie un état d’échec dans l’événement [**RequestComplete**](iagentnotifysink--requestcomplete.md) si vous générez une demande d’animation et que le caractère est masqué.</span><span class="sxs-lookup"><span data-stu-id="2c832-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c832-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c832-120">See Also</span></span>

[<span data-ttu-id="2c832-121">**IAgentCharacter :: Show**</span><span class="sxs-lookup"><span data-stu-id="2c832-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 