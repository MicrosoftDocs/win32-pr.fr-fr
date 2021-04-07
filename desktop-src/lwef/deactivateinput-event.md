---
title: Événement DeactivateInput
description: Événement DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940086"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="bcf5c-103">Événement DeactivateInput</span><span class="sxs-lookup"><span data-stu-id="bcf5c-103">DeactivateInput Event</span></span>

<span data-ttu-id="bcf5c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bcf5c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bcf5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="bcf5c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bcf5c-106">Se produit lorsqu’un client devient non-actif.</span><span class="sxs-lookup"><span data-stu-id="bcf5c-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="bcf5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="bcf5c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bcf5c-108">**Sous** - *agent \* \* \* \_ DeactivateInput* \*  **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="bcf5c-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="bcf5c-109">Partie</span><span class="sxs-lookup"><span data-stu-id="bcf5c-109">Part</span></span>          | <span data-ttu-id="bcf5c-110">Description</span><span class="sxs-lookup"><span data-stu-id="bcf5c-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="bcf5c-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="bcf5c-111">*CharacterID*</span></span> | <span data-ttu-id="bcf5c-112">Retourne l’ID du caractère qui rend le client devenu non actif.</span><span class="sxs-lookup"><span data-stu-id="bcf5c-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="bcf5c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bcf5c-113">Remarks</span></span>

<span data-ttu-id="bcf5c-114">Un client de non-entrée-actif ne reçoit plus d’événements de souris ou de parole du serveur (à moins qu’il ne soit de nouveau en entrée active).</span><span class="sxs-lookup"><span data-stu-id="bcf5c-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="bcf5c-115">Le serveur envoie cet événement uniquement au client qui devient non-actif.</span><span class="sxs-lookup"><span data-stu-id="bcf5c-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="bcf5c-116">Cet événement se produit lorsque votre application cliente est en entrée-active et que l’utilisateur choisit la légende d’un autre client dans le menu contextuel d’un caractère ou dans la fenêtre commandes vocales ou si vous appelez la méthode [**Activate**](activate-method.md) et définissez le paramètre **State** sur 0.</span><span class="sxs-lookup"><span data-stu-id="bcf5c-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="bcf5c-117">Cela peut également se produire lorsque l’utilisateur sélectionne le nom d’un autre caractère en cliquant ou en parlant.</span><span class="sxs-lookup"><span data-stu-id="bcf5c-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="bcf5c-118">Vous recevez également cet événement lorsque votre caractère est masqué ou qu’un autre caractère devient visible.</span><span class="sxs-lookup"><span data-stu-id="bcf5c-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="bcf5c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf5c-119">See Also</span></span>

[<span data-ttu-id="bcf5c-120">**Événement ActivateInput**</span><span class="sxs-lookup"><span data-stu-id="bcf5c-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




