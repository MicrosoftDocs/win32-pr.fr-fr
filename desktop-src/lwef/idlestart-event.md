---
title: Événement IdleStart
description: Événement IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513667"
---
# <a name="idlestart-event"></a><span data-ttu-id="1cb8c-103">Événement IdleStart</span><span class="sxs-lookup"><span data-stu-id="1cb8c-103">IdleStart Event</span></span>

<span data-ttu-id="1cb8c-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1cb8c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1cb8c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="1cb8c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1cb8c-106">Se produit lorsque le serveur définit un caractère à l’état **ralenti** .</span><span class="sxs-lookup"><span data-stu-id="1cb8c-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="1cb8c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="1cb8c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1cb8c-108">**Sous** - *agent \* \* \* \_ IdleStart* \*  **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="1cb8c-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="1cb8c-109">Partie</span><span class="sxs-lookup"><span data-stu-id="1cb8c-109">Part</span></span>          | <span data-ttu-id="1cb8c-110">Description</span><span class="sxs-lookup"><span data-stu-id="1cb8c-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="1cb8c-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="1cb8c-111">*CharacterID*</span></span> | <span data-ttu-id="1cb8c-112">Retourne l’ID du caractère ralenti sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="1cb8c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="1cb8c-113">Remarks</span></span>

<span data-ttu-id="1cb8c-114">Le serveur envoie cet événement à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="1cb8c-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="1cb8c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cb8c-115">See Also</span></span>

[<span data-ttu-id="1cb8c-116">**Événement IdleComplete**</span><span class="sxs-lookup"><span data-stu-id="1cb8c-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




