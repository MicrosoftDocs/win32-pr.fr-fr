---
title: Afficher l’événement
description: Afficher l’événement
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839654"
---
# <a name="show-event"></a><span data-ttu-id="5db4e-103">Afficher l’événement</span><span class="sxs-lookup"><span data-stu-id="5db4e-103">Show Event</span></span>

<span data-ttu-id="5db4e-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5db4e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5db4e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="5db4e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5db4e-106">Se produit lorsqu’un caractère est affiché.</span><span class="sxs-lookup"><span data-stu-id="5db4e-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="5db4e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="5db4e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5db4e-108">**Sub** *agent \* \* \* \_ Show (ByVal* \*  *CharacterID*, **ByVal** *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="5db4e-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="5db4e-109">Partie</span><span class="sxs-lookup"><span data-stu-id="5db4e-109">Part</span></span>          | <span data-ttu-id="5db4e-110">Description</span><span class="sxs-lookup"><span data-stu-id="5db4e-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db4e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5db4e-111">*CharacterID*</span></span> | <span data-ttu-id="5db4e-112">Retourne l’ID du caractère affiché en tant que chaîne.</span><span class="sxs-lookup"><span data-stu-id="5db4e-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="5db4e-113">*Cause*</span><span class="sxs-lookup"><span data-stu-id="5db4e-113">*Cause*</span></span>       | <span data-ttu-id="5db4e-114">Retourne une valeur qui indique ce qui a provoqué l’affichage du caractère.</span><span class="sxs-lookup"><span data-stu-id="5db4e-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="5db4e-115">2 l’utilisateur a affiché le caractère (à l’aide du menu ou de la commande vocale).</span><span class="sxs-lookup"><span data-stu-id="5db4e-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="5db4e-116">4 votre application cliente affichait le caractère.</span><span class="sxs-lookup"><span data-stu-id="5db4e-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="5db4e-117">6 une autre application cliente affichait le caractère.</span><span class="sxs-lookup"><span data-stu-id="5db4e-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5db4e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5db4e-118">Remarks</span></span>

<span data-ttu-id="5db4e-119">Le serveur envoie cet événement à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="5db4e-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="5db4e-120">Pour interroger l’état actuel du caractère, utilisez la propriété [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="5db4e-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="5db4e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db4e-121">See Also</span></span>

<span data-ttu-id="5db4e-122">[**Masquer l’événement**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="5db4e-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





