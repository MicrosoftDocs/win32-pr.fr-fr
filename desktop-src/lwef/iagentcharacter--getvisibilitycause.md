---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380442"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="64528-103">IAgentCharacter::GetVisibilityCause</span><span class="sxs-lookup"><span data-stu-id="64528-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="64528-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="64528-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="64528-105">Récupère la cause de l’état visible du caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="64528-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="64528-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="64528-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="64528-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="64528-108">Adresse d’une variable qui reçoit la cause de la modification de l’état de la dernière visibilité du caractère et sera l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="64528-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="64528-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="64528-109">Value</span></span>                                                                   | <span data-ttu-id="64528-110">Description</span><span class="sxs-lookup"><span data-stu-id="64528-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="64528-111">**const unsigned short** **NeverShown = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="64528-112">Le caractère n’a pas été affiché.</span><span class="sxs-lookup"><span data-stu-id="64528-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="64528-113">**const unsigned short** **UserHid = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="64528-114">Utilisateur a masqué le caractère dans le menu contextuel de l’icône de barre des tâches du caractère ou à l’aide d’une entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="64528-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="64528-115">**const unsigned short** **UserShowed = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="64528-116">L’utilisateur a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="64528-117">**const unsigned short** **ProgramHid = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="64528-118">Votre application a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="64528-119">**const unsigned short** **ProgramShowed = 4 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="64528-120">Votre application a affiché le caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="64528-121">**const unsigned short** **OtherProgramHid = 5 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="64528-122">Une autre application a masqué le caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="64528-123">**const unsigned short** **OtherProgramShowed = 6 ;**</span><span class="sxs-lookup"><span data-stu-id="64528-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="64528-124">Une autre application a montré le caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="64528-125">**const non signé Short** **UserHidViaCharacterMenu = 7**</span><span class="sxs-lookup"><span data-stu-id="64528-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="64528-126">Utilisateur a masqué le caractère dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="64528-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="64528-127">**const non signed Short** **UserHidViaTaskbarIcon = UserHid**</span><span class="sxs-lookup"><span data-stu-id="64528-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="64528-128">Utilisateur a masqué le caractère dans le menu contextuel de l’icône de barre des tâches du caractère ou à l’aide d’une entrée vocale.</span><span class="sxs-lookup"><span data-stu-id="64528-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="64528-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64528-129">See Also</span></span>

[<span data-ttu-id="64528-130">**IAgentNotifySink::VisibleState**</span><span class="sxs-lookup"><span data-stu-id="64528-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 





