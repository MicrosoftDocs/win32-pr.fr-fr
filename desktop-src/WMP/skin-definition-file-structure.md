---
title: Structure du fichier de définition d’apparence
description: Structure du fichier de définition d’apparence
ms.assetid: 6b9ea288-ec64-473b-b796-ab637517099a
keywords:
- Apparences du lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a64226fb918bcbf93c95ece52075e2c8e7ed13e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029477"
---
# <a name="skin-definition-file-structure"></a><span data-ttu-id="d463a-107">Structure du fichier de définition d’apparence</span><span class="sxs-lookup"><span data-stu-id="d463a-107">Skin Definition File Structure</span></span>

<span data-ttu-id="d463a-108">Le fichier de définition d’apparence doit suivre une structure spécifique.</span><span class="sxs-lookup"><span data-stu-id="d463a-108">The skin definition file must follow a specific structure.</span></span> <span data-ttu-id="d463a-109">Vous commencez avec un élément **Theme** , vous créez un ou plusieurs éléments **View** , puis vous définissez chaque élément **View** avec les éléments d’interface utilisateur appropriés pour le type de vue que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="d463a-109">You start with a **THEME** element, create one or more **VIEW** elements, and then define each **VIEW** element with the user interface elements appropriate for the type of view you want to use.</span></span>

## <a name="theme-elements"></a><span data-ttu-id="d463a-110">Éléments de thème</span><span class="sxs-lookup"><span data-stu-id="d463a-110">THEME Elements</span></span>

<span data-ttu-id="d463a-111">Au niveau supérieur, vous devez démarrer le fichier de définition d’apparence avec l’élément de **thème** et le fermer.</span><span class="sxs-lookup"><span data-stu-id="d463a-111">At the top level, you must start the skin definition file with the **THEME** element and close with it.</span></span>


```C++
<THEME>
    ...
</THEME>

```



<span data-ttu-id="d463a-112">L’élément **Theme** est l’élément racine de votre apparence.</span><span class="sxs-lookup"><span data-stu-id="d463a-112">The **THEME** element is the root element for your skin.</span></span> <span data-ttu-id="d463a-113">Un fichier de définition d’apparence ne peut contenir qu’un seul élément **Theme** , et il doit se trouver au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="d463a-113">There can be only one **THEME** element in a skin definition file, and it must be at the top level.</span></span> <span data-ttu-id="d463a-114">Les éléments de **thème** ont des attributs spécifiques et ambiants, mais la plupart du temps, vous n’aurez pas besoin de les utiliser.</span><span class="sxs-lookup"><span data-stu-id="d463a-114">**THEME** elements have specific and ambient attributes, though most of the time you will not need to use them.</span></span> <span data-ttu-id="d463a-115">Pour plus d’informations sur ces attributs, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d463a-115">For more information about these attributes, see the [Skin Programming Reference](skin-programming-reference.md).</span></span>

## <a name="view-elements"></a><span data-ttu-id="d463a-116">Éléments de vue</span><span class="sxs-lookup"><span data-stu-id="d463a-116">VIEW Elements</span></span>

<span data-ttu-id="d463a-117">Chaque **thème** doit avoir au moins un élément d' **affichage** .</span><span class="sxs-lookup"><span data-stu-id="d463a-117">Each **THEME** must have at least one **VIEW** element.</span></span> <span data-ttu-id="d463a-118">L’élément **View** régit l’image particulière que vous voyez à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d463a-118">The **VIEW** element governs the particular image you see on the screen.</span></span> <span data-ttu-id="d463a-119">Vous souhaiterez peut-être disposer de plusieurs vues, ce qui vous permet de basculer vers l’avant et l’arrière.</span><span class="sxs-lookup"><span data-stu-id="d463a-119">You may want to have more than one view, so you can switch back and forth.</span></span> <span data-ttu-id="d463a-120">Par exemple, vous souhaiterez peut-être avoir un grand affichage pour travailler avec des sélections, une vue moyenne pour regarder les visualisations et une petite vue qui s’adapte à un coin de l’écran.</span><span class="sxs-lookup"><span data-stu-id="d463a-120">For example, you might want to have a large view for working with playlists, a medium view for watching visualizations, and a tiny view that fits in a corner of the screen.</span></span>

<span data-ttu-id="d463a-121">Si vous créez plusieurs vues, vous devez vous assurer que chaque vue a une valeur d’attribut d' **ID** unique qui sera utilisée pour identifier la vue.</span><span class="sxs-lookup"><span data-stu-id="d463a-121">If you are creating multiple views, you will want to make sure that each view has a unique **ID** attribute value that will be used to identify the view.</span></span> <span data-ttu-id="d463a-122">Vous devez définir l’attribut **BackgroundImage** ou votre vue n’aura pas d’image de départ.</span><span class="sxs-lookup"><span data-stu-id="d463a-122">You must define the **backgroundImage** attribute or your view will have no starting image.</span></span> <span data-ttu-id="d463a-123">Si vous ne souhaitez pas afficher une image rectangulaire, vous souhaiterez probablement utiliser l’attribut **clippingColor** pour définir les zones de votre apparence qui ne seront pas affichées, et vous souhaiterez probablement définir l’attribut **TitleBar** de l’élément **View** .</span><span class="sxs-lookup"><span data-stu-id="d463a-123">If you do not want to display a rectangular image, you will probably want to use the **clippingColor** attribute to define the areas of your skin that will not display, and you will probably want to set the **titleBar** attribute of the **VIEW** element.</span></span>

<span data-ttu-id="d463a-124">Chaque élément de **vue** peut également avoir un ou plusieurs éléments de sous- **affichage** .</span><span class="sxs-lookup"><span data-stu-id="d463a-124">Each **VIEW** element can also have one or more **SUBVIEW** elements.</span></span> <span data-ttu-id="d463a-125">Un élément de sous- **affichage** est semblable à une **vue** et peut être utilisé pour des parties de l’apparence que vous souhaitez déplacer, masquer ou afficher.</span><span class="sxs-lookup"><span data-stu-id="d463a-125">A **SUBVIEW** element is similar to a **VIEW** and can be used for parts of your skin that you want to move around, hide, or show.</span></span> <span data-ttu-id="d463a-126">Par exemple, un élément de sous- **affichage** peut être utilisé pour créer une barre coulissante qui s’affiche en dehors de votre apparence pour afficher un égaliseur graphique.</span><span class="sxs-lookup"><span data-stu-id="d463a-126">For example, a **SUBVIEW** element might be used to create a sliding tray that pops out of your skin to display a graphic equalizer.</span></span> <span data-ttu-id="d463a-127">Les éléments de sous- **affichage** peuvent être alignés avec la **vue** et avoir d’autres relations spéciales avec la **vue**.</span><span class="sxs-lookup"><span data-stu-id="d463a-127">**SUBVIEW** elements can be aligned with the **VIEW** and have other special relationships to the **VIEW**.</span></span>

## <a name="initializing-windows-media-player"></a><span data-ttu-id="d463a-128">Initialisation du lecteur Windows Media</span><span class="sxs-lookup"><span data-stu-id="d463a-128">Initializing Windows Media Player</span></span>

<span data-ttu-id="d463a-129">Vous pouvez définir certaines propriétés initiales du lecteur Windows Media à l’aide des éléments **Player**, **Settings** et **Controls** .</span><span class="sxs-lookup"><span data-stu-id="d463a-129">You can set certain initial properties of Windows Media Player by using the **PLAYER**, **SETTINGS**, and **CONTROLS** elements.</span></span> <span data-ttu-id="d463a-130">Par exemple, vous pouvez définir le volume sur un niveau initial ou attribuer une valeur par défaut à un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="d463a-130">For example, you could set the volume to an initial level or give a default value for a file name.</span></span>

<span data-ttu-id="d463a-131">Le code suivant montre comment définir la valeur de l' **URL** dans une apparence :</span><span class="sxs-lookup"><span data-stu-id="d463a-131">The following code shows how to set the **URL** value in a skin:</span></span>


```C++
<PLAYER
  URL = "https://proseware.com/mellow.wma">
</PLAYER>

```



<span data-ttu-id="d463a-132">Si vous souhaitez affecter la valeur false à l’attribut **AutoStart** des **paramètres** , vous devez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="d463a-132">If you wanted to set the **autoStart** attribute of **SETTINGS** to False, you would use the following code:</span></span>


```C++
<PLAYER>
  <SETTINGS
    autoStart = "False">
  </SETTINGS>
</PLAYER>

```



<span data-ttu-id="d463a-133">Notez que l’élément **Settings** est imbriqué à l’intérieur de l’élément **Player** .</span><span class="sxs-lookup"><span data-stu-id="d463a-133">Note that the **SETTINGS** element is nested inside the **PLAYER** element.</span></span>

<span data-ttu-id="d463a-134">À l’aide de ces éléments, les attributs et les événements suivants peuvent être spécifiés au moment de la conception :</span><span class="sxs-lookup"><span data-stu-id="d463a-134">Using these elements, the following attributes and events can be specified at design time:</span></span>

<span data-ttu-id="d463a-135">**Attributs de l’élément PLAYER**</span><span class="sxs-lookup"><span data-stu-id="d463a-135">**PLAYER Element Attributes**</span></span>

-   <span data-ttu-id="d463a-136">**url**</span><span class="sxs-lookup"><span data-stu-id="d463a-136">**url**</span></span>
-   <span data-ttu-id="d463a-137">**des réponses**</span><span class="sxs-lookup"><span data-stu-id="d463a-137">**Buffering**</span></span>
-   <span data-ttu-id="d463a-138">**Currentitemchange**</span><span class="sxs-lookup"><span data-stu-id="d463a-138">**Currentitemchange**</span></span>
-   <span data-ttu-id="d463a-139">**Currentplaylistchange**</span><span class="sxs-lookup"><span data-stu-id="d463a-139">**Currentplaylistchange**</span></span>
-   <span data-ttu-id="d463a-140">**Error**</span><span class="sxs-lookup"><span data-stu-id="d463a-140">**Error**</span></span>
-   <span data-ttu-id="d463a-141">**Markerhit**</span><span class="sxs-lookup"><span data-stu-id="d463a-141">**Markerhit**</span></span>
-   <span data-ttu-id="d463a-142">**Mediachange**</span><span class="sxs-lookup"><span data-stu-id="d463a-142">**Mediachange**</span></span>
-   <span data-ttu-id="d463a-143">**Mediacollectionchange**</span><span class="sxs-lookup"><span data-stu-id="d463a-143">**Mediacollectionchange**</span></span>
-   <span data-ttu-id="d463a-144">**Modechange**</span><span class="sxs-lookup"><span data-stu-id="d463a-144">**Modechange**</span></span>
-   <span data-ttu-id="d463a-145">**Mpenstatechange**</span><span class="sxs-lookup"><span data-stu-id="d463a-145">**Mpenstatechange**</span></span>
-   <span data-ttu-id="d463a-146">**Mlaylistchange**</span><span class="sxs-lookup"><span data-stu-id="d463a-146">**Mlaylistchange**</span></span>
-   <span data-ttu-id="d463a-147">**Mlaystatechange**</span><span class="sxs-lookup"><span data-stu-id="d463a-147">**Mlaystatechange**</span></span>
-   <span data-ttu-id="d463a-148">**Mositionchange**</span><span class="sxs-lookup"><span data-stu-id="d463a-148">**Mositionchange**</span></span>
-   <span data-ttu-id="d463a-149">**Mcriptcommand**</span><span class="sxs-lookup"><span data-stu-id="d463a-149">**Mcriptcommand**</span></span>
-   <span data-ttu-id="d463a-150">**Mtatuschange**</span><span class="sxs-lookup"><span data-stu-id="d463a-150">**Mtatuschange**</span></span>

<span data-ttu-id="d463a-151">**Attributs des éléments de paramètres**</span><span class="sxs-lookup"><span data-stu-id="d463a-151">**SETTINGS Element Attributes**</span></span>

-   <span data-ttu-id="d463a-152">**Démarrage automatique**</span><span class="sxs-lookup"><span data-stu-id="d463a-152">**autoStart**</span></span>
-   <span data-ttu-id="d463a-153">**équilibrée**</span><span class="sxs-lookup"><span data-stu-id="d463a-153">**balance**</span></span>
-   <span data-ttu-id="d463a-154">**baseURL**</span><span class="sxs-lookup"><span data-stu-id="d463a-154">**baseURL**</span></span>
-   <span data-ttu-id="d463a-155">**defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="d463a-155">**defaultFrame**</span></span>
-   <span data-ttu-id="d463a-156">**enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="d463a-156">**enableErrorDialogs**</span></span>
-   <span data-ttu-id="d463a-157">**invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="d463a-157">**invokeURLs**</span></span>
-   <span data-ttu-id="d463a-158">**muette**</span><span class="sxs-lookup"><span data-stu-id="d463a-158">**mute**</span></span>
-   <span data-ttu-id="d463a-159">**playCount**</span><span class="sxs-lookup"><span data-stu-id="d463a-159">**playCount**</span></span>
-   <span data-ttu-id="d463a-160">**évaluation**</span><span class="sxs-lookup"><span data-stu-id="d463a-160">**rate**</span></span>
-   <span data-ttu-id="d463a-161">**volume**</span><span class="sxs-lookup"><span data-stu-id="d463a-161">**volume**</span></span>

## <a name="controls-element-attributes"></a><span data-ttu-id="d463a-162">Attributs d’élément de contrôle</span><span class="sxs-lookup"><span data-stu-id="d463a-162">CONTROLS Element Attributes</span></span>

-   <span data-ttu-id="d463a-163">**currentMarker**</span><span class="sxs-lookup"><span data-stu-id="d463a-163">**currentMarker**</span></span>
-   <span data-ttu-id="d463a-164">**currentPosition**</span><span class="sxs-lookup"><span data-stu-id="d463a-164">**currentPosition**</span></span>

## <a name="other-user-interface-elements"></a><span data-ttu-id="d463a-165">Autres éléments de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="d463a-165">Other User Interface Elements</span></span>

<span data-ttu-id="d463a-166">Une fois que vous avez défini votre **thème** et les éléments de **vue** , vous devez remplir votre **vue** avec des éléments d’interface utilisateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d463a-166">Once you have defined your **THEME** and **VIEW** elements, you must populate your **VIEW** with specific user interface elements.</span></span> <span data-ttu-id="d463a-167">Vous n’avez pas à utiliser tous les éléments disponibles dans une apparence, juste ceux dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="d463a-167">You do not have to use all the available elements in a skin, just the ones you need.</span></span>

<span data-ttu-id="d463a-168">Si un élément peut être vu par l’utilisateur, il est appelé contrôle.</span><span class="sxs-lookup"><span data-stu-id="d463a-168">If an element can be seen by the user, it is called a control.</span></span> <span data-ttu-id="d463a-169">Les contrôles suivants sont disponibles pour les apparences :</span><span class="sxs-lookup"><span data-stu-id="d463a-169">The following controls are available for skins:</span></span>

-   <span data-ttu-id="d463a-170">Boutons</span><span class="sxs-lookup"><span data-stu-id="d463a-170">Buttons</span></span>
-   <span data-ttu-id="d463a-171">Curseurs, curseurs personnalisés et barres de progression</span><span class="sxs-lookup"><span data-stu-id="d463a-171">Sliders, custom sliders, and progress bars</span></span>
-   <span data-ttu-id="d463a-172">Zones de texte</span><span class="sxs-lookup"><span data-stu-id="d463a-172">Text boxes</span></span>
-   <span data-ttu-id="d463a-173">Vidéos Windows</span><span class="sxs-lookup"><span data-stu-id="d463a-173">Video windows</span></span>
-   <span data-ttu-id="d463a-174">Fenêtres de visualisation</span><span class="sxs-lookup"><span data-stu-id="d463a-174">Visualization windows</span></span>
-   <span data-ttu-id="d463a-175">Fenêtres de sélection</span><span class="sxs-lookup"><span data-stu-id="d463a-175">Playlist windows</span></span>
-   <span data-ttu-id="d463a-176">Sous-affichage Windows</span><span class="sxs-lookup"><span data-stu-id="d463a-176">Subview windows</span></span>

<span data-ttu-id="d463a-177">En outre, plusieurs éléments peuvent être utilisés pour définir plus précisément les actions du lecteur Windows Media, mais ils requièrent des éléments visuels tels que des boutons ou des curseurs :</span><span class="sxs-lookup"><span data-stu-id="d463a-177">In addition, several elements can be used to further define Windows Media Player actions, but they require visual elements such as buttons or sliders:</span></span>

-   <span data-ttu-id="d463a-178">Paramètres vidéo</span><span class="sxs-lookup"><span data-stu-id="d463a-178">Video settings</span></span>
-   <span data-ttu-id="d463a-179">Paramètres de l’égaliseur</span><span class="sxs-lookup"><span data-stu-id="d463a-179">Equalizer Settings</span></span>
-   <span data-ttu-id="d463a-180">Paramètres de visualisation</span><span class="sxs-lookup"><span data-stu-id="d463a-180">Visualization settings</span></span>

## <a name="buttons"></a><span data-ttu-id="d463a-181">Boutons</span><span class="sxs-lookup"><span data-stu-id="d463a-181">Buttons</span></span>

<span data-ttu-id="d463a-182">Les boutons sont la partie la plus courante d’une apparence.</span><span class="sxs-lookup"><span data-stu-id="d463a-182">Buttons are the most popular part of a skin.</span></span> <span data-ttu-id="d463a-183">Vous pouvez utiliser des boutons pour déclencher des actions telles que lire, arrêter, quitter, réduire et basculer vers un affichage différent.</span><span class="sxs-lookup"><span data-stu-id="d463a-183">You can use buttons to trigger actions such as play, stop, quit, minimize, and switch to different view.</span></span> <span data-ttu-id="d463a-184">Le lecteur Windows Media fournit au créateur d’apparences deux types d’éléments Button : l’élément **Button** et l’élément **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="d463a-184">Windows Media Player provides the skin creator with two types of button elements: the **BUTTON** element and the **BUTTONGROUP** element.</span></span> <span data-ttu-id="d463a-185">En outre, il existe plusieurs types prédéfinis de boutons.</span><span class="sxs-lookup"><span data-stu-id="d463a-185">In addition, there are several predefined types of buttons.</span></span>

-   <span data-ttu-id="d463a-186">**Élément BUTTON.**</span><span class="sxs-lookup"><span data-stu-id="d463a-186">**BUTTON element.**</span></span> <span data-ttu-id="d463a-187">L’élément **Button** est utilisé pour les boutons individuels.</span><span class="sxs-lookup"><span data-stu-id="d463a-187">The **BUTTON** element is used for individual buttons.</span></span> <span data-ttu-id="d463a-188">Si vous utilisez l’élément **Button** , vous devez fournir une image pour chaque bouton et définir l’emplacement exact où vous souhaitez que le bouton apparaisse par rapport à l’image d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d463a-188">If you use the **BUTTON** element, you must supply an image for each button and define the exact location where you want the button to appear relative to the background image.</span></span> <span data-ttu-id="d463a-189">L’un des avantages de l’élément **Button** est que vous pouvez modifier l’image de bouton de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="d463a-189">One of the advantages of the **BUTTON** element is that you can change the button image dynamically.</span></span>
-   <span data-ttu-id="d463a-190">**Élément BUTTONGROUP.**</span><span class="sxs-lookup"><span data-stu-id="d463a-190">**BUTTONGROUP element.**</span></span> <span data-ttu-id="d463a-191">L’élément **BUTTONGROUP** est utilisé pour les groupes de boutons.</span><span class="sxs-lookup"><span data-stu-id="d463a-191">The **BUTTONGROUP** element is used for groups of buttons.</span></span> <span data-ttu-id="d463a-192">En fait, vous devez placer chaque élément **BUTTONGROUP** avec une paire de balises **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="d463a-192">In fact, you must enclose each **BUTTONGROUP** element with a pair of **BUTTONGROUP** tags.</span></span> <span data-ttu-id="d463a-193">L’utilisation de groupes de boutons est plus simple que l’utilisation de boutons individuels, car vous n’avez pas besoin de spécifier l’emplacement exact de chaque bouton.</span><span class="sxs-lookup"><span data-stu-id="d463a-193">Using button groups is easier than using individual buttons because you do not have to specify the exact location for each button.</span></span> <span data-ttu-id="d463a-194">Au lieu de cela, vous fournissez une carte d’images distincte qui définit les actions qui se produisent lorsque la souris pointe sur une zone de votre arrière-plan ou clique dessus.</span><span class="sxs-lookup"><span data-stu-id="d463a-194">Instead, you supply a separate image map that defines the actions that will take place when the mouse hovers over or clicks an area on your background.</span></span> <span data-ttu-id="d463a-195">L’utilisation de cartes d’images est simple, car vous pouvez prendre l’image que vous avez créée pour votre arrière-plan et la copier dans une couche de mappage dans votre programme d’édition de graphiques.</span><span class="sxs-lookup"><span data-stu-id="d463a-195">Using image maps is easy because you can take the art you created for your background and copy it to a mapping layer in your graphics editing program.</span></span> <span data-ttu-id="d463a-196">L’utilisation de votre programme d’édition graphique est plus rapide et plus précise que la tentative de définition exacte de l’emplacement d’un bouton individuel sur l’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d463a-196">Using your graphics editing program is faster and more precise than trying to define exactly where an individual button should be placed on your background.</span></span>
-   <span data-ttu-id="d463a-197">**Boutons prédéfinis.**</span><span class="sxs-lookup"><span data-stu-id="d463a-197">**Predefined buttons.**</span></span> <span data-ttu-id="d463a-198">Il existe plusieurs boutons prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="d463a-198">There are several predefined buttons.</span></span> <span data-ttu-id="d463a-199">Par exemple, vous pouvez utiliser un bouton PLAYELEMENT pour lire des fichiers multimédias numériques et un STOPELEMENT pour arrêter la lecture.</span><span class="sxs-lookup"><span data-stu-id="d463a-199">For example, you can use a PLAYELEMENT button to play digital media files, and a STOPELEMENT to stop playback.</span></span> <span data-ttu-id="d463a-200">Consultez élément [BUTTONGROUP](buttongroup-element.md) et [élément Button](button-element.md) dans la référence de programmation de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="d463a-200">See [BUTTONGROUP](buttongroup-element.md) Element and [BUTTON Element](button-element.md) in the Skin Programming Reference.</span></span> <span data-ttu-id="d463a-201">Le [IMAGEBUTTON](imagebutton.md) peut être utilisé pour afficher des images qui peuvent changer en réponse à des événements spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d463a-201">The [IMAGEBUTTON](imagebutton.md) can be used to display images that can change in response to specific events.</span></span>

## <a name="sliders"></a><span data-ttu-id="d463a-202">Curseurs</span><span class="sxs-lookup"><span data-stu-id="d463a-202">Sliders</span></span>

<span data-ttu-id="d463a-203">Les curseurs sont utiles pour utiliser des informations qui changent au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="d463a-203">Sliders are useful for working with information that changes over time.</span></span> <span data-ttu-id="d463a-204">Par exemple, vous pouvez utiliser un curseur pour indiquer la quantité de musique déjà lue pour un fichier multimédia particulier.</span><span class="sxs-lookup"><span data-stu-id="d463a-204">For example, you might use a slider to indicate the amount of music that has already played for a particular media file.</span></span> <span data-ttu-id="d463a-205">Les curseurs peuvent être horizontaux ou verticaux, linéaires ou circulaires, ou toute forme que vous pouvez considérer.</span><span class="sxs-lookup"><span data-stu-id="d463a-205">Sliders can be horizontal or vertical, linear or circular, or any shape you can think of.</span></span> <span data-ttu-id="d463a-206">Les curseurs sont fournis en trois catégories : les curseurs, les barres de progression et les curseurs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="d463a-206">Sliders come in three varieties: sliders, progress bars, and custom sliders.</span></span>

-   <span data-ttu-id="d463a-207">**Curseurs.**</span><span class="sxs-lookup"><span data-stu-id="d463a-207">**Sliders.**</span></span> <span data-ttu-id="d463a-208">Vous pouvez utiliser l’élément **Slider** pour les contrôles de volume ou pour permettre à l’utilisateur de passer à une autre partie du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="d463a-208">You can use the **SLIDER** element for volume controls or to allow the user to move to a different part of the media content.</span></span>
-   <span data-ttu-id="d463a-209">**Barres de progression.**</span><span class="sxs-lookup"><span data-stu-id="d463a-209">**Progress bars.**</span></span> <span data-ttu-id="d463a-210">Les barres de progression sont similaires aux curseurs.</span><span class="sxs-lookup"><span data-stu-id="d463a-210">Progress bars are similar to sliders.</span></span> <span data-ttu-id="d463a-211">Les barres de progression sont conçues pour afficher graphiquement le pourcentage d’un processus particulier qui est terminé, mais pas pour un processus avec lequel l’utilisateur souhaite interagir.</span><span class="sxs-lookup"><span data-stu-id="d463a-211">Progress bars are designed for graphically displaying the percentage of a particular process that has been completed, but not for a process that the user will want to interact with.</span></span> <span data-ttu-id="d463a-212">Par exemple, vous souhaiterez peut-être utiliser une barre de progression pour indiquer la progression de la mise en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d463a-212">For example, you might want to use a progress bar to indicate buffering progress.</span></span>
-   <span data-ttu-id="d463a-213">**Curseurs personnalisés.**</span><span class="sxs-lookup"><span data-stu-id="d463a-213">**Custom sliders.**</span></span> <span data-ttu-id="d463a-214">Des fonctionnalités de curseur personnalisées sont fournies pour vous permettre de créer des contrôles tels que des boutons ou d’effectuer des mécanismes de contrôle inhabituels.</span><span class="sxs-lookup"><span data-stu-id="d463a-214">Custom slider functionality is provided so you can create controls such as knobs, or make unusual control mechanisms.</span></span> <span data-ttu-id="d463a-215">Par exemple, si vous souhaitez créer un contrôle de volume qui habille votre apparence, vous pouvez le faire avec un curseur personnalisé.</span><span class="sxs-lookup"><span data-stu-id="d463a-215">For example, if you want to create a volume control that wraps around your skin, you can do it with a custom slider.</span></span> <span data-ttu-id="d463a-216">Pour configurer le curseur personnalisé, vous devez créer une image interactive qui contient des images en nuances de gris pour définir les emplacements des valeurs sur le curseur.</span><span class="sxs-lookup"><span data-stu-id="d463a-216">To set up the custom slider, you must create an image map that contains grayscale images to define the locations of the values on the slider.</span></span> <span data-ttu-id="d463a-217">Il est relativement facile d’effectuer cette opération avec un programme d’édition graphique qui prend en charge les couches.</span><span class="sxs-lookup"><span data-stu-id="d463a-217">This is relatively easy to do with a graphics editing program that supports layers.</span></span>

## <a name="text"></a><span data-ttu-id="d463a-218">Texte</span><span class="sxs-lookup"><span data-stu-id="d463a-218">Text</span></span>

<span data-ttu-id="d463a-219">Vous pouvez utiliser l’élément de **texte** pour afficher du texte sur votre apparence, par exemple des titres de chanson.</span><span class="sxs-lookup"><span data-stu-id="d463a-219">You can use the **TEXT** element to display text on your skin, such as song titles.</span></span>

## <a name="video"></a><span data-ttu-id="d463a-220">Vidéo</span><span class="sxs-lookup"><span data-stu-id="d463a-220">Video</span></span>

<span data-ttu-id="d463a-221">Vous pouvez afficher une vidéo dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="d463a-221">You can display video in your skin.</span></span> <span data-ttu-id="d463a-222">L’élément **Video** vous permet de définir la taille et la position de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="d463a-222">The **VIDEO** element allows you to set the size and position of the video window.</span></span>

<span data-ttu-id="d463a-223">Vous pouvez également autoriser l’utilisateur à modifier les paramètres vidéo avec l’élément **VIDEOSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="d463a-223">You can also allow the user to change the video settings with the **VIDEOSETTINGS** element.</span></span> <span data-ttu-id="d463a-224">Par exemple, vous pouvez créer des contrôles pour ajuster la luminosité de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="d463a-224">For example, you can create controls to adjust the brightness of the video.</span></span>

<span data-ttu-id="d463a-225">Si vous ne fournissez pas d’élément vidéo et que le contenu contient une vidéo, le lecteur Windows Media revient en mode complet et votre apparence ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="d463a-225">If you do not supply a video element and the content contains video, Windows Media Player will return to full mode and your skin will not be displayed.</span></span>

## <a name="equalizer-settings"></a><span data-ttu-id="d463a-226">Paramètres de l’égaliseur</span><span class="sxs-lookup"><span data-stu-id="d463a-226">Equalizer Settings</span></span>

<span data-ttu-id="d463a-227">Vous pouvez définir le filtrage pour des bandes de fréquence audio spécifiques à l’aide de l’élément **EQUALIZERSETTINGS** .</span><span class="sxs-lookup"><span data-stu-id="d463a-227">You can set the filtering for specific audio frequency bands by using the **EQUALIZERSETTINGS** element.</span></span> <span data-ttu-id="d463a-228">Vous pouvez amplifier les basses, ajuster les aigus et configurer vos sons pour qu’ils correspondent à vos oreilles ou à votre salon.</span><span class="sxs-lookup"><span data-stu-id="d463a-228">You can boost the bass, tweak the treble, and set up your sounds to match your ears or your living room.</span></span>

## <a name="visualizations"></a><span data-ttu-id="d463a-229">Visualisations</span><span class="sxs-lookup"><span data-stu-id="d463a-229">Visualizations</span></span>

<span data-ttu-id="d463a-230">Vous pouvez afficher des visualisations dans votre apparence.</span><span class="sxs-lookup"><span data-stu-id="d463a-230">You can display visualizations in your skin.</span></span> <span data-ttu-id="d463a-231">Les visualisations sont des effets visuels qui changent au fil du temps à mesure que le son est lu par le biais du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d463a-231">Visualizations are visual effects that change over time as audio is playing through Windows Media Player.</span></span> <span data-ttu-id="d463a-232">L’élément **Effects** détermine l’emplacement de lecture des visualisations, la taille de la fenêtre et les visualisations qui seront jouées.</span><span class="sxs-lookup"><span data-stu-id="d463a-232">The **EFFECTS** element determines where the visualizations will play, what size the window will be, and which visualizations will be played.</span></span>

## <a name="playlists"></a><span data-ttu-id="d463a-233">Sélections</span><span class="sxs-lookup"><span data-stu-id="d463a-233">Playlists</span></span>

<span data-ttu-id="d463a-234">Vous pouvez utiliser l’élément **playlist** pour permettre à l’utilisateur de sélectionner un élément dans une sélection spécifique.</span><span class="sxs-lookup"><span data-stu-id="d463a-234">You can use the **PLAYLIST** element to let the user select an item from a specific playlist.</span></span>

## <a name="subviews"></a><span data-ttu-id="d463a-235">Sous-affichages</span><span class="sxs-lookup"><span data-stu-id="d463a-235">Subviews</span></span>

<span data-ttu-id="d463a-236">Vous pouvez utiliser l’élément de sous- **affichage** pour afficher des jeux secondaires de contrôles d’interface, tels qu’une sélection ou des contrôles vidéo.</span><span class="sxs-lookup"><span data-stu-id="d463a-236">You can use the **SUBVIEW** element to display secondary sets of interface controls, such as a playlist or video controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d463a-237">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d463a-237">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d463a-238">**Fichiers d’apparence**</span><span class="sxs-lookup"><span data-stu-id="d463a-238">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




