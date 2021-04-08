---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840541"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="986a4-103">IAgentCharacterEx::GetActive</span><span class="sxs-lookup"><span data-stu-id="986a4-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="986a4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="986a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="986a4-105">Récupère les valeur indiquant si votre application cliente est le client actif du caractère et si le caractère est le plus haut.</span><span class="sxs-lookup"><span data-stu-id="986a4-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="986a4-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="986a4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="986a4-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span><span class="sxs-lookup"><span data-stu-id="986a4-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="986a4-108">Adresse d’une variable qui reçoit l’une des valeurs suivantes pour le paramètre d’État :</span><span class="sxs-lookup"><span data-stu-id="986a4-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="986a4-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="986a4-109">Value</span></span>                                                              | <span data-ttu-id="986a4-110">Description</span><span class="sxs-lookup"><span data-stu-id="986a4-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="986a4-111">**const non signed Short** **ACTIVATe \_ notactive = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="986a4-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="986a4-112">Votre client n’est pas le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="986a4-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="986a4-113">**const non signé Short** **Activate \_ active = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="986a4-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="986a4-114">Votre client est le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="986a4-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="986a4-115">**const non signed Short** **Activate \_ INPUTACTIVE = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="986a4-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="986a4-116">Votre client est en entrée-actif (client actif du premier caractère).</span><span class="sxs-lookup"><span data-stu-id="986a4-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="986a4-117">Ce paramètre vous permet de savoir si vous êtes le client actif du caractère ou si votre caractère est le caractère actif d’entrée.</span><span class="sxs-lookup"><span data-stu-id="986a4-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="986a4-118">Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="986a4-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="986a4-119">De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="986a4-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="986a4-120">Utilisez la méthode [**Activate**](iagentcharacter--activate.md) pour définir si votre application est le client actif du personnage ou pour faire de votre application le client actif d’entrée (ce qui rend également le premier caractère).</span><span class="sxs-lookup"><span data-stu-id="986a4-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="986a4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="986a4-121">See Also</span></span>

<span data-ttu-id="986a4-122">[**IAgentCharacter :: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx :: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="986a4-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 





