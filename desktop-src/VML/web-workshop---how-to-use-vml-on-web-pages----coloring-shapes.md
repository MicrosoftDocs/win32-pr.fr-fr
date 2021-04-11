---
title: Colorer les formes
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Atelier Web, formes de coloration
- conception de pages Web, colorer les formes
- Langage VML (VML), colorer les formes
- VML (langage VML), formes de coloration
- graphiques vectoriels, colorer les formes
- Formes VML, coloration
- colorer les formes
- Langage VML (VML), noms de couleur de mot clé
- VML (langage VML), noms de couleur de mot clé
- graphiques vectoriels, noms de couleur de mot clé
- noms des couleurs des mots clés
- Langage VML (VML), triplets RVB
- VML (langage VML), triplets RGB
- graphiques vectoriels, triplets RGB
- Triplets RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031543"
---
# <a name="coloring-shapes"></a><span data-ttu-id="0dfe5-119">Colorer les formes</span><span class="sxs-lookup"><span data-stu-id="0dfe5-119">Coloring Shapes</span></span>

<span data-ttu-id="0dfe5-120">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0dfe5-121">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0dfe5-122">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0dfe5-123">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0dfe5-124">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0dfe5-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0dfe5-125">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0dfe5-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0dfe5-126">Comme nous l’avons mentionné dans les sections précédentes, vous pouvez utiliser « Red » pour représenter une couleur en rouge, « Blue » pour représenter une couleur en bleu, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-126">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="0dfe5-127">Dans cette rubrique, nous allons vous montrer comment dessiner des formes dans les couleurs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-127">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="0dfe5-128">VML étend la syntaxe des couleurs HTML et CSS.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-128">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="0dfe5-129">Lorsque le type d’attribut d’un élément VML est Color, tel que **FillColor** et **StrokeColor** , vous pouvez exprimer la couleur à l’aide d’un [nom de couleur de mot clé](#keyword-color-name) ou d’un [triplet RVB](#rgb-triplet).</span><span class="sxs-lookup"><span data-stu-id="0dfe5-129">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="0dfe5-130">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0dfe5-130">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="0dfe5-131">Nom de la couleur du mot clé</span><span class="sxs-lookup"><span data-stu-id="0dfe5-131">Keyword Color Name</span></span>

<span data-ttu-id="0dfe5-132">Le code HTML 4,0 définit une liste de noms de couleurs de mot clé.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-132">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="0dfe5-133">Il s’agit de l’Aqua, du noir, du bleu, de la fuchsia, du gris, du vert, de la chaux, du marron, de la marine, de l’Olivier, du violet, du rouge, de l’argent, du bleu vert et du jaune.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-133">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="0dfe5-134">La valeur RVB pour ces 16 couleurs est définie dans la [spécification HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="0dfe5-134">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="0dfe5-135">Par exemple, vous pouvez dessiner un rectangle rempli en jaune en spécifiant `fillcolor="yellow"` , et lui attribuer un contour bleu en spécifiant `strokecolor="blue"` , comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0dfe5-135">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 octets)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="0dfe5-137">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0dfe5-137">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="0dfe5-138">Triplet RVB</span><span class="sxs-lookup"><span data-stu-id="0dfe5-138">RGB Triplet</span></span>

<span data-ttu-id="0dfe5-139">Si la couleur n’est pas un [nom de couleur de mot clé](#keyword-color-name), vous pouvez exprimer la couleur sous la forme d’un triple nombre décimal ou d’une tripleté hexadécimale RVB.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-139">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="0dfe5-140">Avec les triplets RVB, vous pouvez spécifier des valeurs pour les composants rouge, vert et bleu de la couleur, en affectant à chaque composant une valeur comprise entre 0 et 255 en décimal, ou 00 à FF en hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-140">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="0dfe5-141">Par exemple, vous pouvez créer un rectangle rempli avec une couleur personnalisée avec une valeur RVB de 253, 249, 186 en décimal en spécifiant `fillcolor="rgb(253,249, 186)"` ou `fillcolor="#FDF9BA"` , comme indiqué dans la représentation VML suivante.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-141">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="0dfe5-142">Au format hexadécimal, la valeur 253 devient FD, 249 devient F9 et 186 devient BA.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-142">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 octets)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="0dfe5-144">Si le RVB au format hexadécimal a un modèle tel que XXYYZZ, vous pouvez l’abréger en XYZ.</span><span class="sxs-lookup"><span data-stu-id="0dfe5-144">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="0dfe5-145">Par exemple, « \# 66FF99 » peut être écrit en tant que « \# 6F9 ».</span><span class="sxs-lookup"><span data-stu-id="0dfe5-145">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="0dfe5-146">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0dfe5-146">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="0dfe5-147">Résumé</span><span class="sxs-lookup"><span data-stu-id="0dfe5-147">Summary</span></span>

<span data-ttu-id="0dfe5-148">Dans VML, vous pouvez représenter une couleur dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="0dfe5-148">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="0dfe5-149">FillColor = "Blue"</span><span class="sxs-lookup"><span data-stu-id="0dfe5-149">fillcolor="blue"</span></span>
2.  <span data-ttu-id="0dfe5-150">FillColor = "RGB (0, 0255)"</span><span class="sxs-lookup"><span data-stu-id="0dfe5-150">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="0dfe5-151">FillColor = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="0dfe5-151">fillcolor="\#0000ff"</span></span>

 

 