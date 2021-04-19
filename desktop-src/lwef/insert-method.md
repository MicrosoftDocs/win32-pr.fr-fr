---
title: Insert, méthode
description: Insert, méthode
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106542846"
---
# <a name="insert-method"></a><span data-ttu-id="f219d-103">Insert, méthode</span><span class="sxs-lookup"><span data-stu-id="f219d-103">Insert Method</span></span>

<span data-ttu-id="f219d-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f219d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f219d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="f219d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f219d-106">Insère un objet **Command** dans la collection **Commands** .</span><span class="sxs-lookup"><span data-stu-id="f219d-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="f219d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="f219d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f219d-108">\*agent ***. Caractères («*** CharacterID \* \* * »). Commands. Insert* \*  *Name*, *RefName*, *avant*\_</span><span class="sxs-lookup"><span data-stu-id="f219d-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="f219d-109">*Légende*, *voix, activée, visible*</span><span class="sxs-lookup"><span data-stu-id="f219d-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="f219d-110">Partie</span><span class="sxs-lookup"><span data-stu-id="f219d-110">Part</span></span>      | <span data-ttu-id="f219d-111">Description</span><span class="sxs-lookup"><span data-stu-id="f219d-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f219d-112">*Nom*</span><span class="sxs-lookup"><span data-stu-id="f219d-112">*Name*</span></span>    | <span data-ttu-id="f219d-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f219d-113">Required.</span></span> <span data-ttu-id="f219d-114">Valeur de chaîne correspondant à l’ID que vous attribuez à la [**commande**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f219d-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="f219d-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="f219d-115">*RefName*</span></span> | <span data-ttu-id="f219d-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f219d-116">Required.</span></span> <span data-ttu-id="f219d-117">Valeur de chaîne correspondant au nom (ID) de la commande juste au-dessus ou au-dessous de l’emplacement où vous souhaitez insérer la nouvelle commande.</span><span class="sxs-lookup"><span data-stu-id="f219d-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="f219d-118">*Avant*</span><span class="sxs-lookup"><span data-stu-id="f219d-118">*Before*</span></span>  | <span data-ttu-id="f219d-119">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f219d-119">Optional.</span></span> <span data-ttu-id="f219d-120">Valeur booléenne indiquant s’il faut insérer la nouvelle commande avant la commande spécifiée par *RefName*.</span><span class="sxs-lookup"><span data-stu-id="f219d-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="f219d-121">**True** (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="f219d-121">**True** (Default).</span></span> <span data-ttu-id="f219d-122">La nouvelle commande est insérée avant la commande référencée.</span><span class="sxs-lookup"><span data-stu-id="f219d-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="f219d-123">**Valeur false** La nouvelle commande est insérée après la commande référencée.</span><span class="sxs-lookup"><span data-stu-id="f219d-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="f219d-124">*Caption*</span><span class="sxs-lookup"><span data-stu-id="f219d-124">*Caption*</span></span> | <span data-ttu-id="f219d-125">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f219d-125">Optional.</span></span> <span data-ttu-id="f219d-126">Valeur de chaîne correspondant au nom qui s’affiche dans le menu contextuel du caractère et dans la fenêtre commandes lorsque l’application cliente est active en entrée.</span><span class="sxs-lookup"><span data-stu-id="f219d-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="f219d-127">Pour plus d’informations, consultez la propriété [**Caption**](caption-property.md)de l’objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="f219d-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="f219d-128">*Voice*</span><span class="sxs-lookup"><span data-stu-id="f219d-128">*Voice*</span></span>   | <span data-ttu-id="f219d-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f219d-129">Optional.</span></span> <span data-ttu-id="f219d-130">Valeur de chaîne correspondant aux mots ou expressions à utiliser par le moteur de reconnaissance vocale pour la reconnaissance de cette commande.</span><span class="sxs-lookup"><span data-stu-id="f219d-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="f219d-131">Pour plus d’informations sur les alternatives de mise en forme pour la chaîne, consultez la propriété **Voice** de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="f219d-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="f219d-132">*Enabled*</span><span class="sxs-lookup"><span data-stu-id="f219d-132">*Enabled*</span></span> | <span data-ttu-id="f219d-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f219d-133">Optional.</span></span> <span data-ttu-id="f219d-134">Valeur booléenne indiquant si la commande est activée.</span><span class="sxs-lookup"><span data-stu-id="f219d-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="f219d-135">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="f219d-135">The default value is **True**.</span></span> <span data-ttu-id="f219d-136">Pour plus d’informations, consultez la propriété **Enabled** de l’objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="f219d-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="f219d-137">*Visible*</span><span class="sxs-lookup"><span data-stu-id="f219d-137">*Visible*</span></span> | <span data-ttu-id="f219d-138">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="f219d-138">Optional.</span></span> <span data-ttu-id="f219d-139">Valeur booléenne indiquant si la commande est visible dans la fenêtre commandes lorsque l’application cliente est en entrée active.</span><span class="sxs-lookup"><span data-stu-id="f219d-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="f219d-140">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="f219d-140">The default value is **True**.</span></span> <span data-ttu-id="f219d-141">Pour plus d’informations, consultez la propriété [**visible**](visible-property.md) de l’objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="f219d-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f219d-142">Notes</span><span class="sxs-lookup"><span data-stu-id="f219d-142">Remarks</span></span>

<span data-ttu-id="f219d-143">La valeur de la propriété [**Name**](name-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) doit être unique au sein de sa collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f219d-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="f219d-144">Vous devez supprimer une **commande** avant de pouvoir créer une nouvelle **commande** avec le même paramètre de propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="f219d-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="f219d-145">Toute tentative de création d’une **commande** avec une propriété **Name** qui existe déjà génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="f219d-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="f219d-146">Cette méthode retourne également un objet [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="f219d-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="f219d-147">Cela vous permet de déclarer un objet et de lui assigner une **commande** lorsque vous appelez la méthode **Insert** .</span><span class="sxs-lookup"><span data-stu-id="f219d-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="f219d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f219d-148">See Also</span></span>

<span data-ttu-id="f219d-149">Méthode [**Add**](add-method.md), méthode [**Remove**](remove-method.md), méthode [**RemoveAll**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="f219d-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

