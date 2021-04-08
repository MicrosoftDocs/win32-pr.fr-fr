---
title: Propriété MoveCause
description: Propriété MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840094"
---
# <a name="movecause-property"></a><span data-ttu-id="95304-103">Propriété MoveCause</span><span class="sxs-lookup"><span data-stu-id="95304-103">MoveCause Property</span></span>

<span data-ttu-id="95304-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="95304-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="95304-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="95304-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="95304-106">Retourne une valeur entière qui spécifie ce qui a provoqué le dernier déplacement du caractère.</span><span class="sxs-lookup"><span data-stu-id="95304-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="95304-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="95304-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="95304-108">*agent*. **Caractères («***CharacterID***»). MoveCause**</span><span class="sxs-lookup"><span data-stu-id="95304-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="95304-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="95304-109">Value</span></span> | <span data-ttu-id="95304-110">Description</span><span class="sxs-lookup"><span data-stu-id="95304-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="95304-111">0</span><span class="sxs-lookup"><span data-stu-id="95304-111">0</span></span>     | <span data-ttu-id="95304-112">Le caractère n’a pas été déplacé.</span><span class="sxs-lookup"><span data-stu-id="95304-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="95304-113">1</span><span class="sxs-lookup"><span data-stu-id="95304-113">1</span></span>     | <span data-ttu-id="95304-114">L’utilisateur a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="95304-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="95304-115">2</span><span class="sxs-lookup"><span data-stu-id="95304-115">2</span></span>     | <span data-ttu-id="95304-116">Votre application a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="95304-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="95304-117">3</span><span class="sxs-lookup"><span data-stu-id="95304-117">3</span></span>     | <span data-ttu-id="95304-118">Une autre application cliente a déplacé le caractère.</span><span class="sxs-lookup"><span data-stu-id="95304-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="95304-119">4</span><span class="sxs-lookup"><span data-stu-id="95304-119">4</span></span>     | <span data-ttu-id="95304-120">Le serveur de l’agent a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran.</span><span class="sxs-lookup"><span data-stu-id="95304-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95304-121">Notes</span><span class="sxs-lookup"><span data-stu-id="95304-121">Remarks</span></span>

<span data-ttu-id="95304-122">Vous pouvez utiliser cette propriété pour déterminer ce qui a provoqué le déplacement du caractère, lorsque plusieurs applications partagent le même caractère.</span><span class="sxs-lookup"><span data-stu-id="95304-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="95304-123">Ces valeurs sont les mêmes que celles retournées par l’événement [**Move**](move-event.md) .</span><span class="sxs-lookup"><span data-stu-id="95304-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="95304-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95304-124">See Also</span></span>

<span data-ttu-id="95304-125">[**Move, événement**](move-event.md), [ **méthode MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="95304-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




