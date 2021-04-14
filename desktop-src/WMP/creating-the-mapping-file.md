---
title: Création du fichier de mappage
description: Création du fichier de mappage
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- création d’apparences, mappage de fichiers
- Apparences du lecteur Windows Media, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, mappage d’images
- Apparences du lecteur Windows Media, mappage d’images
- apparences, mappage d’images
- mappage d’images dans des apparences
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379620"
---
# <a name="creating-the-mapping-file"></a><span data-ttu-id="85ffa-111">Création du fichier de mappage</span><span class="sxs-lookup"><span data-stu-id="85ffa-111">Creating the Mapping File</span></span>

<span data-ttu-id="85ffa-112">Une fois que vous avez créé les éléments de votre fichier art principal, il est relativement facile de créer un fichier de mappage.</span><span class="sxs-lookup"><span data-stu-id="85ffa-112">Once you have created the pieces of your primary art file, it is relatively easy to create a mapping file.</span></span> <span data-ttu-id="85ffa-113">Vous allez créer le nouveau fichier de mappage en combinant l’image des deux couches de bouton que vous avez déjà créées.</span><span class="sxs-lookup"><span data-stu-id="85ffa-113">You will create the new mapping file by combining the art from the two button layers you already created.</span></span>

1.  <span data-ttu-id="85ffa-114">Vous devrez prendre les deux boutons que vous avez créés pour le fichier art principal et les copier dans une nouvelle couche.</span><span class="sxs-lookup"><span data-stu-id="85ffa-114">You will need to take the two buttons you created for the primary art file and copy them to a new layer.</span></span> <span data-ttu-id="85ffa-115">Procédez comme suit : copiez la couche du bouton Fermer, supprimez tous les effets de couche, puis renommez-la « fermer le mappage ».</span><span class="sxs-lookup"><span data-stu-id="85ffa-115">Use the following steps: Copy the Close button layer, remove any Layer effects, and rename it "Close map".</span></span> <span data-ttu-id="85ffa-116">L’illustration doit paraître plate, sans biseau.</span><span class="sxs-lookup"><span data-stu-id="85ffa-116">The art should look flat, with no bevels.</span></span>
2.  <span data-ttu-id="85ffa-117">Utilisez le sélecteur de couleurs pour créer une couleur de premier plan du rouge pur.</span><span class="sxs-lookup"><span data-stu-id="85ffa-117">Use the Color Picker to create a foreground color of pure red.</span></span> <span data-ttu-id="85ffa-118">Assurez-vous que la valeur du numéro de couleur est « \# FF0000 ».</span><span class="sxs-lookup"><span data-stu-id="85ffa-118">Be sure the color number value is "\#FF0000".</span></span> <span data-ttu-id="85ffa-119">Utilisez ensuite l’outil Pot de peinture pour remplir l’intérieur du cercle de la couche de fermeture de la carte.</span><span class="sxs-lookup"><span data-stu-id="85ffa-119">Then use the Paint Bucket tool to fill the inside of the circle of the Close map layer.</span></span>
3.  <span data-ttu-id="85ffa-120">Copiez la couche du bouton de lecture, supprimez tous les effets de couche, puis renommez-la « Play map ».</span><span class="sxs-lookup"><span data-stu-id="85ffa-120">Copy the Play button layer, remove any Layer effects, and rename it "Play map".</span></span> <span data-ttu-id="85ffa-121">Là encore, l’art doit paraître plat.</span><span class="sxs-lookup"><span data-stu-id="85ffa-121">Again, the art should look flat.</span></span> <span data-ttu-id="85ffa-122">Vous ne souhaitez pas d’effets dans la couche de mappage, car vous définissez simplement des régions de la bitmap que le lecteur Windows Media utilisera pour déterminer où la souris effectue une action et ce que vous souhaitez en faire.</span><span class="sxs-lookup"><span data-stu-id="85ffa-122">You do not want any effects in the mapping layer because you are just defining regions of the bitmap that Windows Media Player will use to determine where the mouse performs an action and what you want to do with it.</span></span>
4.  <span data-ttu-id="85ffa-123">Utilisez le sélecteur de couleurs pour créer une couleur de premier plan du vert pur.</span><span class="sxs-lookup"><span data-stu-id="85ffa-123">Use the Color Picker to create a foreground color of pure green.</span></span> <span data-ttu-id="85ffa-124">Assurez-vous que la valeur du numéro de couleur est « \# 00FF00 ».</span><span class="sxs-lookup"><span data-stu-id="85ffa-124">Be sure the color number value is "\#00FF00".</span></span> <span data-ttu-id="85ffa-125">Utilisez ensuite l’outil Pot de peinture pour remplir l’intérieur du cercle de la couche de lecture.</span><span class="sxs-lookup"><span data-stu-id="85ffa-125">Then use the Paint Bucket tool to fill the inside of the circle of the Play map layer.</span></span>

<span data-ttu-id="85ffa-126">Vous êtes maintenant prêt à créer le fichier art de mappage.</span><span class="sxs-lookup"><span data-stu-id="85ffa-126">You are now ready to create the mapping art file.</span></span> <span data-ttu-id="85ffa-127">Masquer toutes les couches, puis afficher uniquement les couches suivantes, dans cet ordre (de haut en bas) :</span><span class="sxs-lookup"><span data-stu-id="85ffa-127">Hide all layers, and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="85ffa-128">Lire le mappage</span><span class="sxs-lookup"><span data-stu-id="85ffa-128">Play map</span></span>

<span data-ttu-id="85ffa-129">Fermer le mappage</span><span class="sxs-lookup"><span data-stu-id="85ffa-129">Close map</span></span>

<span data-ttu-id="85ffa-130">Enregistrez dans un nouveau fichier à l’aide de la commande Enregistrer une copie du menu fichier.</span><span class="sxs-lookup"><span data-stu-id="85ffa-130">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="85ffa-131">Sélectionnez l’option BMP dans la partie enregistrer sous de la boîte de dialogue Enregistrer une copie et tapez un nom de fichier auquel vous allez vous référer ultérieurement dans votre fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="85ffa-131">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="85ffa-132">Dans l’idéal, il doit se trouver dans le même répertoire que votre fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="85ffa-132">Ideally it should be in the same directory as your skin definition file.</span></span> <span data-ttu-id="85ffa-133">Par exemple, vous pouvez appeler ce fichier map.bmp.</span><span class="sxs-lookup"><span data-stu-id="85ffa-133">For example, you could call this file map.bmp.</span></span> <span data-ttu-id="85ffa-134">Choisissez les paramètres par défaut et enregistrez le fichier.</span><span class="sxs-lookup"><span data-stu-id="85ffa-134">Choose the default settings and save the file.</span></span>

<span data-ttu-id="85ffa-135">Votre fichier de mappage doit ressembler à l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="85ffa-135">Your mapping file should look like the following illustration.</span></span>

![Fichier de mappage](images/g01map.png)

<span data-ttu-id="85ffa-137">Comme vous pouvez le deviner, la zone verte est utilisée pour déterminer le moment où le lecteur Windows Media démarre et la zone rouge pour indiquer qu’il doit s’arrêter.</span><span class="sxs-lookup"><span data-stu-id="85ffa-137">As you might guess, the green area will be used to determine when to make Windows Media Player start and the red area is for telling it to stop.</span></span> <span data-ttu-id="85ffa-138">Les deux couleurs peuvent être utilisées, à condition que vous utilisiez les numéros de couleur lorsque vous configurez le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="85ffa-138">Any two colors can be used, as long as you use the color numbers when you set up the skin definition file.</span></span> <span data-ttu-id="85ffa-139">Assurez-vous que les couleurs de la carte sont des couleurs pures pour la région que vous souhaitez utiliser et que vous avez des bords distincts.</span><span class="sxs-lookup"><span data-stu-id="85ffa-139">Be sure the colors in the map are pure colors for the region you want to use and have distinct edges.</span></span> <span data-ttu-id="85ffa-140">Une couleur pure est une couleur où chaque pixel d’une zone a la même valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="85ffa-140">A pure color would be one where every single pixel in the area has the same color value.</span></span> <span data-ttu-id="85ffa-141">L’utilisation d’un effet peut atténuer ou déformer le bord, ce qui modifie légèrement les couleurs de certains pixels.</span><span class="sxs-lookup"><span data-stu-id="85ffa-141">Using an effect may blur or distort the edge, thereby slightly modifying the colors of some of the pixels.</span></span> <span data-ttu-id="85ffa-142">Le fichier de mappage n’est visible que par la souris, pas par un homme, donc ne vous ne devez pas le décorer, et supprimez les effets de couche que vous avez pu effectuer à partir d’autres couches.</span><span class="sxs-lookup"><span data-stu-id="85ffa-142">The mapping file is only seen by the mouse, not a human, so do not bother decorating it, and remove any layer effects you may have carried over from other layers.</span></span>

<span data-ttu-id="85ffa-143">Lorsque vous enregistrez votre fichier, le nom de fichier que vous choisissez sera ultérieurement utilisé comme valeur de l’attribut **mappingImage** de l’élément **BUTTONGROUP** dans votre fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="85ffa-143">When you save your file, the file name you choose will later be used as the value for the **mappingImage** attribute of the **BUTTONGROUP** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85ffa-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85ffa-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85ffa-145">**Création de votre première apparence**</span><span class="sxs-lookup"><span data-stu-id="85ffa-145">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




