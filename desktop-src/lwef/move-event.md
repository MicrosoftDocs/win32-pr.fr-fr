---
title: Déplacer l’événement
description: Déplacer l’événement
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840093"
---
# <a name="move-event"></a><span data-ttu-id="c12c4-103">Déplacer l’événement</span><span class="sxs-lookup"><span data-stu-id="c12c4-103">Move Event</span></span>

<span data-ttu-id="c12c4-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c12c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c12c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="c12c4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c12c4-106">Se produit lorsqu’un caractère est déplacé.</span><span class="sxs-lookup"><span data-stu-id="c12c4-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="c12c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="c12c4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c12c4-108">**Sub** *agent* \_ **Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="c12c4-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="c12c4-109">Partie</span><span class="sxs-lookup"><span data-stu-id="c12c4-109">Part</span></span>          | <span data-ttu-id="c12c4-110">Description</span><span class="sxs-lookup"><span data-stu-id="c12c4-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12c4-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="c12c4-111">*CharacterID*</span></span> | <span data-ttu-id="c12c4-112">Retourne l’ID du caractère qui a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c12c4-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c12c4-113">*X*</span><span class="sxs-lookup"><span data-stu-id="c12c4-113">*X*</span></span>           | <span data-ttu-id="c12c4-114">Retourne la coordonnée x (en pixels) du bord supérieur du nouvel emplacement du cadre de caractère sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="c12c4-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="c12c4-115">*O*</span><span class="sxs-lookup"><span data-stu-id="c12c4-115">*Y*</span></span>           | <span data-ttu-id="c12c4-116">Retourne la coordonnée y (en pixels) du bord gauche du nouvel emplacement du cadre de caractère sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="c12c4-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="c12c4-117">*Cause*</span><span class="sxs-lookup"><span data-stu-id="c12c4-117">*Cause*</span></span>       | <span data-ttu-id="c12c4-118">Retourne une valeur qui indique ce qui a provoqué le déplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="c12c4-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="c12c4-119">1 l’utilisateur a fait glisser le caractère.</span><span class="sxs-lookup"><span data-stu-id="c12c4-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="c12c4-120">2 votre application cliente a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="c12c4-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="c12c4-121">3 une autre application cliente a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="c12c4-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="c12c4-122">4 le serveur de l’agent a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran.</span><span class="sxs-lookup"><span data-stu-id="c12c4-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="c12c4-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c12c4-123">Remarks</span></span>

<span data-ttu-id="c12c4-124">Cet événement se produit lorsque l’utilisateur ou une application modifie la position du caractère.</span><span class="sxs-lookup"><span data-stu-id="c12c4-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="c12c4-125">Les coordonnées sont pertinentes dans l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="c12c4-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="c12c4-126">Cet événement est envoyé uniquement aux clients du caractère (applications qui ont chargé le caractère).</span><span class="sxs-lookup"><span data-stu-id="c12c4-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="c12c4-127">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="c12c4-127">**See Also**</span></span>

<span data-ttu-id="c12c4-128">[**Propriété MoveCause**](movecause-property.md), [ **événement Size**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="c12c4-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 





