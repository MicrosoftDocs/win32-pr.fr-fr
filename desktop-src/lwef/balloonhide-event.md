---
title: Événement BalloonHide
description: Événement BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197299"
---
# <a name="balloonhide-event"></a><span data-ttu-id="a4484-103">Événement BalloonHide</span><span class="sxs-lookup"><span data-stu-id="a4484-103">BalloonHide Event</span></span>

<span data-ttu-id="a4484-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4484-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a4484-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="a4484-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a4484-106">Se produit lorsque la bulle de texte d’un caractère est masquée.</span><span class="sxs-lookup"><span data-stu-id="a4484-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="a4484-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="a4484-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a4484-108">**Sub** *agent* \_ **BalloonHide** **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="a4484-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="a4484-109">Partie</span><span class="sxs-lookup"><span data-stu-id="a4484-109">Part</span></span>          | <span data-ttu-id="a4484-110">Description</span><span class="sxs-lookup"><span data-stu-id="a4484-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="a4484-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="a4484-111">*CharacterID*</span></span> | <span data-ttu-id="a4484-112">Retourne l’ID du caractère associé au mot-bulle.</span><span class="sxs-lookup"><span data-stu-id="a4484-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="a4484-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a4484-113">Remarks</span></span>

<span data-ttu-id="a4484-114">Le serveur envoie cet événement uniquement aux clients du caractère (applications qui ont chargé le caractère) qui utilise le mot-bulle.</span><span class="sxs-lookup"><span data-stu-id="a4484-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="a4484-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4484-115">See Also</span></span>

[<span data-ttu-id="a4484-116">**Événement BalloonShow**</span><span class="sxs-lookup"><span data-stu-id="a4484-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




