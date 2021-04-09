---
title: Masquer l’événement
description: Masquer l’événement
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840113"
---
# <a name="hide-event"></a><span data-ttu-id="609c3-103">Masquer l’événement</span><span class="sxs-lookup"><span data-stu-id="609c3-103">Hide Event</span></span>

<span data-ttu-id="609c3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="609c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="609c3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="609c3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="609c3-106">Se produit lorsqu’un caractère est masqué.</span><span class="sxs-lookup"><span data-stu-id="609c3-106">Occurs when a character is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="609c3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="609c3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="609c3-108">**Sub** *agent \* \* \* \_ Hide (* \*  **ByVal** *CharacterID*, **ByVal** *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="609c3-108">**Sub** *agent\*\*\*\_Hide(*\* **ByVal** *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="609c3-109">Partie</span><span class="sxs-lookup"><span data-stu-id="609c3-109">Part</span></span>          | <span data-ttu-id="609c3-110">Description</span><span class="sxs-lookup"><span data-stu-id="609c3-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="609c3-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="609c3-111">*CharacterID*</span></span> | <span data-ttu-id="609c3-112">Retourne l’ID du caractère masqué sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="609c3-112">Returns the ID of the hidden character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="609c3-113">*Cause*</span><span class="sxs-lookup"><span data-stu-id="609c3-113">*Cause*</span></span>       | <span data-ttu-id="609c3-114">Retourne une valeur qui indique ce qui a provoqué le masquage du caractère.</span><span class="sxs-lookup"><span data-stu-id="609c3-114">Returns a value that indicates what caused the character to hide.</span></span> <span data-ttu-id="609c3-115">1 utilisateur a masqué le caractère en sélectionnant la commande dans le menu contextuel de l’icône de barre des tâches du caractère ou en utilisant l’entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="609c3-115">1 User hid the character by selecting the command on the character's taskbar icon pop-up menu or using speech input.</span></span><br/> <span data-ttu-id="609c3-116">3 votre application cliente a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="609c3-116">3 Your client application hid the character.</span></span><br/> <span data-ttu-id="609c3-117">5 une autre application cliente a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="609c3-117">5 Another client application hid the character.</span></span><br/> <span data-ttu-id="609c3-118">7 l’utilisateur a masqué le caractère en sélectionnant la commande dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="609c3-118">7 User hid the character by selecting the command on the character's pop-up menu.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="609c3-119">Notes</span><span class="sxs-lookup"><span data-stu-id="609c3-119">Remarks</span></span>

<span data-ttu-id="609c3-120">Le serveur envoie cet événement à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="609c3-120">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="609c3-121">Pour interroger l’état actuel du caractère, utilisez la propriété [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="609c3-121">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="609c3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="609c3-122">See Also</span></span>

<span data-ttu-id="609c3-123">[**Afficher l’événement**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="609c3-123">[**Show event**](show-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





