---
title: Ajouter une méthode
description: Ajouter une méthode
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029098"
---
# <a name="add-method"></a><span data-ttu-id="9bbf5-103">Ajouter une méthode</span><span class="sxs-lookup"><span data-stu-id="9bbf5-103">Add Method</span></span>

<span data-ttu-id="9bbf5-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9bbf5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9bbf5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="9bbf5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9bbf5-106">Ajoute un objet [Command](the-command-object.md) à la collection [Commands](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="9bbf5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="9bbf5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9bbf5-108">\*agent ***. Caractères («*** CharacterID \* \* * »). Commandes. Ajouter* un \*  *nom*, une *légende*, une *voix*, *activé*, *visible*</span><span class="sxs-lookup"><span data-stu-id="9bbf5-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="9bbf5-109">Partie</span><span class="sxs-lookup"><span data-stu-id="9bbf5-109">Part</span></span>      | <span data-ttu-id="9bbf5-110">Description</span><span class="sxs-lookup"><span data-stu-id="9bbf5-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbf5-111">*Nom*</span><span class="sxs-lookup"><span data-stu-id="9bbf5-111">*Name*</span></span>    | <span data-ttu-id="9bbf5-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-112">Required.</span></span> <span data-ttu-id="9bbf5-113">Valeur de chaîne correspondant à l’ID que vous attribuez à la commande.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="9bbf5-114">*Caption*</span><span class="sxs-lookup"><span data-stu-id="9bbf5-114">*Caption*</span></span> | <span data-ttu-id="9bbf5-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-115">Optional.</span></span> <span data-ttu-id="9bbf5-116">Valeur de chaîne correspondant au nom qui s’affiche dans le menu contextuel du caractère et dans la fenêtre commandes lorsque l’application cliente est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="9bbf5-117">Pour plus d’informations, consultez la propriété [Caption](caption-property.md) de l’objet [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="9bbf5-118">*Voice*</span><span class="sxs-lookup"><span data-stu-id="9bbf5-118">*Voice*</span></span>   | <span data-ttu-id="9bbf5-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-119">Optional.</span></span> <span data-ttu-id="9bbf5-120">Valeur de chaîne correspondant aux mots ou expressions à utiliser par le moteur de reconnaissance vocale pour la reconnaissance de cette commande.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="9bbf5-121">Pour plus d’informations sur les alternatives de mise en forme pour la chaîne, consultez la propriété [Voice](voice-property.md) de l’objet de [commande](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="9bbf5-122">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="9bbf5-122">*Enabled*</span></span> | <span data-ttu-id="9bbf5-123">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-123">Optional.</span></span> <span data-ttu-id="9bbf5-124">Valeur booléenne indiquant si la commande est activée.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="9bbf5-125">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-125">The default value is **True**.</span></span> <span data-ttu-id="9bbf5-126">Pour plus d’informations, consultez la propriété [Enabled](enabled-property.md) de l’objet [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="9bbf5-127">*Visible*</span><span class="sxs-lookup"><span data-stu-id="9bbf5-127">*Visible*</span></span> | <span data-ttu-id="9bbf5-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-128">Optional.</span></span> <span data-ttu-id="9bbf5-129">Valeur booléenne indiquant si la commande est visible dans le menu contextuel du caractère lorsque l’application cliente est en entrée active.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="9bbf5-130">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-130">The default value is **True**.</span></span> <span data-ttu-id="9bbf5-131">Pour plus d’informations, consultez la propriété [visible](visible-property.md) de l’objet [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bbf5-132">Notes</span><span class="sxs-lookup"><span data-stu-id="9bbf5-132">Remarks</span></span>

<span data-ttu-id="9bbf5-133">La valeur de la propriété [Name](name-property.md) d’un objet [Command](the-command-object.md) doit être unique au sein de sa collection [Commands](the-commands-collection-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="9bbf5-134">Vous devez supprimer une commande avant de pouvoir créer une nouvelle commande avec le même paramètre de propriété Name.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="9bbf5-135">Toute tentative de création d’une commande avec une propriété Name qui existe déjà génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="9bbf5-136">Cette méthode retourne également un objet [Command](the-command-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbf5-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="9bbf5-137">Cela vous permet de déclarer un objet et de lui assigner une commande lorsque vous appelez addMethod.</span><span class="sxs-lookup"><span data-stu-id="9bbf5-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="9bbf5-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bbf5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bbf5-139">**Insert (méthode)**</span><span class="sxs-lookup"><span data-stu-id="9bbf5-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="9bbf5-140">**RemoveAll, méthode**</span><span class="sxs-lookup"><span data-stu-id="9bbf5-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="9bbf5-141">**Remove (méthode)**</span><span class="sxs-lookup"><span data-stu-id="9bbf5-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




