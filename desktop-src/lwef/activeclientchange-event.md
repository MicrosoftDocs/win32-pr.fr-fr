---
title: Événement ActiveClientChange
description: Événement ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196769"
---
# <a name="activeclientchange-event"></a><span data-ttu-id="9f245-103">Événement ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="9f245-103">ActiveClientChange Event</span></span>

<span data-ttu-id="9f245-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9f245-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9f245-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="9f245-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9f245-106">Se produit lorsque le client actif du caractère change.</span><span class="sxs-lookup"><span data-stu-id="9f245-106">Occurs when the active client of the character changes.</span></span>

</dd> <dt>

<span data-ttu-id="9f245-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="9f245-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9f245-108">**Sous** - *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *actif* **)**</span><span class="sxs-lookup"><span data-stu-id="9f245-108">**Sub** *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *Active* **)**</span></span>



| <span data-ttu-id="9f245-109">Partie</span><span class="sxs-lookup"><span data-stu-id="9f245-109">Part</span></span>          | <span data-ttu-id="9f245-110">Description</span><span class="sxs-lookup"><span data-stu-id="9f245-110">Description</span></span>                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f245-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="9f245-111">*CharacterID*</span></span> | <span data-ttu-id="9f245-112">Retourne l’ID du caractère pour lequel l’événement s’est produit.</span><span class="sxs-lookup"><span data-stu-id="9f245-112">Returns the ID of the character for which the event occurred.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="9f245-113">*Actif*</span><span class="sxs-lookup"><span data-stu-id="9f245-113">*Active*</span></span>      | <span data-ttu-id="9f245-114">Valeur booléenne qui indique si le client est devenu actif ou non actif.</span><span class="sxs-lookup"><span data-stu-id="9f245-114">A Boolean value that indicates whether the client became active or not active.</span></span> <span data-ttu-id="9f245-115">**True** L’application cliente est devenue le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9f245-115">**True** The client application became the active client of the character.</span></span> <br/> <span data-ttu-id="9f245-116">**Valeur false** L’application cliente n’est plus le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9f245-116">**False** The client application is no longer the active client of the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9f245-117">Notes</span><span class="sxs-lookup"><span data-stu-id="9f245-117">Remarks</span></span>

<span data-ttu-id="9f245-118">Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="9f245-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="9f245-119">De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements de [commande](command-event.md) .</span><span class="sxs-lookup"><span data-stu-id="9f245-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [Command](command-event.md) events.</span></span>

<span data-ttu-id="9f245-120">Lorsque le client actif d’un caractère change, cet événement transmet l’ID de ce caractère et la **valeur true** si votre application est devenue le client actif du caractère ou **false** si elle n’est plus le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="9f245-120">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="9f245-121">Une application cliente peut recevoir cet événement lorsque l’utilisateur sélectionne l’entrée d’une application cliente dans le menu contextuel d’un caractère ou par une commande vocale, lorsque l’application cliente modifie son état actif ou lorsqu’une autre application cliente quitte sa connexion à l’agent.</span><span class="sxs-lookup"><span data-stu-id="9f245-121">A client application may receive this event when the user selects a client application's entry in character's pop-up menu or by voice command, when the client application changes its active status, or when another client application quits its connection to Agent.</span></span> <span data-ttu-id="9f245-122">Agent envoie cet événement uniquement aux applications clientes qui sont directement affectées ; qu’il s’agisse du client actif ou d’un arrêt du client actif.</span><span class="sxs-lookup"><span data-stu-id="9f245-122">Agent sends this event only to the client applications that are directly affected; that either become the active client or stop being the active client.</span></span>

### <a name="see-also"></a><span data-ttu-id="9f245-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f245-123">See Also</span></span>

<span data-ttu-id="9f245-124">\* \* \* \* [ActivateInput \* \* Event \* \*](activateinput-event.md)\* [\* \*](active-property.md)\* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* [\* \* \*](deactivateinput-event.md)\* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* \* [\* \*](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="9f245-124">[\*\*\*\*ActivateInput\*\* event\*\*](activateinput-event.md), [\*\*\*\*Active\*\* property\*\*](active-property.md), [\*\*\*\*DeactivateInput\*\* event\*\*](deactivateinput-event.md), [\*\*\*\*Activate\*\* method\*\*](activate-method.md)</span></span>


 

 





