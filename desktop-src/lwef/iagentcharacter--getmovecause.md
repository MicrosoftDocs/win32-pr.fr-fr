---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119683"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="d0ffd-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="d0ffd-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="d0ffd-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0ffd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="d0ffd-105">Récupère la cause du dernier déplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="d0ffd-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d0ffd-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="d0ffd-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="d0ffd-108">Adresse d’une variable qui reçoit la cause du dernier déplacement du caractère et sera l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="d0ffd-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="d0ffd-109">Value</span><span class="sxs-lookup"><span data-stu-id="d0ffd-109">Value</span></span>                                                               | <span data-ttu-id="d0ffd-110">Description</span><span class="sxs-lookup"><span data-stu-id="d0ffd-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ffd-111">**const unsigned short** **NeverMoved = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="d0ffd-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="d0ffd-112">Le caractère n’a pas été déplacé.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="d0ffd-113">**const unsigned short** **UserMoved = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="d0ffd-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="d0ffd-114">L’utilisateur a fait glisser le caractère.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="d0ffd-115">**const unsigned short** **ProgramMoved = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="d0ffd-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="d0ffd-116">Votre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="d0ffd-117">**const unsigned short** **OtherProgramMoved = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="d0ffd-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="d0ffd-118">Une autre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="d0ffd-119">**const non signé Short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="d0ffd-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="d0ffd-120">Le serveur a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran.</span><span class="sxs-lookup"><span data-stu-id="d0ffd-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d0ffd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0ffd-121">See Also</span></span>

[<span data-ttu-id="d0ffd-122">**IAgentNotifySink :: Move**</span><span class="sxs-lookup"><span data-stu-id="d0ffd-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





