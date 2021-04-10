---
title: IAgentNotifySink déplacer
description: IAgentNotifySink déplacer
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940268"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="82ba3-103">IAgentNotifySink :: Move</span><span class="sxs-lookup"><span data-stu-id="82ba3-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="82ba3-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82ba3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="82ba3-105">Avertit une application cliente lorsque le caractère a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="82ba3-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="82ba3-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="82ba3-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="82ba3-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="82ba3-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-108">Identificateur du caractère qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="82ba3-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-109"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="82ba3-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-110">Coordonnée x de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="82ba3-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="82ba3-111">L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.</span><span class="sxs-lookup"><span data-stu-id="82ba3-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-112"><span id="y"></span><span id="Y"></span>*y*</span><span class="sxs-lookup"><span data-stu-id="82ba3-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-113">Coordonnée y de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche).</span><span class="sxs-lookup"><span data-stu-id="82ba3-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="82ba3-114">L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.</span><span class="sxs-lookup"><span data-stu-id="82ba3-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="82ba3-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-116">Cause du déplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="82ba3-116">The cause of the character move.</span></span> <span data-ttu-id="82ba3-117">Le paramètre peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="82ba3-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="82ba3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="82ba3-118">Value</span></span>                                                          | <span data-ttu-id="82ba3-119">Description</span><span class="sxs-lookup"><span data-stu-id="82ba3-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="82ba3-120">**const unsigned short** **NeverMoved = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="82ba3-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="82ba3-121">Le caractère n’a pas été déplacé.</span><span class="sxs-lookup"><span data-stu-id="82ba3-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="82ba3-122">**const unsigned short** **UserMoved = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="82ba3-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="82ba3-123">L’utilisateur a fait glisser le caractère.</span><span class="sxs-lookup"><span data-stu-id="82ba3-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="82ba3-124">**const unsigned short** **ProgramMoved = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="82ba3-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="82ba3-125">Votre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="82ba3-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="82ba3-126">**const unsigned short** **OtherProgramMoved = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="82ba3-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="82ba3-127">Une autre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="82ba3-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="82ba3-128">**const non signé Short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="82ba3-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="82ba3-129">Le serveur a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran.</span><span class="sxs-lookup"><span data-stu-id="82ba3-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="82ba3-130">Cet événement est envoyé à tous les clients du caractère.</span><span class="sxs-lookup"><span data-stu-id="82ba3-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="82ba3-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82ba3-131">See Also</span></span>

<span data-ttu-id="82ba3-132">[**IAgentCharacter :: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter :: MoveTo**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="82ba3-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 





