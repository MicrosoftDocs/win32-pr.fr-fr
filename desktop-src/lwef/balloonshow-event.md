---
title: Événement BalloonShow
description: Événement BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380206"
---
# <a name="balloonshow-event"></a><span data-ttu-id="3367e-103">Événement BalloonShow</span><span class="sxs-lookup"><span data-stu-id="3367e-103">BalloonShow Event</span></span>

<span data-ttu-id="3367e-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3367e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3367e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="3367e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3367e-106">Se produit lorsque la bulle de texte d’un caractère est affichée.</span><span class="sxs-lookup"><span data-stu-id="3367e-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="3367e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="3367e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3367e-108">**Sub** *agent* \_ **BalloonShow** **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="3367e-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="3367e-109">Partie</span><span class="sxs-lookup"><span data-stu-id="3367e-109">Part</span></span>          | <span data-ttu-id="3367e-110">Description</span><span class="sxs-lookup"><span data-stu-id="3367e-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="3367e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="3367e-111">*CharacterID*</span></span> | <span data-ttu-id="3367e-112">Retourne l’ID du caractère associé au mot-bulle.</span><span class="sxs-lookup"><span data-stu-id="3367e-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3367e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3367e-113">Remarks</span></span>

<span data-ttu-id="3367e-114">Le serveur envoie cet événement uniquement aux clients du caractère (applications qui ont chargé le caractère) qui utilise le mot-bulle.</span><span class="sxs-lookup"><span data-stu-id="3367e-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="3367e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3367e-115">See Also</span></span>

[<span data-ttu-id="3367e-116">**Événement BalloonHide**</span><span class="sxs-lookup"><span data-stu-id="3367e-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




