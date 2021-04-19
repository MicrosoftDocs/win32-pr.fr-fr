---
title: Événement DragComplete
description: Événement DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a02fe98e4cf3cdefc1b7734305067550e4923
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512448"
---
# <a name="dragcomplete-event"></a><span data-ttu-id="2ded7-103">Événement DragComplete</span><span class="sxs-lookup"><span data-stu-id="2ded7-103">DragComplete Event</span></span>

<span data-ttu-id="2ded7-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ded7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2ded7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="2ded7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2ded7-106">Se produit lorsque l’utilisateur termine le glissement d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="2ded7-106">Occurs when the user completes dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="2ded7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="2ded7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2ded7-108">**Sub** *agent \* \* \* \_ DragComplete* \*  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *MAJ*, **ByVal** *X*, **ByVal** *Y \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="2ded7-108">**Sub** *agent\*\*\*\_DragComplete*\* **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="2ded7-109">Partie</span><span class="sxs-lookup"><span data-stu-id="2ded7-109">Part</span></span>          | <span data-ttu-id="2ded7-110">Description</span><span class="sxs-lookup"><span data-stu-id="2ded7-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ded7-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="2ded7-111">*CharacterID*</span></span> | <span data-ttu-id="2ded7-112">Retourne l’ID du caractère déplacé sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="2ded7-112">Returns the ID of the dragged character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2ded7-113">*Button*</span><span class="sxs-lookup"><span data-stu-id="2ded7-113">*Button*</span></span>      | <span data-ttu-id="2ded7-114">Retourne un entier qui identifie le bouton qui a été enfoncé et relâché pour déclencher l’événement.</span><span class="sxs-lookup"><span data-stu-id="2ded7-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="2ded7-115">L’argument Button est un champ de bits avec les bits correspondant au bouton gauche (bit 0), le bouton droit (bit 1) et le bouton central (bit 2).</span><span class="sxs-lookup"><span data-stu-id="2ded7-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="2ded7-116">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="2ded7-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2ded7-117">Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2ded7-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2ded7-118">*Majuscule*</span><span class="sxs-lookup"><span data-stu-id="2ded7-118">*Shift*</span></span>       | <span data-ttu-id="2ded7-119">Retourne un entier qui correspond à l’état des touches Maj, CTRL et ALT lorsque le bouton spécifié dans l’argument de bouton est enfoncé ou relâché.</span><span class="sxs-lookup"><span data-stu-id="2ded7-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="2ded7-120">Un bit est défini si la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="2ded7-120">A bit is set if the key is down.</span></span> <span data-ttu-id="2ded7-121">L’argument Shift est un champ de bits avec les bits de poids faible correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2).</span><span class="sxs-lookup"><span data-stu-id="2ded7-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="2ded7-122">Ces bits correspondent respectivement aux valeurs 1, 2 et 4.</span><span class="sxs-lookup"><span data-stu-id="2ded7-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="2ded7-123">L’argument Shift indique l’état de ces clés.</span><span class="sxs-lookup"><span data-stu-id="2ded7-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="2ded7-124">Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="2ded7-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="2ded7-125">Par exemple, si les touches CTRL et ALT étaient enfoncées, la valeur de Shift serait 6.</span><span class="sxs-lookup"><span data-stu-id="2ded7-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="2ded7-126">*X, Y*</span><span class="sxs-lookup"><span data-stu-id="2ded7-126">*X,Y*</span></span>         | <span data-ttu-id="2ded7-127">Retourne un entier qui spécifie l’emplacement actuel du pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="2ded7-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="2ded7-128">Les valeurs X et Y sont toujours exprimées en pixels, par rapport à l’angle supérieur gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="2ded7-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="2ded7-129">Notes</span><span class="sxs-lookup"><span data-stu-id="2ded7-129">Remarks</span></span>

<span data-ttu-id="2ded7-130">Cet événement est envoyé uniquement au client d’entrée-actif d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="2ded7-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="2ded7-131">Lorsque l’utilisateur fait glisser un caractère sans client d’entrée-actif, le serveur définit son dernier client d’entrée/de sortie en tant que client en entrée-actif, en envoyant l’événement [**ActivateInput**](activateinput-event.md) à ce client, puis en envoyant les événements [**DragStart**](dragstart-event.md) et **DragComplete** .</span><span class="sxs-lookup"><span data-stu-id="2ded7-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the [**DragStart**](dragstart-event.md) and **DragComplete** events.</span></span>

### <a name="see-also"></a><span data-ttu-id="2ded7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ded7-132">See Also</span></span>

[<span data-ttu-id="2ded7-133">**Événement DragStart**</span><span class="sxs-lookup"><span data-stu-id="2ded7-133">**DragStart event**</span></span>](dragstart-event.md)


 

 




