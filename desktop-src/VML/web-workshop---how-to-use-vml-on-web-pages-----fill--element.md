---
title: Utilisation de l’élément Fill
description: Cet article décrit l’utilisation de l’élément Fill de VML, fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Atelier Web, remplir l’élément
- conception de pages Web, remplir l’élément
- Langage VML (VML), Fill, élément
- VML (langage VML), élément de remplissage
- Vector Graphics, Fill, élément
- Fill, élément
- Éléments VML, remplissage
- Formes VML, élément Fill
- Langage VML (VML), remplissage dégradé
- VML (langage VML), remplissage dégradé
- graphiques vectoriels, remplissage dégradé
- Formes VML, remplissage dégradé
- formes remplies de dégradés
- Langage VML (VML), remplissage de motif
- VML (langage VML), remplissage de motif
- graphiques vectoriels, remplissage de motif
- Formes VML, remplissage de motif
- formes remplies de motifs
- Langage VML (VML), remplissage de l’image
- VML (langage VML), remplissage de l’image
- graphiques vectoriels, remplissage d’image
- Formes VML, remplissage image
- formes pleines d’images
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407792"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="fd655-126">Utilisation de l’élément Fill</span><span class="sxs-lookup"><span data-stu-id="fd655-126">Using the Fill Element</span></span>

<span data-ttu-id="fd655-127">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fd655-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fd655-128">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fd655-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fd655-129">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="fd655-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fd655-130">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="fd655-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fd655-131">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fd655-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fd655-132">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fd655-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fd655-133">Comme vous l’avez appris, vous pouvez utiliser l’attribut de propriété **FillColor** d’un élément de forme prédéfini, tel que `<oval>` ,,,,, `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` , `<arc>` --pour spécifier la couleur utilisée pour remplir la forme.</span><span class="sxs-lookup"><span data-stu-id="fd655-133">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="fd655-134">Dans cette rubrique, nous allons vous montrer comment dessiner une forme remplie avec des effets plus avancés.</span><span class="sxs-lookup"><span data-stu-id="fd655-134">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="fd655-135">Vous pouvez placer le `<fill>` sous-élément à l’intérieur de `<shape>` , ou `<shapetype>` , ou n’importe quel élément de forme prédéfini pour décrire comment remplir la forme.</span><span class="sxs-lookup"><span data-stu-id="fd655-135">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="fd655-136">Vous pouvez ensuite utiliser les attributs de propriété du `<fill>` sous-élément pour personnaliser l’effet de remplissage, tel que le [remplissage dégradé](#gradient-fill), le [remplissage de motif](#pattern-fill), le [remplissage d’image](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="fd655-136">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="fd655-137">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="fd655-137">In this topic:</span></span>

-   [<span data-ttu-id="fd655-138">Remplissage dégradé</span><span class="sxs-lookup"><span data-stu-id="fd655-138">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="fd655-139">Remplissage du motif</span><span class="sxs-lookup"><span data-stu-id="fd655-139">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="fd655-140">Remplissage de l’image</span><span class="sxs-lookup"><span data-stu-id="fd655-140">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="fd655-141">Remplissage dégradé</span><span class="sxs-lookup"><span data-stu-id="fd655-141">Gradient Fill</span></span>

<span data-ttu-id="fd655-142">Pour dessiner une forme remplie de dégradés, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « gradient » ou « gradientRadial », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **Method**, **color2**, **focus** et **angle**.</span><span class="sxs-lookup"><span data-stu-id="fd655-142">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="fd655-143">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="fd655-143">**Examples:**</span></span>

<span data-ttu-id="fd655-144">Pour créer une forme qui est remplie horizontalement, vous pouvez définir l’attribut de propriété de **type** sur « gradient », comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-144">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 octets)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="fd655-146">Si vous modifiez l’attribut de propriété **FillColor** de la forme, la forme est ensuite remplie d’une couleur différente.</span><span class="sxs-lookup"><span data-stu-id="fd655-146">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="fd655-147">Vous pouvez ajouter une deuxième couleur en spécifiant l’attribut de propriété **color2** du `<fill>` sous-élément.</span><span class="sxs-lookup"><span data-stu-id="fd655-147">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="fd655-148">Par exemple, pour créer une forme qui est remplie à l’aide de deux couleurs, vous pouvez ajouter une deuxième couleur en spécifiant l’attribut de propriété **color2** du `<fill>` sous-élément, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-148">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 octets)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="fd655-150">Vous pouvez définir l’attribut de propriété de la **méthode** sur « Linear » ou « Sigma » ou « any » ou « None ».</span><span class="sxs-lookup"><span data-stu-id="fd655-150">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="fd655-151">L’effet du dégradé est légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="fd655-151">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="fd655-152">En outre, vous pouvez utiliser l’attribut de propriété **angle**,**focus**,**focussize** ou **focusposition** pour modifier la façon dont le dégradé se déplace.</span><span class="sxs-lookup"><span data-stu-id="fd655-152">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="fd655-153">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="fd655-153">**Examples:**</span></span>

 

<span data-ttu-id="fd655-154">Pour créer une forme dégradée verticalement, vous pouvez définir l’attribut de propriété angle sur angle = « -90 », comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-154">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 octets)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="fd655-156">Pour créer une forme qui est remplie d’un dégradé Diagonal, vous pouvez définir l’attribut de propriété **angle** sur angle = « -135 », comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-156">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 octets)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="fd655-158">Pour créer une forme qui est remplie d’une diagonale dégradée, vous pouvez définir l’attribut de propriété **angle** sur angle = « -45 », comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-158">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 octets)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="fd655-160">Pour créer une forme qui est remplie par le dégradé à partir du centre, vous pouvez spécifier `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-160">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 octets)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="fd655-162">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="fd655-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="fd655-163">Remplissage du motif</span><span class="sxs-lookup"><span data-stu-id="fd655-163">Pattern Fill</span></span>

<span data-ttu-id="fd655-164">Pour dessiner une forme remplie de motifs, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « Pattern », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **src** et **color2**.</span><span class="sxs-lookup"><span data-stu-id="fd655-164">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="fd655-165">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="fd655-165">**Examples:**</span></span>

<span data-ttu-id="fd655-166">Pour créer une forme remplie avec une image de modèle, vous pouvez spécifier l’attribut de propriété de **type** sur « pattern » et faire pointer l’attribut de propriété **src** vers l’emplacement du fichier d’image de modèle, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-166">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 octets)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="fd655-168">Si vous pointez l’attribut de propriété **src** vers un fichier de modèle différent, vous pouvez créer une forme qui est remplie avec un autre modèle.</span><span class="sxs-lookup"><span data-stu-id="fd655-168">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="fd655-169">En outre, vous pouvez modifier la couleur en spécifiant une valeur différente pour l’attribut de propriété **FillColor** ou **color2** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-169">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 octets)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="fd655-171">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="fd655-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="fd655-172">Remplissage de l’image</span><span class="sxs-lookup"><span data-stu-id="fd655-172">Picture Fill</span></span>

<span data-ttu-id="fd655-173">Pour dessiner une forme remplie d’image, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « Frame », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **src** et **color2**.</span><span class="sxs-lookup"><span data-stu-id="fd655-173">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="fd655-174">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="fd655-174">**Examples:**</span></span>

<span data-ttu-id="fd655-175">Pour créer une forme remplie avec un fichier image, vous pouvez spécifier l’attribut de propriété de **type** « Frame », puis faire pointer l’attribut de propriété **src** vers l’emplacement du fichier image, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="fd655-175">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 octets)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="fd655-177">Vous pouvez facilement créer une forme remplie avec une autre image en pointant l’attribut de propriété **src** vers un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="fd655-177">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="fd655-178">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="fd655-178">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 