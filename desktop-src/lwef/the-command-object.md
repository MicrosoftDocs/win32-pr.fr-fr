---
title: Objet Command
description: Objet Command
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509841"
---
# <a name="the-command-object"></a><span data-ttu-id="1f1a0-103">Objet Command</span><span class="sxs-lookup"><span data-stu-id="1f1a0-103">The Command Object</span></span>

<span data-ttu-id="1f1a0-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1f1a0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="1f1a0-105">Un objet [**Command**](/windows/desktop/lwef/the-command-object) est un élément d’une collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="1f1a0-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="1f1a0-106">Le serveur permet à l’utilisateur d’accéder à vos objets de **commande** lorsque votre application cliente devient entrée-active.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="1f1a0-107">Propriétés de l’objet Command</span><span class="sxs-lookup"><span data-stu-id="1f1a0-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="1f1a0-108">Pour accéder à la propriété d’un objet [**Command**](/windows/desktop/lwef/the-command-object) , vous le référencez dans sa collection à l’aide de sa propriété [**Name**](name-property.md) .</span><span class="sxs-lookup"><span data-stu-id="1f1a0-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="1f1a0-109">Dans VBScript et Visual Basic vous pouvez utiliser directement la propriété **Name** :</span><span class="sxs-lookup"><span data-stu-id="1f1a0-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="1f1a0-110">Pour les langages de programmation qui ne prennent pas en charge les collections, utilisez la méthode [**Command**](command-method.md) :</span><span class="sxs-lookup"><span data-stu-id="1f1a0-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="1f1a0-111">Vous pouvez également référencer un objet de commande en créant une référence à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="1f1a0-112">Dans Visual Basic, déclarez une variable objet et utilisez l’instruction SET pour créer la référence :</span><span class="sxs-lookup"><span data-stu-id="1f1a0-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="1f1a0-113">Dans Visual Basic 5,0, vous pouvez également déclarer l’objet comme type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) et créer la référence.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="1f1a0-114">Cette Convention permet une liaison précoce, ce qui améliore les performances :</span><span class="sxs-lookup"><span data-stu-id="1f1a0-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="1f1a0-115">Dans VBScript, vous pouvez déclarer une référence en tant que type particulier, mais vous pouvez toujours déclarer la variable et la définir sur la [**commande**](/windows/desktop/lwef/the-command-object) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="1f1a0-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="1f1a0-116">Une commande peut apparaître dans le menu contextuel du caractère et dans la fenêtre commandes, ou dans les deux.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="1f1a0-117">Pour apparaître dans le menu contextuel, il doit avoir une légende et la propriété [**visible**](visible-property.md) doit avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="1f1a0-118">En outre, sa propriété **visible** de l’objet de collection Commands doit également avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="1f1a0-119">Pour apparaître dans la fenêtre commandes, la [**légende**](caption-property.md) et les propriétés [**vocales**](voice-property.md) doivent être définies pour une [**commande**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="1f1a0-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="1f1a0-120">Notez que les entrées du menu contextuel d’un caractère ne changent pas pendant que le menu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="1f1a0-121">Si vous ajoutez ou supprimez des commandes ou modifiez leurs propriétés alors que le menu contextuel du caractère s’affiche, le menu affiche ces modifications chaque fois que l’utilisateur l’affiche à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="1f1a0-122">Toutefois, la fenêtre commandes reflète dynamiquement les modifications que vous apportez.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="1f1a0-123">Le tableau suivant résume la façon dont les propriétés d’une [**commande**](/windows/desktop/lwef/the-command-object) affectent sa présentation :</span><span class="sxs-lookup"><span data-stu-id="1f1a0-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="1f1a0-124">Propriété Caption</span><span class="sxs-lookup"><span data-stu-id="1f1a0-124">Caption Property</span></span>

<span data-ttu-id="1f1a0-125">Voice-Caption, propriété</span><span class="sxs-lookup"><span data-stu-id="1f1a0-125">Voice-Caption Property</span></span>

<span data-ttu-id="1f1a0-126">Voice, propriété</span><span class="sxs-lookup"><span data-stu-id="1f1a0-126">Voice Property</span></span>

<span data-ttu-id="1f1a0-127">Propriété visible</span><span class="sxs-lookup"><span data-stu-id="1f1a0-127">Visible Property</span></span>

<span data-ttu-id="1f1a0-128">Propriété activée</span><span class="sxs-lookup"><span data-stu-id="1f1a0-128">Enabled Property</span></span>

<span data-ttu-id="1f1a0-129">Apparaît dans le menu contextuel du caractère</span><span class="sxs-lookup"><span data-stu-id="1f1a0-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="1f1a0-130">Apparaît dans la fenêtre commandes</span><span class="sxs-lookup"><span data-stu-id="1f1a0-130">Appears in Commands Window</span></span>

<span data-ttu-id="1f1a0-131">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-131">Yes</span></span>

<span data-ttu-id="1f1a0-132">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-132">Yes</span></span>

<span data-ttu-id="1f1a0-133">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-133">Yes</span></span>

<span data-ttu-id="1f1a0-134">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-134">True</span></span>

<span data-ttu-id="1f1a0-135">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-135">True</span></span>

<span data-ttu-id="1f1a0-136">Normal, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-137">Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="1f1a0-138">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-138">Yes</span></span>

<span data-ttu-id="1f1a0-139">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-139">Yes</span></span>

<span data-ttu-id="1f1a0-140">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-140">Yes</span></span>

<span data-ttu-id="1f1a0-141">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-141">True</span></span>

<span data-ttu-id="1f1a0-142">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-142">False</span></span>

<span data-ttu-id="1f1a0-143">Désactivé, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-144">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-144">No</span></span>

<span data-ttu-id="1f1a0-145">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-145">Yes</span></span>

<span data-ttu-id="1f1a0-146">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-146">Yes</span></span>

<span data-ttu-id="1f1a0-147">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-147">Yes</span></span>

<span data-ttu-id="1f1a0-148">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-148">False</span></span>

<span data-ttu-id="1f1a0-149">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-149">True</span></span>

<span data-ttu-id="1f1a0-150">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-150">Does not appear</span></span>

<span data-ttu-id="1f1a0-151">Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="1f1a0-152">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-152">Yes</span></span>

<span data-ttu-id="1f1a0-153">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-153">Yes</span></span>

<span data-ttu-id="1f1a0-154">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-154">Yes</span></span>

<span data-ttu-id="1f1a0-155">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-155">False</span></span>

<span data-ttu-id="1f1a0-156">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-156">False</span></span>

<span data-ttu-id="1f1a0-157">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-157">Does not appear</span></span>

<span data-ttu-id="1f1a0-158">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-158">No</span></span>

<span data-ttu-id="1f1a0-159">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-159">Yes</span></span>

<span data-ttu-id="1f1a0-160">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-160">Yes</span></span>

<span data-ttu-id="1f1a0-161">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-161">No</span></span> 

<span data-ttu-id="1f1a0-162">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-162">True</span></span>

<span data-ttu-id="1f1a0-163">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-163">True</span></span>

<span data-ttu-id="1f1a0-164">Normal, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-165">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-165">No</span></span>

<span data-ttu-id="1f1a0-166">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-166">Yes</span></span>

<span data-ttu-id="1f1a0-167">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-167">Yes</span></span>

<span data-ttu-id="1f1a0-168">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-168">No</span></span> 

<span data-ttu-id="1f1a0-169">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-169">True</span></span>

<span data-ttu-id="1f1a0-170">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-170">False</span></span>

<span data-ttu-id="1f1a0-171">Désactivé, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-172">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-172">No</span></span>

<span data-ttu-id="1f1a0-173">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-173">Yes</span></span>

<span data-ttu-id="1f1a0-174">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-174">Yes</span></span>

<span data-ttu-id="1f1a0-175">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-175">No</span></span> 

<span data-ttu-id="1f1a0-176">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-176">False</span></span>

<span data-ttu-id="1f1a0-177">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-177">True</span></span>

<span data-ttu-id="1f1a0-178">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-178">Does not appear</span></span>

<span data-ttu-id="1f1a0-179">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-179">No</span></span>

<span data-ttu-id="1f1a0-180">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-180">Yes</span></span>

<span data-ttu-id="1f1a0-181">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-181">Yes</span></span>

<span data-ttu-id="1f1a0-182">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-182">No</span></span> 

<span data-ttu-id="1f1a0-183">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-183">False</span></span>

<span data-ttu-id="1f1a0-184">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-184">False</span></span>

<span data-ttu-id="1f1a0-185">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-185">Does not appear</span></span>

<span data-ttu-id="1f1a0-186">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-186">No</span></span>

<span data-ttu-id="1f1a0-187">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-187">No</span></span> 

<span data-ttu-id="1f1a0-188">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-188">Yes</span></span>

<span data-ttu-id="1f1a0-189">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-189">Yes</span></span>

<span data-ttu-id="1f1a0-190">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-190">True</span></span>

<span data-ttu-id="1f1a0-191">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-191">True</span></span>

<span data-ttu-id="1f1a0-192">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-192">Does not appear</span></span>

<span data-ttu-id="1f1a0-193">Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="1f1a0-194">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-194">No</span></span> 

<span data-ttu-id="1f1a0-195">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-195">Yes</span></span>

<span data-ttu-id="1f1a0-196">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-196">Yes</span></span>

<span data-ttu-id="1f1a0-197">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-197">True</span></span>

<span data-ttu-id="1f1a0-198">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-198">False</span></span>

<span data-ttu-id="1f1a0-199">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-199">Does not appear</span></span>

<span data-ttu-id="1f1a0-200">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-200">No</span></span>

<span data-ttu-id="1f1a0-201">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-201">No</span></span> 

<span data-ttu-id="1f1a0-202">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-202">Yes</span></span>

<span data-ttu-id="1f1a0-203">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-203">Yes</span></span>

<span data-ttu-id="1f1a0-204">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-204">False</span></span>

<span data-ttu-id="1f1a0-205">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-205">True</span></span>

<span data-ttu-id="1f1a0-206">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-206">Does not appear</span></span>

<span data-ttu-id="1f1a0-207">Oui, à l’aide de [ **VoiceCaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="1f1a0-208">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-208">No</span></span> 

<span data-ttu-id="1f1a0-209">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-209">Yes</span></span>

<span data-ttu-id="1f1a0-210">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-210">Yes</span></span>

<span data-ttu-id="1f1a0-211">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-211">False</span></span>

<span data-ttu-id="1f1a0-212">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-212">False</span></span>

<span data-ttu-id="1f1a0-213">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-213">Does not appear</span></span>

<span data-ttu-id="1f1a0-214">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-214">No</span></span>

<span data-ttu-id="1f1a0-215">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-215">No</span></span> 

<span data-ttu-id="1f1a0-216">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-216">Yes</span></span>

<span data-ttu-id="1f1a0-217">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-217">No</span></span> 

<span data-ttu-id="1f1a0-218">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-218">True</span></span>

<span data-ttu-id="1f1a0-219">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-219">True</span></span>

<span data-ttu-id="1f1a0-220">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-220">Does not appear</span></span>

<span data-ttu-id="1f1a0-221">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-221">No</span></span>

<span data-ttu-id="1f1a0-222">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-222">No</span></span> 

<span data-ttu-id="1f1a0-223">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-223">Yes</span></span>

<span data-ttu-id="1f1a0-224">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-224">No</span></span> 

<span data-ttu-id="1f1a0-225">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-225">True</span></span>

<span data-ttu-id="1f1a0-226">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-226">False</span></span>

<span data-ttu-id="1f1a0-227">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-227">Does not appear</span></span>

<span data-ttu-id="1f1a0-228">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-228">No</span></span>

<span data-ttu-id="1f1a0-229">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-229">No</span></span> 

<span data-ttu-id="1f1a0-230">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-230">Yes</span></span>

<span data-ttu-id="1f1a0-231">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-231">No</span></span> 

<span data-ttu-id="1f1a0-232">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-232">False</span></span>

<span data-ttu-id="1f1a0-233">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-233">True</span></span>

<span data-ttu-id="1f1a0-234">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-234">Does not appear</span></span>

<span data-ttu-id="1f1a0-235">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-235">No</span></span>

<span data-ttu-id="1f1a0-236">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-236">No</span></span> 

<span data-ttu-id="1f1a0-237">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-237">Yes</span></span>

<span data-ttu-id="1f1a0-238">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-238">No</span></span> 

<span data-ttu-id="1f1a0-239">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-239">False</span></span>

<span data-ttu-id="1f1a0-240">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-240">False</span></span>

<span data-ttu-id="1f1a0-241">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-241">Does not appear</span></span>

<span data-ttu-id="1f1a0-242">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-242">No</span></span>

<span data-ttu-id="1f1a0-243">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-243">Yes</span></span>

<span data-ttu-id="1f1a0-244">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-244">No</span></span> 

<span data-ttu-id="1f1a0-245">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-245">Yes</span></span>

<span data-ttu-id="1f1a0-246">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-246">True</span></span>

<span data-ttu-id="1f1a0-247">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-247">True</span></span>

<span data-ttu-id="1f1a0-248">Normal, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-249">Oui, à l’aide de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-250">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-250">Yes</span></span>

<span data-ttu-id="1f1a0-251">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-251">No</span></span> 

<span data-ttu-id="1f1a0-252">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-252">Yes</span></span>

<span data-ttu-id="1f1a0-253">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-253">True</span></span>

<span data-ttu-id="1f1a0-254">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-254">False</span></span>

<span data-ttu-id="1f1a0-255">Désactivé, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-256">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-256">No</span></span>

<span data-ttu-id="1f1a0-257">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-257">Yes</span></span>

<span data-ttu-id="1f1a0-258">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-258">No</span></span> 

<span data-ttu-id="1f1a0-259">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-259">Yes</span></span>

<span data-ttu-id="1f1a0-260">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-260">False</span></span>

<span data-ttu-id="1f1a0-261">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-261">True</span></span>

<span data-ttu-id="1f1a0-262">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-262">Does not appear</span></span>

<span data-ttu-id="1f1a0-263">Oui, à l’aide de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-264">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-264">Yes</span></span>

<span data-ttu-id="1f1a0-265">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-265">No</span></span> 

<span data-ttu-id="1f1a0-266">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-266">Yes</span></span>

<span data-ttu-id="1f1a0-267">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-267">False</span></span>

<span data-ttu-id="1f1a0-268">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-268">False</span></span>

<span data-ttu-id="1f1a0-269">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-269">Does not appear</span></span>

<span data-ttu-id="1f1a0-270">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-270">No</span></span>

<span data-ttu-id="1f1a0-271">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-271">Yes</span></span>

<span data-ttu-id="1f1a0-272">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-272">No</span></span> 

<span data-ttu-id="1f1a0-273">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-273">No</span></span> 

<span data-ttu-id="1f1a0-274">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-274">True</span></span>

<span data-ttu-id="1f1a0-275">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-275">True</span></span>

<span data-ttu-id="1f1a0-276">Normal, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-277">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-277">No</span></span>

<span data-ttu-id="1f1a0-278">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-278">Yes</span></span>

<span data-ttu-id="1f1a0-279">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-279">No</span></span> 

<span data-ttu-id="1f1a0-280">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-280">No</span></span> 

<span data-ttu-id="1f1a0-281">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-281">True</span></span>

<span data-ttu-id="1f1a0-282">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-282">False</span></span>

<span data-ttu-id="1f1a0-283">Désactivé, utilisation de la [ **légende**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="1f1a0-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="1f1a0-284">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-284">No</span></span>

<span data-ttu-id="1f1a0-285">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-285">Yes</span></span>

<span data-ttu-id="1f1a0-286">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-286">No</span></span> 

<span data-ttu-id="1f1a0-287">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-287">No</span></span> 

<span data-ttu-id="1f1a0-288">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-288">False</span></span>

<span data-ttu-id="1f1a0-289">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-289">True</span></span>

<span data-ttu-id="1f1a0-290">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-290">Does not appear</span></span>

<span data-ttu-id="1f1a0-291">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-291">No</span></span>

<span data-ttu-id="1f1a0-292">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-292">Yes</span></span>

<span data-ttu-id="1f1a0-293">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-293">No</span></span> 

<span data-ttu-id="1f1a0-294">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-294">No</span></span> 

<span data-ttu-id="1f1a0-295">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-295">False</span></span>

<span data-ttu-id="1f1a0-296">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-296">False</span></span>

<span data-ttu-id="1f1a0-297">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-297">Does not appear</span></span>

<span data-ttu-id="1f1a0-298">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-298">No</span></span>

<span data-ttu-id="1f1a0-299">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-299">No</span></span> 

<span data-ttu-id="1f1a0-300">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-300">No</span></span> 

<span data-ttu-id="1f1a0-301">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-301">Yes</span></span>

<span data-ttu-id="1f1a0-302">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-302">True</span></span>

<span data-ttu-id="1f1a0-303">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-303">True</span></span>

<span data-ttu-id="1f1a0-304">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-304">Does not appear</span></span>

<span data-ttu-id="1f1a0-305">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-305">No</span></span> 

<span data-ttu-id="1f1a0-306">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-306">No</span></span> 

<span data-ttu-id="1f1a0-307">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-307">No</span></span> 

<span data-ttu-id="1f1a0-308">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-308">Yes</span></span>

<span data-ttu-id="1f1a0-309">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-309">True</span></span>

<span data-ttu-id="1f1a0-310">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-310">False</span></span>

<span data-ttu-id="1f1a0-311">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-311">Does not appear</span></span>

<span data-ttu-id="1f1a0-312">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-312">No</span></span>

<span data-ttu-id="1f1a0-313">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-313">No</span></span> 

<span data-ttu-id="1f1a0-314">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-314">No</span></span> 

<span data-ttu-id="1f1a0-315">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-315">Yes</span></span>

<span data-ttu-id="1f1a0-316">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-316">False</span></span>

<span data-ttu-id="1f1a0-317">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-317">True</span></span>

<span data-ttu-id="1f1a0-318">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-318">Does not appear</span></span>

<span data-ttu-id="1f1a0-319">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-319">No</span></span> 

<span data-ttu-id="1f1a0-320">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-320">No</span></span> 

<span data-ttu-id="1f1a0-321">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-321">No</span></span> 

<span data-ttu-id="1f1a0-322">Oui</span><span class="sxs-lookup"><span data-stu-id="1f1a0-322">Yes</span></span>

<span data-ttu-id="1f1a0-323">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-323">False</span></span>

<span data-ttu-id="1f1a0-324">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-324">False</span></span>

<span data-ttu-id="1f1a0-325">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-325">Does not appear</span></span>

<span data-ttu-id="1f1a0-326">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-326">No</span></span>

<span data-ttu-id="1f1a0-327">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-327">No</span></span> 

<span data-ttu-id="1f1a0-328">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-328">No</span></span> 

<span data-ttu-id="1f1a0-329">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-329">No</span></span> 

<span data-ttu-id="1f1a0-330">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-330">True</span></span>

<span data-ttu-id="1f1a0-331">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-331">True</span></span>

<span data-ttu-id="1f1a0-332">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-332">Does not appear</span></span>

<span data-ttu-id="1f1a0-333">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-333">No</span></span>

<span data-ttu-id="1f1a0-334">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-334">No</span></span> 

<span data-ttu-id="1f1a0-335">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-335">No</span></span> 

<span data-ttu-id="1f1a0-336">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-336">No</span></span> 

<span data-ttu-id="1f1a0-337">Vrai</span><span class="sxs-lookup"><span data-stu-id="1f1a0-337">True</span></span>

<span data-ttu-id="1f1a0-338">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-338">False</span></span>

<span data-ttu-id="1f1a0-339">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-339">Does not appear</span></span>

<span data-ttu-id="1f1a0-340">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-340">No</span></span>

<span data-ttu-id="1f1a0-341">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-341">No</span></span> 

<span data-ttu-id="1f1a0-342">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-342">No</span></span> 

<span data-ttu-id="1f1a0-343">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-343">No</span></span> 

<span data-ttu-id="1f1a0-344">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-344">False</span></span>

<span data-ttu-id="1f1a0-345">True</span><span class="sxs-lookup"><span data-stu-id="1f1a0-345">True</span></span>

<span data-ttu-id="1f1a0-346">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-346">Does not appear</span></span>

<span data-ttu-id="1f1a0-347">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-347">No</span></span>

<span data-ttu-id="1f1a0-348">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-348">No</span></span> 

<span data-ttu-id="1f1a0-349">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-349">No</span></span> 

<span data-ttu-id="1f1a0-350">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-350">No</span></span> 

<span data-ttu-id="1f1a0-351">Faux</span><span class="sxs-lookup"><span data-stu-id="1f1a0-351">False</span></span>

<span data-ttu-id="1f1a0-352">False</span><span class="sxs-lookup"><span data-stu-id="1f1a0-352">False</span></span>

<span data-ttu-id="1f1a0-353">N’apparaît pas</span><span class="sxs-lookup"><span data-stu-id="1f1a0-353">Does not appear</span></span>

<span data-ttu-id="1f1a0-354">Non</span><span class="sxs-lookup"><span data-stu-id="1f1a0-354">No</span></span>

 <span data-ttu-id="1f1a0-355">Si le paramètre de la propriété a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-355">If the property setting is null.</span></span> <span data-ttu-id="1f1a0-356">Dans certains langages de programmation, une chaîne vide ne peut pas être interprétée de la même façon qu’une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="1f1a0-357">La commande est toujours accessible en voix.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="1f1a0-358">Lorsque le serveur reçoit une entrée pour l’une de vos commandes, il envoie un événement de [**commande**](/windows/desktop/lwef/the-command-object) et transmet le nom de la **commande** en tant qu’attribut de l’objet [**UserInput**](/windows/desktop/lwef/iagentuserinput) .</span><span class="sxs-lookup"><span data-stu-id="1f1a0-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="1f1a0-359">Vous pouvez ensuite utiliser des instructions conditionnelles pour faire correspondre et traiter la **commande**.</span><span class="sxs-lookup"><span data-stu-id="1f1a0-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

