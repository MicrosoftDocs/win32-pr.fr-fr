---
title: Propriété Active
description: Propriété Active
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196768"
---
# <a name="active-property"></a><span data-ttu-id="ee21d-103">Propriété Active</span><span class="sxs-lookup"><span data-stu-id="ee21d-103">Active Property</span></span>

<span data-ttu-id="ee21d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ee21d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ee21d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="ee21d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ee21d-106">Retourne une valeur indiquant si votre application est le client actif du caractère et si le caractère est le plus haut.</span><span class="sxs-lookup"><span data-stu-id="ee21d-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="ee21d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="ee21d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ee21d-108">\*agent. ***Caractères \* \* \* \* ("*** CharacterID \* \* *").* \*  \[  =  *État* actif\]</span><span class="sxs-lookup"><span data-stu-id="ee21d-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="ee21d-109">Partie</span><span class="sxs-lookup"><span data-stu-id="ee21d-109">Part</span></span>    | <span data-ttu-id="ee21d-110">Description</span><span class="sxs-lookup"><span data-stu-id="ee21d-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee21d-111">*state*</span><span class="sxs-lookup"><span data-stu-id="ee21d-111">*state*</span></span> | <span data-ttu-id="ee21d-112">Expression entière spécifiant l’état de votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="ee21d-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="ee21d-113">0 n’est pas le client actif.</span><span class="sxs-lookup"><span data-stu-id="ee21d-113">0 Not the active client.</span></span><br/> <span data-ttu-id="ee21d-114">1 le client actif.</span><span class="sxs-lookup"><span data-stu-id="ee21d-114">1 The active client.</span></span> <br/> <span data-ttu-id="ee21d-115">2 le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="ee21d-115">2 The input-active client.</span></span> <span data-ttu-id="ee21d-116">(Le caractère le plus élevé.)</span><span class="sxs-lookup"><span data-stu-id="ee21d-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee21d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ee21d-117">Remarks</span></span>

<span data-ttu-id="ee21d-118">Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements [**Click**](click-event.md) ou [DragStart](dragstart-event.md) du contrôle Microsoft Agent).</span><span class="sxs-lookup"><span data-stu-id="ee21d-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="ee21d-119">De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements de commande.</span><span class="sxs-lookup"><span data-stu-id="ee21d-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="ee21d-120">Vous pouvez utiliser la méthode [**Activate**](activate-method.md)pour définir si votre application est le client actif du personnage ou pour faire de votre application le client actif d’entrée (ce qui rend également le caractère le plus haut).</span><span class="sxs-lookup"><span data-stu-id="ee21d-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="ee21d-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee21d-121">See Also</span></span>

[<span data-ttu-id="ee21d-122">Activate \* \*, méthode \* \*</span><span class="sxs-lookup"><span data-stu-id="ee21d-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





