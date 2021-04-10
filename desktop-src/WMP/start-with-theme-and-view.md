---
title: Démarrer avec un thème et une vue
description: Démarrer avec un thème et une vue
ms.assetid: 1ac92f3a-463a-4343-a269-5230c644b57f
keywords:
- créer des apparences, élément THEMe
- Apparences du lecteur Windows Media, élément de thème
- apparences, élément THEMe
- fichiers de définition d’apparence, élément THEMe
- Élément THEMe
- créer des apparences, élément d’affichage
- Apparences du lecteur Windows Media, élément d’affichage
- Skins, élément VIEW
- fichiers de définition d’apparence, élément de vue
- Élément VIEW
- éléments, vue
- éléments, thème
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499444ee2093e743f58174797794a50fbf74555a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840710"
---
# <a name="start-with-theme-and-view"></a><span data-ttu-id="d59c0-115">Démarrer avec un thème et une vue</span><span class="sxs-lookup"><span data-stu-id="d59c0-115">Start with THEME and VIEW</span></span>

<span data-ttu-id="d59c0-116">Chaque apparence doit avoir exactement un élément de **thème** et au moins un élément d' **affichage** .</span><span class="sxs-lookup"><span data-stu-id="d59c0-116">Every skin must have exactly one **THEME** element and at least one **VIEW** element.</span></span>

<span data-ttu-id="d59c0-117">À l’aide de votre éditeur de texte, créez le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="d59c0-117">Using your text editor, create the following text:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "False">


    </VIEW>
</THEME>

```



<span data-ttu-id="d59c0-118">Laissez des lignes vides avant la balise de **vue** de fermeture, car vous ajouterez plus de code ici ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d59c0-118">Leave some blank lines before the closing **VIEW** tag because you'll be adding more code here later.</span></span>

<span data-ttu-id="d59c0-119">Enregistrez votre fichier avec le nom de fichier de votre choix, mais assurez-vous que l’extension est. WMS.</span><span class="sxs-lookup"><span data-stu-id="d59c0-119">Save your file with any file name you wish, but be sure that the extension is .wms.</span></span> <span data-ttu-id="d59c0-120">Par exemple, un nom de fichier classique peut être skinone. WMS.</span><span class="sxs-lookup"><span data-stu-id="d59c0-120">For example, a typical file name might be skinone.wms.</span></span>

<span data-ttu-id="d59c0-121">Chaque apparence doit commencer par <THEME> et se terminer par </THEME>.</span><span class="sxs-lookup"><span data-stu-id="d59c0-121">Every skin must start with <THEME> and end with </THEME>.</span></span> <span data-ttu-id="d59c0-122">Vous ne pouvez avoir qu’un seul élément **Theme** dans votre apparence, mais vous devez en avoir un.</span><span class="sxs-lookup"><span data-stu-id="d59c0-122">You can only have one **THEME** element in your skin, but you must have one.</span></span>

<span data-ttu-id="d59c0-123">Vous devez également avoir au moins un élément **View** .</span><span class="sxs-lookup"><span data-stu-id="d59c0-123">You must also have at least one **VIEW** element.</span></span> <span data-ttu-id="d59c0-124">Vous pouvez avoir plus d’une **vue**, mais cet exemple n’en a qu’une.</span><span class="sxs-lookup"><span data-stu-id="d59c0-124">You can have more than one **VIEW**, but this example only has one.</span></span> <span data-ttu-id="d59c0-125">Vous devez avoir une ouverture <VIEW> et une fermeture <VIEW>. Notez que la </VIEW> balise d’ouverture ne ferme pas immédiatement la balise, mais qu’elle comprend plusieurs attributs avant le Chevron fermant (>).</span><span class="sxs-lookup"><span data-stu-id="d59c0-125">You must have an opening <VIEW> and a closing <VIEW>. Notice that the opening </VIEW> tag does not close the tag right away, but includes several attributes before the closing angle bracket (>).</span></span> <span data-ttu-id="d59c0-126">Les attributs suivants sont utilisés dans l’élément **Theme** dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="d59c0-126">The following attributes are used in the **THEME** element in this example:</span></span>

<span data-ttu-id="d59c0-127">**clippingColor**</span><span class="sxs-lookup"><span data-stu-id="d59c0-127">**clippingColor**</span></span>

<span data-ttu-id="d59c0-128">Vous n’aurez pas toujours besoin de l’attribut **clippingColor** si les bords de votre apparence sont rectangulaires.</span><span class="sxs-lookup"><span data-stu-id="d59c0-128">You will not always need the **clippingColor** attribute if the edges of your skin are rectangular.</span></span> <span data-ttu-id="d59c0-129">L’apparence de cet exemple est en forme ovale. vous avez donc besoin d’une couleur de découpage pour les parties de l’apparence sur lesquelles vous souhaitez afficher le Bureau ; essentiellement toutes les parties en dehors de l’ovale.</span><span class="sxs-lookup"><span data-stu-id="d59c0-129">The skin in this example is oval-shaped, so you need a clipping color for the parts of the skin that you want to see the desktop through; essentially all parts outside the oval.</span></span> <span data-ttu-id="d59c0-130">Dans cet exemple d’apparence, nous utilisons un jaune foncé, spécifié comme « \# CCCC00 » dans le format Web.</span><span class="sxs-lookup"><span data-stu-id="d59c0-130">In this example skin, we will use a dark yellow, specified as "\#CCCC00" in Web format.</span></span> <span data-ttu-id="d59c0-131">Les raisons de ce choix sont fournies lors de la [création du fichier art principal](creating-the-primary-art-file.md).</span><span class="sxs-lookup"><span data-stu-id="d59c0-131">The reasons for this choice are given in [Creating the Primary Art File](creating-the-primary-art-file.md).</span></span> <span data-ttu-id="d59c0-132">Fondamentalement, cette valeur sera toujours un nombre que vous obtiendrez de votre programme art.</span><span class="sxs-lookup"><span data-stu-id="d59c0-132">Essentially, this value will always be a number that you get from your art program.</span></span>

<span data-ttu-id="d59c0-133">**backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="d59c0-133">**backgroundImage**</span></span>

<span data-ttu-id="d59c0-134">Il s’agit du nom du fichier art principal.</span><span class="sxs-lookup"><span data-stu-id="d59c0-134">This is the name of the primary art file.</span></span> <span data-ttu-id="d59c0-135">Il doit s’agir du nom de fichier et du chemin d’accès exacts de votre fichier art principal.</span><span class="sxs-lookup"><span data-stu-id="d59c0-135">It should be the exact file name and path of your primary art file.</span></span> <span data-ttu-id="d59c0-136">Seuls les fichiers BMP, JPG, GIF et PNG sont pris en charge et BMP est recommandé.</span><span class="sxs-lookup"><span data-stu-id="d59c0-136">Only BMP, JPG, GIF, and PNG files are supported, and BMP is recommended.</span></span>

<span data-ttu-id="d59c0-137">**Spreadsheet**</span><span class="sxs-lookup"><span data-stu-id="d59c0-137">**titleBar**</span></span>

<span data-ttu-id="d59c0-138">Cette apparence n’a pas de **TitleBar**, donc la valeur sera « false ».</span><span class="sxs-lookup"><span data-stu-id="d59c0-138">This skin does not have a **titleBar**, so the value will be "false".</span></span> <span data-ttu-id="d59c0-139">Vous n’avez besoin que d’une barre de titre si vous souhaitez que votre apparence ait une couleur d’arrière-plan et qu’elle soit rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="d59c0-139">You will only want a title bar if you want your skin to have a background color and be rectangular.</span></span>

<span data-ttu-id="d59c0-140">Veillez à placer le Chevron fermant (>) après la valeur **TitleBar** pour indiquer que vous avez terminé la définition de la **vue**.</span><span class="sxs-lookup"><span data-stu-id="d59c0-140">Be sure that you put the closing angle bracket (>) after the **titleBar** value to indicate that you are finished defining the **VIEW**.</span></span> <span data-ttu-id="d59c0-141">Laissez quelques lignes vides avant le **mode** de fermeture et les balises de **thème** .</span><span class="sxs-lookup"><span data-stu-id="d59c0-141">Leave a few blank lines before the closing **VIEW** and **THEME** tags.</span></span> <span data-ttu-id="d59c0-142">Vous aurez besoin des lignes pour le code que vous ajouterez ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d59c0-142">You will need the lines for code that you will add later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d59c0-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d59c0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d59c0-144">**Création du fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="d59c0-144">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




