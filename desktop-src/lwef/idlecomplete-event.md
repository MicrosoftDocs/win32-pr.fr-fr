---
title: Événement IdleComplete
description: Événement IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028471"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="18d84-103">Événement IdleComplete</span><span class="sxs-lookup"><span data-stu-id="18d84-103">IdleComplete Event</span></span>

<span data-ttu-id="18d84-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="18d84-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="18d84-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="18d84-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="18d84-106">Se produit lorsque le serveur met fin à l’état de **ralenti** d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="18d84-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="18d84-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="18d84-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="18d84-108">**Sous** - *agent \* \* \* \_ IdleComplete* \*  **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="18d84-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="18d84-109">Partie</span><span class="sxs-lookup"><span data-stu-id="18d84-109">Part</span></span>          | <span data-ttu-id="18d84-110">Description</span><span class="sxs-lookup"><span data-stu-id="18d84-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="18d84-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="18d84-111">*CharacterID*</span></span> | <span data-ttu-id="18d84-112">Retourne l’ID du caractère ralenti sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="18d84-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="18d84-113">Notes</span><span class="sxs-lookup"><span data-stu-id="18d84-113">Remarks</span></span>

<span data-ttu-id="18d84-114">Le serveur envoie cet événement à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="18d84-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="18d84-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18d84-115">See Also</span></span>

[<span data-ttu-id="18d84-116">**Événement IdleStart**</span><span class="sxs-lookup"><span data-stu-id="18d84-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




