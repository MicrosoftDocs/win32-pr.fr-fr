---
title: Ajout de Play BUTTONELEMENT
description: Ajout de Play BUTTONELEMENT
ms.assetid: 895850a7-7538-4581-8348-41cbb3bc9717
keywords:
- créer des apparences, BUTTONELEMENT, élément
- Apparences du lecteur Windows Media, BUTTONELEMENT, élément
- Skins, BUTTONELEMENT, élément
- fichiers de définition d’apparence, élément BUTTONELEMENT
- Élément BUTTONELEMENT
- éléments, BUTTONELEMENT
- création d’apparences, boutons de lecture
- Apparences du lecteur Windows Media, boutons de lecture
- apparences, boutons de lecture
- fichiers de définition d’apparence, boutons de lecture
- Boutons de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92b5416adf2e323043eb563ec08e1e4d2525733
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507247"
---
# <a name="adding-the-play-buttonelement"></a><span data-ttu-id="b4d7f-114">Ajout de Play BUTTONELEMENT</span><span class="sxs-lookup"><span data-stu-id="b4d7f-114">Adding the Play BUTTONELEMENT</span></span>

<span data-ttu-id="b4d7f-115">Enfin, vous pouvez ajouter les éléments **BUTTONELEMENT** qui connectent les boutons visuels à l’écran aux actions du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-115">Finally, you can add the **BUTTONELEMENT** elements that connect the visual buttons on the screen to Windows Media Player actions.</span></span> <span data-ttu-id="b4d7f-116">C’est le cœur de votre apparence et vous pouvez le considérer comme un câblage de la surface de l’apparence à la machine interne du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-116">This is the core of your skin and you can think of it as wiring the surface of the skin to the inner machinery of Windows Media Player.</span></span>

<span data-ttu-id="b4d7f-117">**BUTTONELEMENT** s sont contenus dans un **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-117">**BUTTONELEMENT** s are contained within a **BUTTONGROUP**.</span></span> <span data-ttu-id="b4d7f-118">Vous devez toujours avoir au moins un **BUTTONELEMENT** à l’intérieur de chaque **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-118">You must always have at least one **BUTTONELEMENT** inside each **BUTTONGROUP**.</span></span>

<span data-ttu-id="b4d7f-119">Placez le code de lecture de la **BUTTONELEMENT** après le crochet pointu fermant de **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-119">Put the Play **BUTTONELEMENT** code after the closing angle bracket of **BUTTONGROUP**.</span></span>


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick = "JScript: player.URL='https://proseware.com/laure.wma';" />

```



<span data-ttu-id="b4d7f-120">Les attributs suivants sont utilisés pour définir **BUTTONELEMENT** pour le bouton de lecture :</span><span class="sxs-lookup"><span data-stu-id="b4d7f-120">The following attributes are used to define the **BUTTONELEMENT** for the Play button:</span></span>

<span data-ttu-id="b4d7f-121">**mappingColor**</span><span class="sxs-lookup"><span data-stu-id="b4d7f-121">**mappingColor**</span></span>

<span data-ttu-id="b4d7f-122">Il s’agit de la valeur de couleur d’une région dans le fichier art de mappage que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-122">This is the color value of a region in the mapping art file you created before.</span></span> <span data-ttu-id="b4d7f-123">Dans ce cas, il s’agit de la couleur verte unie.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-123">In this case it is the solid green color.</span></span> <span data-ttu-id="b4d7f-124">Cet attribut est obligatoire pour tout **BUTTONELEMENT**.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-124">This attribute is required for any **BUTTONELEMENT**.</span></span> <span data-ttu-id="b4d7f-125">En définissant cette couleur, vous indiquez au lecteur Windows Media d’associer cette zone de couleur au code XML de ce bouton.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-125">By defining this color, you are telling Windows Media Player to associate this color area with the XML code of this button.</span></span>

<span data-ttu-id="b4d7f-126">**Info-bulle**</span><span class="sxs-lookup"><span data-stu-id="b4d7f-126">**upToolTip**</span></span>

<span data-ttu-id="b4d7f-127">Cela définit le texte qui s’affichera si l’utilisateur pointe la souris sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-127">This defines the text that will be displayed if the user hovers the mouse over the button.</span></span> <span data-ttu-id="b4d7f-128">Ne confondez pas cela avec l’image de survol qui sera affichée.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-128">Do not confuse this with the hover art that will be displayed.</span></span> <span data-ttu-id="b4d7f-129">Une info-bulle est une petite légende qui prend un moment pour apparaître.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-129">A ToolTip is a small balloon caption that takes a moment to appear.</span></span> <span data-ttu-id="b4d7f-130">Toutefois, l’image de la pointe de survol apparaît instantanément dans la couleur et la forme de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-130">The hover art image, however, will appear instantly in whatever color and shape you choose.</span></span>

<span data-ttu-id="b4d7f-131">**onClick**</span><span class="sxs-lookup"><span data-stu-id="b4d7f-131">**onClick**</span></span>

<span data-ttu-id="b4d7f-132">Cela définit l’événement qui se produit lorsque la souris clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-132">This defines the event that occurs when the mouse clicks on the button.</span></span> <span data-ttu-id="b4d7f-133">La valeur de cet attribut d’événement est appelée gestionnaire d’événements et sera soit une ligne de code Microsoft JScript, soit une fonction JScript dans un fichier texte externe qui est chargée par l’attribut **loadScript** d’une **vue**.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-133">The value of this event attribute is called an event handler and will be either a line of Microsoft JScript code, or a JScript function in an external text file that is loaded by the **loadScript** attribute of a **VIEW**.</span></span> <span data-ttu-id="b4d7f-134">Dans ce cas, le code JScript appelle la méthode d' **URL** du lecteur Windows Media, qui charge et démarre la lecture d’un fichier nommé « Laure. WMA ».</span><span class="sxs-lookup"><span data-stu-id="b4d7f-134">In this case, the JScript code calls the **URL** method of Windows Media Player, which loads and starts playing a file named "laure.wma".</span></span> <span data-ttu-id="b4d7f-135">Notez que la ligne se termine par un point-virgule à l’intérieur des guillemets, ce qui est une bonne pratique de codage JScript.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-135">Note that the line ends with a semicolon inside the quotes, which is good JScript coding practice.</span></span> <span data-ttu-id="b4d7f-136">Notez également l’utilisation de guillemets simples à l’intérieur des guillemets doubles pour définir le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-136">Note also the use of single quotes inside the double quotes to set off the file name.</span></span> <span data-ttu-id="b4d7f-137">Pour plus d’informations sur JScript, consultez [utilisation de JScript](using-jscript.md) dans la section à propos des apparences de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="b4d7f-137">For more information about JScript, see [Using JScript](using-jscript.md) in the About Skins section of this SDK.</span></span>

<span data-ttu-id="b4d7f-138">Notez qu’il n’y a pas de balise **BUTTONELEMENT** de fin.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-138">Notice that there is no ending **BUTTONELEMENT** tag.</span></span> <span data-ttu-id="b4d7f-139">Si un élément ne délimite pas un autre élément, vous pouvez le fermer à l’aide de la barre oblique juste avant le Chevron fermant.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-139">If an element does not enclose another element, you can close it off with the forward slash just before the closing angle bracket.</span></span> <span data-ttu-id="b4d7f-140">Cela indique au XML que vous avez terminé avec cet élément.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-140">This tells XML that you are finished with that element.</span></span> <span data-ttu-id="b4d7f-141">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="b4d7f-141">For example,</span></span>


```C++
<BUTTONELEMENT></BUTTONELEMENT>
```



<span data-ttu-id="b4d7f-142">et</span><span class="sxs-lookup"><span data-stu-id="b4d7f-142">and</span></span>


```C++
<BUTTONELEMENT/>
```



<span data-ttu-id="b4d7f-143">transmettent les mêmes informations en XML.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-143">convey the same information in XML.</span></span>

<span data-ttu-id="b4d7f-144">La puissance des habillages provient de l’utilisation de gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-144">The power of skins comes from using event handlers.</span></span> <span data-ttu-id="b4d7f-145">Si l’utilisateur effectue une opération avec une souris, vous pouvez gérer cet événement avec JScript.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-145">If the user does something with a mouse, you can handle that event with JScript.</span></span> <span data-ttu-id="b4d7f-146">Votre code peut être une ligne unique qui fait une action simple pour le lecteur Windows Media, ou bien une application complète écrite en JScript.</span><span class="sxs-lookup"><span data-stu-id="b4d7f-146">Your code can be a single line that makes Windows Media Player do something simple like play, or it can be a complete application written in JScript.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4d7f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4d7f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4d7f-148">**Création du fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="b4d7f-148">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




