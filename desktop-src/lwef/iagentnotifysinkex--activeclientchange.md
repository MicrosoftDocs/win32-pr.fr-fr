---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511431"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="9bb3e-103">IAgentNotifySinkEx::ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="9bb3e-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="9bb3e-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9bb3e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="9bb3e-105">Avertit une application cliente si son client actif n’est plus le client actif d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="9bb3e-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="9bb3e-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="9bb3e-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="9bb3e-108">Identificateur du caractère pour lequel l’état du client actif a été modifié.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="9bb3e-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span><span class="sxs-lookup"><span data-stu-id="9bb3e-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="9bb3e-110">Changement d’état actif du client, qui peut être une combinaison de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9bb3e-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="9bb3e-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="9bb3e-111">Value</span></span>                                                              | <span data-ttu-id="9bb3e-112">Description</span><span class="sxs-lookup"><span data-stu-id="9bb3e-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="9bb3e-113">**const non signed Short** **ACTIVATe \_ notactive = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="9bb3e-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="9bb3e-114">Votre client n’est pas le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="9bb3e-115">**const non signé Short** **Activate \_ active = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="9bb3e-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="9bb3e-116">Votre client est le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="9bb3e-117">**const non signed Short** **Activate \_ INPUTACTIVE = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="9bb3e-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="9bb3e-118">Votre client est en entrée-actif (client actif du premier caractère).</span><span class="sxs-lookup"><span data-stu-id="9bb3e-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="9bb3e-119">Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="9bb3e-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="9bb3e-120">De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="9bb3e-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="9bb3e-121">Lorsque le client actif d’un caractère change, cet événement transmet l’ID de ce caractère et la **valeur true** si votre application est devenue le client actif du caractère ou **false** si elle n’est plus le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="9bb3e-122">Une application cliente peut recevoir cet événement lorsque l’utilisateur sélectionne une autre entrée de l’application cliente dans le menu contextuel du caractère ou à l’aide de la commande vocale, que l’application cliente modifie son état actif ou qu’une autre application cliente quitte sa connexion à Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="9bb3e-123">Agent envoie cet événement uniquement aux applications clientes directement affectées, c’est-à-dire celles qui deviennent le client actif ou qui cessent d’être le client actif.</span><span class="sxs-lookup"><span data-stu-id="9bb3e-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="9bb3e-124">Vous pouvez utiliser la méthode [**Activate**](iagentcharacter--activate.md) pour définir si votre application est le client actif du caractère ou pour faire de votre application le client d’entrée-actif (qui rend également le caractère le plus haut).</span><span class="sxs-lookup"><span data-stu-id="9bb3e-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="9bb3e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9bb3e-125">See Also</span></span>

<span data-ttu-id="9bb3e-126">[**IAgentCharacter :: Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx :: GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink :: ActivateInputState**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="9bb3e-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 





