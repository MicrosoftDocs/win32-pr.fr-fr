---
title: Événement HelpComplete
description: Événement HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106543048"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="53547-103">Événement HelpComplete</span><span class="sxs-lookup"><span data-stu-id="53547-103">HelpComplete Event</span></span>

<span data-ttu-id="53547-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53547-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="53547-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="53547-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="53547-106">Indique que le mode d’aide contextuelle a été quitté.</span><span class="sxs-lookup"><span data-stu-id="53547-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="53547-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="53547-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="53547-108">**Sub** *agent. \* \* \* (ByVal* \*  \*CharacterID \* \* *, ByVal* \*  \*Name \* \* *, ByVal* \*  *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="53547-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="53547-109">Partie</span><span class="sxs-lookup"><span data-stu-id="53547-109">Part</span></span>          | <span data-ttu-id="53547-110">Description</span><span class="sxs-lookup"><span data-stu-id="53547-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53547-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="53547-111">*CharacterID*</span></span> | <span data-ttu-id="53547-112">Retourne l’ID du caractère sur lequel l’utilisateur a cliqué sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="53547-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="53547-113">*Nom*</span><span class="sxs-lookup"><span data-stu-id="53547-113">*Name*</span></span>        | <span data-ttu-id="53547-114">Retourne une valeur de chaîne identifiant le nom (ID) de la commande.</span><span class="sxs-lookup"><span data-stu-id="53547-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="53547-115">*Cause*</span><span class="sxs-lookup"><span data-stu-id="53547-115">*Cause*</span></span>       | <span data-ttu-id="53547-116">Retourne une valeur qui indique ce qui a provoqué l’exécution du mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="53547-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="53547-117">1 l’utilisateur a sélectionné une commande fournie par votre application.</span><span class="sxs-lookup"><span data-stu-id="53547-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="53547-118">2 l’utilisateur a sélectionné l’objet [**commandes**](/windows/desktop/lwef/the-commands-collection-object) d’un autre client.</span><span class="sxs-lookup"><span data-stu-id="53547-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="53547-119">3 l’utilisateur a sélectionné la commande ouvrir les commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="53547-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="53547-120">4 l’utilisateur a sélectionné la commande fermer les commandes vocales.</span><span class="sxs-lookup"><span data-stu-id="53547-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="53547-121">5 l’utilisateur a sélectionné la commande show *CharacterName* .</span><span class="sxs-lookup"><span data-stu-id="53547-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="53547-122">6 l’utilisateur a sélectionné la commande masquer *CharacterName* .</span><span class="sxs-lookup"><span data-stu-id="53547-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="53547-123">7 l’utilisateur a sélectionné (sur) le caractère.</span><span class="sxs-lookup"><span data-stu-id="53547-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="53547-124">Notes</span><span class="sxs-lookup"><span data-stu-id="53547-124">Remarks</span></span>

<span data-ttu-id="53547-125">En général, le mode d’aide se termine lorsque l’utilisateur clique ou fait glisser le caractère ou sélectionne une commande dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="53547-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="53547-126">Le fait de cliquer sur un autre caractère ou sur un autre emplacement de l’écran n’annule pas le mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="53547-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="53547-127">Le client qui définit le mode d’aide pour le caractère peut annuler le mode d’aide en affectant à [**HelpModeOn**](helpmodeon-property.md) la **valeur false**.</span><span class="sxs-lookup"><span data-stu-id="53547-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="53547-128">(Cela ne déclenche pas l’événement **HelpComplete** .)</span><span class="sxs-lookup"><span data-stu-id="53547-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="53547-129">Lorsque l’utilisateur sélectionne une commande à partir du menu contextuel du caractère en mode d’aide, le serveur supprime le menu, appelle l’aide avec la [**HelpContextID**](helpcontextid-property.md)spécifiée de la commande et envoie cet événement.</span><span class="sxs-lookup"><span data-stu-id="53547-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="53547-130">Le contexte (également appelé « qu’est-ce que c’est ? ») La fenêtre d’aide s’affiche à l’emplacement du pointeur.</span><span class="sxs-lookup"><span data-stu-id="53547-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="53547-131">Si l’utilisateur sélectionne la commande par entrée vocale, la fenêtre d’aide s’affiche sur le caractère.</span><span class="sxs-lookup"><span data-stu-id="53547-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="53547-132">Si le caractère est hors écran, la fenêtre s’affiche à l’écran le plus proche de la position actuelle du caractère.</span><span class="sxs-lookup"><span data-stu-id="53547-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="53547-133">Si le serveur retourne le nom sous la forme d’une chaîne vide (""), il indique que l’utilisateur a sélectionné une commande fournie par le serveur.</span><span class="sxs-lookup"><span data-stu-id="53547-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="53547-134">Cet événement est envoyé uniquement à l’application cliente qui place le caractère en mode d’aide.</span><span class="sxs-lookup"><span data-stu-id="53547-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="53547-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53547-135">See Also</span></span>

<span data-ttu-id="53547-136">[**Propriété HelpModeOn**](helpmodeon-property.md), [ **HelpContextID, propriété**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="53547-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

