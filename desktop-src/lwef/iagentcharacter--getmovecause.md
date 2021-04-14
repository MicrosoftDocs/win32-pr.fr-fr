---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380446"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="6bfeb-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="6bfeb-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="6bfeb-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6bfeb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="6bfeb-105">Récupère la cause du dernier déplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="6bfeb-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6bfeb-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="6bfeb-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="6bfeb-108">Adresse d’une variable qui reçoit la cause du dernier déplacement du caractère et sera l’une des suivantes :</span><span class="sxs-lookup"><span data-stu-id="6bfeb-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6bfeb-109">**const unsigned short** **NeverMoved = 0 ;**</span><span class="sxs-lookup"><span data-stu-id="6bfeb-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="6bfeb-110">Le caractère n’a pas été déplacé.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="6bfeb-111">**const unsigned short** **UserMoved = 1 ;**</span><span class="sxs-lookup"><span data-stu-id="6bfeb-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="6bfeb-112">L’utilisateur a fait glisser le caractère.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="6bfeb-113">**const unsigned short** **ProgramMoved = 2 ;**</span><span class="sxs-lookup"><span data-stu-id="6bfeb-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="6bfeb-114">Votre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="6bfeb-115">**const unsigned short** **OtherProgramMoved = 3 ;**</span><span class="sxs-lookup"><span data-stu-id="6bfeb-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="6bfeb-116">Une autre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="6bfeb-117">**const non signé Short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="6bfeb-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="6bfeb-118">Le serveur a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran.</span><span class="sxs-lookup"><span data-stu-id="6bfeb-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6bfeb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bfeb-119">See Also</span></span>

[<span data-ttu-id="6bfeb-120">**IAgentNotifySink :: Move**</span><span class="sxs-lookup"><span data-stu-id="6bfeb-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





