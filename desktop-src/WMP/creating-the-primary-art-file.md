---
title: Création du fichier art principal
description: Création du fichier art principal
ms.assetid: 50099050-2ce8-4cbf-82b7-3018f6579bd2
keywords:
- création d’apparences, de fichiers art primaires
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, images principales
- Apparences du lecteur Windows Media, images principales
- apparences, images principales
- images principales dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ceb92a5a87c1fc03ec7336a7ca5dd7814e4a1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104568893"
---
# <a name="creating-the-primary-art-file"></a><span data-ttu-id="0277a-111">Création du fichier art principal</span><span class="sxs-lookup"><span data-stu-id="0277a-111">Creating the Primary Art File</span></span>

<span data-ttu-id="0277a-112">Le fichier art principal contiendra l’illustration que l’utilisateur de votre Skin voit d’abord.</span><span class="sxs-lookup"><span data-stu-id="0277a-112">The primary art file will contain the art that the user of your skin first sees.</span></span> <span data-ttu-id="0277a-113">Dans ce cas, vous allez créer des images dans différentes couches de votre programme art.</span><span class="sxs-lookup"><span data-stu-id="0277a-113">In this case, you will be creating images in different layers of your art program.</span></span> <span data-ttu-id="0277a-114">La raison de l’utilisation des couches est que vous copierez ultérieurement des couches spécifiques pour créer des fichiers de mappage et des fichiers d’art alternatifs.</span><span class="sxs-lookup"><span data-stu-id="0277a-114">The reason for using layers is that you will copy specific layers later to create map files and alternate art files.</span></span>

<span data-ttu-id="0277a-115">Pour créer le fichier art principal, vous allez créer les couches suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="0277a-115">To create the primary art file, you will create the following layers in the following order:</span></span>

<span data-ttu-id="0277a-116">Couche d’arrière-plan de l’apparence</span><span class="sxs-lookup"><span data-stu-id="0277a-116">Skin background layer</span></span>

<span data-ttu-id="0277a-117">Il s’agit de la couleur qui sera transparente lorsque l’apparence sera affichée.</span><span class="sxs-lookup"><span data-stu-id="0277a-117">This is the color that will be transparent when the skin is displayed.</span></span> <span data-ttu-id="0277a-118">Créez d’abord une couche pour cette couche, mais choisissez la couleur finale de cette couche après avoir choisi une couleur pour la couche de conteneur d’apparences.</span><span class="sxs-lookup"><span data-stu-id="0277a-118">Create a layer for this first, but choose the final color of this layer after you chose a color for the skin container layer.</span></span> <span data-ttu-id="0277a-119">Cette couleur doit être semblable à, mais pas à la couche du conteneur d’apparences, pour masquer les effets d’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="0277a-119">This color should be similar to, but not the same as, the skin container layer, to hide any anti-aliasing effects.</span></span>

<span data-ttu-id="0277a-120">Couche de conteneur d’apparence</span><span class="sxs-lookup"><span data-stu-id="0277a-120">Skin container layer</span></span>

<span data-ttu-id="0277a-121">Il s’agit de l’image qui formera le contour de votre apparence et sera ce que l’utilisateur voit.</span><span class="sxs-lookup"><span data-stu-id="0277a-121">This is the image that will form the outline of your skin and will be what the user sees.</span></span> <span data-ttu-id="0277a-122">Il s’agit également du conteneur pour les deux boutons de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="0277a-122">It also will be the container for the two buttons in this example.</span></span> <span data-ttu-id="0277a-123">Imaginez votre apparence comme un conteneur pour les contrôles d’interface utilisateur, tels que les boutons, les curseurs, etc.</span><span class="sxs-lookup"><span data-stu-id="0277a-123">Think of your skin as a container for user interface controls such as buttons, sliders, and so on.</span></span> <span data-ttu-id="0277a-124">Dans cet exemple, le conteneur est une ellipse jaune.</span><span class="sxs-lookup"><span data-stu-id="0277a-124">In this example, the container is a yellow oval.</span></span>

<span data-ttu-id="0277a-125">Calques de bouton lire et fermer</span><span class="sxs-lookup"><span data-stu-id="0277a-125">Play and Close button layers</span></span>

<span data-ttu-id="0277a-126">Il s’agit des deux contrôles d’interface utilisateur que cet exemple utilise.</span><span class="sxs-lookup"><span data-stu-id="0277a-126">These are the two user interface controls that this example uses.</span></span> <span data-ttu-id="0277a-127">Vous allez les placer dans des couches distinctes afin de pouvoir les ajuster facilement ou les copier ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0277a-127">You will put them in separate layers so that you can easily adjust them or copy them later.</span></span>

<span data-ttu-id="0277a-128">Avant de créer vos couches, vous devez créer le fichier qui contiendra vos couches.</span><span class="sxs-lookup"><span data-stu-id="0277a-128">Before you create your layers, you must create the file that will hold your layers.</span></span> <span data-ttu-id="0277a-129">Démarrez Photoshop et créez un nouveau fichier de 100 pixels de haut et 200 pixels de large.</span><span class="sxs-lookup"><span data-stu-id="0277a-129">Start up Photoshop and create a new file that is 100 pixels high and 200 pixels wide.</span></span> <span data-ttu-id="0277a-130">Le fichier utilisé pour créer l’illustration de cet exemple est appelé tiny.psd et est inclus dans le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="0277a-130">The file used to create the art for this sample is called tiny.psd and is included with the SDK.</span></span>

<span data-ttu-id="0277a-131">Toutes les instructions sont fournies en termes de Photoshop, mais tout autre programme artistique peut être utilisé pour créer des apparences tant que vous pouvez les enregistrer dans l’un des formats de fichier pris en charge par le lecteur Windows Media (BMP, GIF, JPG et PNG).</span><span class="sxs-lookup"><span data-stu-id="0277a-131">All instructions are given in terms of Photoshop, but any other art program can be used to create skins as long as you can save to one of the file formats supported by the Windows Media Player (BMP, GIF, JPG, and PNG).</span></span> <span data-ttu-id="0277a-132">La création d’apparences est plus facile si vous utilisez un programme artistique avec des couches, comme Adobe Photoshop, Jasc Paint Shop Pro ou Jedor VISCOSITE.</span><span class="sxs-lookup"><span data-stu-id="0277a-132">You will find skin creation easier if you use an art program that has layers, such as Adobe Photoshop, Jasc Paint Shop Pro, or Jedor Viscosity.</span></span> <span data-ttu-id="0277a-133">Les couches sont extrêmement utiles, car les images doivent être alignées correctement pour le mappage d’images et l’affichage d’autres images.</span><span class="sxs-lookup"><span data-stu-id="0277a-133">Layers are extremely useful because images must be properly aligned for image mapping and display of alternative images.</span></span>

## <a name="skin-background-layer"></a><span data-ttu-id="0277a-134">Couche d’arrière-plan de l’apparence</span><span class="sxs-lookup"><span data-stu-id="0277a-134">Skin Background Layer</span></span>

<span data-ttu-id="0277a-135">Créez une nouvelle couche et nommez-la « Skin background ».</span><span class="sxs-lookup"><span data-stu-id="0277a-135">Create a new layer and name it "Skin background".</span></span> <span data-ttu-id="0277a-136">Celle-ci devient la couleur de transparence que vous allez définir dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="0277a-136">This will become the transparency color you will define in the skin definition file.</span></span> <span data-ttu-id="0277a-137">Attendez que la couleur du conteneur d’apparence soit choisie avant de remplir la couche d’arrière-plan de l’apparence avec une couleur spécifique.</span><span class="sxs-lookup"><span data-stu-id="0277a-137">Wait until the color for the skin container is chosen before filling the skin background layer with a specific color.</span></span>

## <a name="skin-container-layer"></a><span data-ttu-id="0277a-138">Couche de conteneur d’apparence</span><span class="sxs-lookup"><span data-stu-id="0277a-138">Skin Container Layer</span></span>

<span data-ttu-id="0277a-139">Créez ensuite une nouvelle couche et nommez-la « conteneur d’apparence ».</span><span class="sxs-lookup"><span data-stu-id="0277a-139">Next create a new layer and call it "Skin container".</span></span> <span data-ttu-id="0277a-140">Cela va définir les bords de votre apparence et sera le conteneur pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="0277a-140">This will define the edges of your skin and will be the container for the buttons.</span></span>

<span data-ttu-id="0277a-141">Choisissez une couleur de premier plan pour la forme, à l’aide des curseurs de couleur Web.</span><span class="sxs-lookup"><span data-stu-id="0277a-141">Choose a foreground color for the shape, using the Web color sliders.</span></span> <span data-ttu-id="0277a-142">Dans cet exemple, la couleur « \# DBDD11 » a été choisie.</span><span class="sxs-lookup"><span data-stu-id="0277a-142">In this example, the color "\#DBDD11" was chosen.</span></span>

<span data-ttu-id="0277a-143">Créez ensuite une forme ovale.</span><span class="sxs-lookup"><span data-stu-id="0277a-143">Next create an oval shape.</span></span> <span data-ttu-id="0277a-144">Le moyen le plus simple consiste à utiliser l’outil Eliptical Marquee et à créer une sélection ovale.</span><span class="sxs-lookup"><span data-stu-id="0277a-144">The easiest way is to use the Eliptical Marquee tool and create an oval selection.</span></span> <span data-ttu-id="0277a-145">Une fois que vous avez créé une sélection ovale qui correspond à la taille et à la forme souhaitées, remplissez la sélection avec la couleur de premier plan et annulez la sélection.</span><span class="sxs-lookup"><span data-stu-id="0277a-145">When you have created an oval selection that is the size and shape you want, fill the selection with the foreground color and cancel the selection.</span></span>

<span data-ttu-id="0277a-146">Enfin, pour que cet aspect soit un peu plus intéressant, appliquez l’effet de couche de biseau et le relief avec les valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="0277a-146">Finally, to make this look a bit more interesting, apply the layer effect of Bevel and Emboss with the default values.</span></span>

<span data-ttu-id="0277a-147">Votre couche de conteneur d’apparences doit ressembler à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="0277a-147">Your skin container layer should look like the following illustration.</span></span>

![couche de conteneur d’apparence](images/g01cont.png)

## <a name="background-skin-color"></a><span data-ttu-id="0277a-149">Couleur de l’apparence d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="0277a-149">Background Skin Color</span></span>

<span data-ttu-id="0277a-150">Maintenant que vous avez choisi une couleur de premier plan pour votre forme de conteneur d’apparences, vous pouvez choisir une couleur similaire pour votre couche d’arrière-plan d’apparence.</span><span class="sxs-lookup"><span data-stu-id="0277a-150">Now that you have chosen a foreground color for your skin container shape, you can choose a similar color for your skin background layer.</span></span> <span data-ttu-id="0277a-151">Vous ne souhaitez pas avoir la même couleur, ou votre conteneur d’apparences sera également transparent.</span><span class="sxs-lookup"><span data-stu-id="0277a-151">You do not want the exact same color, or your skin container will be transparent also.</span></span> <span data-ttu-id="0277a-152">En fait, veillez à ne pas utiliser cette couleur exacte dans votre peau, même dans les photographies, car partout où cette couleur apparaît, l’image de bureau s’affiche à la place.</span><span class="sxs-lookup"><span data-stu-id="0277a-152">In fact, be sure you do not use this exact color anywhere else in your skin, even in photographs, because wherever this color appears, the desktop image will appear instead.</span></span>

<span data-ttu-id="0277a-153">Vous souhaitez une couleur proche de la couleur du conteneur d’apparences pour éviter les effets d’anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="0277a-153">You want a color close to the skin container color to avoid anti-aliasing effects.</span></span> <span data-ttu-id="0277a-154">Par exemple, si vous avez un arrière-plan noir, certains éléments noirs peuvent s’afficher autour du bord de l’apparence.</span><span class="sxs-lookup"><span data-stu-id="0277a-154">For example, if you have a black background, some bits of black may show up around the edge of your skin.</span></span> <span data-ttu-id="0277a-155">En choisissant une couleur proche de la couleur du conteneur d’apparences, les pixels isolés qui s’affichent dans le processus d’anticrénelage ne seront pas remarqués.</span><span class="sxs-lookup"><span data-stu-id="0277a-155">By choosing a color close to the color of the skin container, any stray pixels that show up in the anti-aliasing process will be unnoticed.</span></span>

<span data-ttu-id="0277a-156">L’anticrénelage est le processus de lissage des bords des formes inclinées ou courbes.</span><span class="sxs-lookup"><span data-stu-id="0277a-156">Anti-aliasing is the process of smoothing the edges of slanted or curved shapes.</span></span> <span data-ttu-id="0277a-157">L’anticrénelage crée de nouvelles couleurs, pour les pixels situés le long des bords d’une forme, qui sont une fusion de la couleur de premier plan et la couleur d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="0277a-157">Anti-aliasing creates new colors, for pixels along the edges of a shape, that are a blend of the foreground color and the background color.</span></span> <span data-ttu-id="0277a-158">Certaines de ces couleurs entre elles peuvent provoquer l’absence de pixels lorsque la couleur d’arrière-plan est rendue transparente.</span><span class="sxs-lookup"><span data-stu-id="0277a-158">Some of these in-between colors can cause pixels to be missed when the background color is made transparent.</span></span>

<span data-ttu-id="0277a-159">Votre couche d’arrière-plan d’apparence doit ressembler à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="0277a-159">Your skin background layer should look like the following illustration.</span></span>

![couche d’apparence d’arrière-plan](images/g01backg.png)

## <a name="play-and-close-button-layers"></a><span data-ttu-id="0277a-161">Calques de bouton lire et fermer</span><span class="sxs-lookup"><span data-stu-id="0277a-161">Play and Close Button Layers</span></span>

<span data-ttu-id="0277a-162">Créez une nouvelle couche et nommez-la « bouton Fermer ».</span><span class="sxs-lookup"><span data-stu-id="0277a-162">Create a new layer and name it "Close button".</span></span> <span data-ttu-id="0277a-163">À l’aide de l’outil Eliptical palissade Selection, créez un cercle et positionnez-le sur le côté gauche de l’image globale.</span><span class="sxs-lookup"><span data-stu-id="0277a-163">Using the Eliptical Marquee selection tool again, create a circle and position it on the left side of the overall image.</span></span> <span data-ttu-id="0277a-164">Activez la visibilité du fichier conteneur d’apparence pour vous aider à placer la sélection.</span><span class="sxs-lookup"><span data-stu-id="0277a-164">Turn on the visibility of the skin container file to help place the selection.</span></span>

<span data-ttu-id="0277a-165">Lorsque vous êtes satisfait du positionnement, remplissez la sélection avec n’importe quelle couleur (à l’exception de la couleur du conteneur d’apparences ou de l’arrière-plan de l’apparence).</span><span class="sxs-lookup"><span data-stu-id="0277a-165">When you are satisfied with the placement, fill the selection with any color (except the color of the skin container or the skin background).</span></span> <span data-ttu-id="0277a-166">Dans cet exemple, une couleur violette a été choisie.</span><span class="sxs-lookup"><span data-stu-id="0277a-166">In this example, a purple color was chosen.</span></span> <span data-ttu-id="0277a-167">Vous n’avez pas besoin de vous souvenir du numéro de la couleur.</span><span class="sxs-lookup"><span data-stu-id="0277a-167">You do not need to remember the number of the color.</span></span> <span data-ttu-id="0277a-168">Puis, annulez la sélection et appliquez un autre effet de couche de biseau et de relief par défaut.</span><span class="sxs-lookup"><span data-stu-id="0277a-168">Then cancel the selection and apply another default Bevel and Emboss layer effect.</span></span> <span data-ttu-id="0277a-169">Si vous souhaitez appliquer des effets non-couche à votre bouton, faites une copie de l’original pour une utilisation ultérieure dans le mappage.</span><span class="sxs-lookup"><span data-stu-id="0277a-169">If you want to apply non-layer effects to your button, make a copy of the original for later use in mapping.</span></span>

<span data-ttu-id="0277a-170">Votre bouton Fermer doit ressembler à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="0277a-170">Your Close button should look like the following illustration.</span></span>

![bouton de fermeture](images/g01qbut.png)

<span data-ttu-id="0277a-172">Créez une nouvelle couche et nommez-la « bouton de lecture ».</span><span class="sxs-lookup"><span data-stu-id="0277a-172">Create a new layer and name it "Play button".</span></span> <span data-ttu-id="0277a-173">Utilisez les mêmes techniques que celles que vous avez effectuées pour le bouton Fermer, mais donnez-lui une couleur différente.</span><span class="sxs-lookup"><span data-stu-id="0277a-173">Use the same techniques you did for the Close button, but give it a different color.</span></span> <span data-ttu-id="0277a-174">Dans ce cas, une couleur de bouton rose a été choisie, mais toute couleur peut être utilisée tant qu’elle n’est pas de la même couleur que le conteneur d’habillage (car elle se mélange dans le conteneur) ou la couleur d’arrière-plan de l’apparence (car elle devient transparente).</span><span class="sxs-lookup"><span data-stu-id="0277a-174">In this case, a pink button color was chosen, but any color can be used as long as it is not the same color as the skin container (because it would blend into the container) or the skin background color (because it would become transparent).</span></span>

<span data-ttu-id="0277a-175">Votre bouton de lecture doit ressembler à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="0277a-175">Your Play button should look like the following illustration.</span></span>

![bouton de lecture](images/g01pbut.png)

## <a name="combine-layers-and-save"></a><span data-ttu-id="0277a-177">Combiner des couches et enregistrer</span><span class="sxs-lookup"><span data-stu-id="0277a-177">Combine Layers and Save</span></span>

<span data-ttu-id="0277a-178">Vous êtes maintenant prêt à créer le fichier art principal.</span><span class="sxs-lookup"><span data-stu-id="0277a-178">You are now ready to create the primary art file.</span></span> <span data-ttu-id="0277a-179">Masquer toutes les couches, puis afficher uniquement les couches suivantes, dans cet ordre (de haut en bas) :</span><span class="sxs-lookup"><span data-stu-id="0277a-179">Hide all layers and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="0277a-180">Bouton de lecture</span><span class="sxs-lookup"><span data-stu-id="0277a-180">Play button</span></span>

<span data-ttu-id="0277a-181">Bouton Fermer</span><span class="sxs-lookup"><span data-stu-id="0277a-181">Close button</span></span>

<span data-ttu-id="0277a-182">Conteneur d’apparences</span><span class="sxs-lookup"><span data-stu-id="0277a-182">Skin container</span></span>

<span data-ttu-id="0277a-183">Arrière-plan de la peau</span><span class="sxs-lookup"><span data-stu-id="0277a-183">Skin background</span></span>

<span data-ttu-id="0277a-184">Enregistrez dans un nouveau fichier à l’aide de la commande Enregistrer une copie du menu fichier.</span><span class="sxs-lookup"><span data-stu-id="0277a-184">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="0277a-185">Sélectionnez l’option BMP dans la partie enregistrer sous de la boîte de dialogue Enregistrer une copie et tapez un nom de fichier auquel vous allez vous référer ultérieurement dans votre fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="0277a-185">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="0277a-186">Dans l’idéal, vous devez enregistrer ce fichier dans le même répertoire que votre fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="0277a-186">Ideally you should save this in the same directory as your skin definition file.</span></span> <span data-ttu-id="0277a-187">Par exemple, vous pouvez appeler cette background.bmp.</span><span class="sxs-lookup"><span data-stu-id="0277a-187">For example, you could call this background.bmp.</span></span> <span data-ttu-id="0277a-188">Choisissez les paramètres par défaut et enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="0277a-188">Choose the default settings and save the file.</span></span>

<span data-ttu-id="0277a-189">Votre fichier art principal doit se présenter comme suit :</span><span class="sxs-lookup"><span data-stu-id="0277a-189">Your primary art file should look like this:</span></span>

![fichier art principal](images/g01prime.png)

<span data-ttu-id="0277a-191">Vous utiliserez ce nom de fichier comme valeur pour l’attribut **BackgroundImage** de l’élément **View** dans votre fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="0277a-191">You will use this file name as the value for the **backgroundImage** attribute of the **VIEW** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0277a-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0277a-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0277a-193">**Création de votre première apparence**</span><span class="sxs-lookup"><span data-stu-id="0277a-193">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




