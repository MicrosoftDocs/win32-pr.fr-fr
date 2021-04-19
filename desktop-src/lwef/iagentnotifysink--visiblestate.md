---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508996"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="6dced-103">IAgentNotifySink::VisibleState</span><span class="sxs-lookup"><span data-stu-id="6dced-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="6dced-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6dced-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="6dced-105">Avertit une application cliente lorsque l’état de visibilité du caractère change.</span><span class="sxs-lookup"><span data-stu-id="6dced-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="6dced-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="6dced-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="6dced-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="6dced-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="6dced-108">Identificateur du caractère dont l’état de visibilité est modifié.</span><span class="sxs-lookup"><span data-stu-id="6dced-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="6dced-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="6dced-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="6dced-110">Indicateur de visibilité.</span><span class="sxs-lookup"><span data-stu-id="6dced-110">Visibility flag.</span></span> <span data-ttu-id="6dced-111">Cette valeur booléenne est **true** lorsque le caractère devient visible et **false** lorsque le caractère devient masqué.</span><span class="sxs-lookup"><span data-stu-id="6dced-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="6dced-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="6dced-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="6dced-113">Cause de la dernière modification de l’état de visibilité du caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="6dced-114">Le paramètre peut être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="6dced-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="6dced-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dced-115">Value</span></span>                                                                   | <span data-ttu-id="6dced-116">Description</span><span class="sxs-lookup"><span data-stu-id="6dced-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dced-117">**const unsigned short** **NeverShown = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="6dced-118">Le caractère n’a pas été affiché.</span><span class="sxs-lookup"><span data-stu-id="6dced-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="6dced-119">**const unsigned short** **UserHid = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="6dced-120">Utilisateur a masqué le caractère avec le menu contextuel de l’icône de barre des tâches du caractère ou avec une entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="6dced-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="6dced-121">**const unsigned short** **UserShowed = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="6dced-122">L’utilisateur a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="6dced-123">**const unsigned short** **ProgramHid = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="6dced-124">Votre application a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="6dced-125">**const unsigned short** **ProgramShowed = 4 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="6dced-126">Votre application a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="6dced-127">**const unsigned short** **OtherProgramHid = 5 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="6dced-128">Une autre application a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="6dced-129">**const unsigned short** **OtherProgramShowed = 6 ;**</span><span class="sxs-lookup"><span data-stu-id="6dced-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="6dced-130">Une autre application a montré le caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="6dced-131">**const non signé Short** **UserHidViaCharacterMenu = 7**</span><span class="sxs-lookup"><span data-stu-id="6dced-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="6dced-132">Utilisateur a masqué le caractère dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="6dced-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="6dced-133">**const non signed Short** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="6dced-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="6dced-134">Utilisateur a masqué le caractère dans le menu contextuel de l’icône de barre des tâches du caractère ou à l’aide d’une entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="6dced-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6dced-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dced-135">See Also</span></span>

<span data-ttu-id="6dced-136">[**IAgentCharacter :: getVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter :: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="6dced-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 





