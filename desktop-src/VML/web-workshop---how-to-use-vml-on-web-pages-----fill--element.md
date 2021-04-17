---
title: Utilisation de l’élément Fill
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
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
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104570474"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="99823-127">Utilisation de l’élément Fill</span><span class="sxs-lookup"><span data-stu-id="99823-127">Using the Fill Element</span></span>

<span data-ttu-id="99823-128">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="99823-128">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="99823-129">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="99823-129">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="99823-130">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="99823-130">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="99823-131">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="99823-131">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="99823-132">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="99823-132">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="99823-133">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="99823-133">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="99823-134">Comme vous l’avez appris, vous pouvez utiliser l’attribut de propriété **FillColor** d’un élément de forme prédéfini, tel que `<oval>` ,,,,, `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` , `<arc>` --pour spécifier la couleur utilisée pour remplir la forme.</span><span class="sxs-lookup"><span data-stu-id="99823-134">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="99823-135">Dans cette rubrique, nous allons vous montrer comment dessiner une forme remplie avec des effets plus avancés.</span><span class="sxs-lookup"><span data-stu-id="99823-135">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="99823-136">Vous pouvez placer le `<fill>` sous-élément à l’intérieur de `<shape>` , ou `<shapetype>` , ou n’importe quel élément de forme prédéfini pour décrire comment remplir la forme.</span><span class="sxs-lookup"><span data-stu-id="99823-136">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="99823-137">Vous pouvez ensuite utiliser les attributs de propriété du `<fill>` sous-élément pour personnaliser l’effet de remplissage, tel que le [remplissage dégradé](#gradient-fill), le [remplissage de motif](#pattern-fill), le [remplissage d’image](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="99823-137">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="99823-138">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="99823-138">In this topic:</span></span>

-   [<span data-ttu-id="99823-139">Remplissage dégradé</span><span class="sxs-lookup"><span data-stu-id="99823-139">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="99823-140">Remplissage du motif</span><span class="sxs-lookup"><span data-stu-id="99823-140">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="99823-141">Remplissage de l’image</span><span class="sxs-lookup"><span data-stu-id="99823-141">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="99823-142">Remplissage dégradé</span><span class="sxs-lookup"><span data-stu-id="99823-142">Gradient Fill</span></span>

<span data-ttu-id="99823-143">Pour dessiner une forme remplie de dégradés, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « gradient » ou « gradientRadial », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **Method**, **color2**, **focus** et **angle**.</span><span class="sxs-lookup"><span data-stu-id="99823-143">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="99823-144">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="99823-144">**Examples:**</span></span>

<span data-ttu-id="99823-145">Pour créer une forme qui est remplie horizontalement, vous pouvez définir l’attribut de propriété de **type** sur « gradient », comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-145">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 octets)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="99823-147">Si vous modifiez l’attribut de propriété **FillColor** de la forme, la forme est ensuite remplie d’une couleur différente.</span><span class="sxs-lookup"><span data-stu-id="99823-147">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="99823-148">Vous pouvez ajouter une deuxième couleur en spécifiant l’attribut de propriété **color2** du `<fill>` sous-élément.</span><span class="sxs-lookup"><span data-stu-id="99823-148">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="99823-149">Par exemple, pour créer une forme qui est remplie à l’aide de deux couleurs, vous pouvez ajouter une deuxième couleur en spécifiant l’attribut de propriété **color2** du `<fill>` sous-élément, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-149">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 octets)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="99823-151">Vous pouvez définir l’attribut de propriété de la **méthode** sur « Linear » ou « Sigma » ou « any » ou « None ».</span><span class="sxs-lookup"><span data-stu-id="99823-151">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="99823-152">L’effet du dégradé est légèrement différent.</span><span class="sxs-lookup"><span data-stu-id="99823-152">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="99823-153">En outre, vous pouvez utiliser l’attribut de propriété **angle**,**focus**,**focussize** ou **focusposition** pour modifier la façon dont le dégradé se déplace.</span><span class="sxs-lookup"><span data-stu-id="99823-153">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="99823-154">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="99823-154">**Examples:**</span></span>

 

<span data-ttu-id="99823-155">Pour créer une forme dégradée verticalement, vous pouvez définir l’attribut de propriété angle sur angle = « -90 », comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-155">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 octets)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="99823-157">Pour créer une forme qui est remplie d’un dégradé Diagonal, vous pouvez définir l’attribut de propriété **angle** sur angle = « -135 », comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-157">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 octets)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="99823-159">Pour créer une forme qui est remplie d’une diagonale dégradée, vous pouvez définir l’attribut de propriété **angle** sur angle = « -45 », comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-159">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 octets)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="99823-161">Pour créer une forme qui est remplie par le dégradé à partir du centre, vous pouvez spécifier `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-161">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 octets)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="99823-163">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="99823-163">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="99823-164">Remplissage du motif</span><span class="sxs-lookup"><span data-stu-id="99823-164">Pattern Fill</span></span>

<span data-ttu-id="99823-165">Pour dessiner une forme remplie de motifs, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « Pattern », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **src** et **color2**.</span><span class="sxs-lookup"><span data-stu-id="99823-165">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="99823-166">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="99823-166">**Examples:**</span></span>

<span data-ttu-id="99823-167">Pour créer une forme remplie avec une image de modèle, vous pouvez spécifier l’attribut de propriété de **type** sur « pattern » et faire pointer l’attribut de propriété **src** vers l’emplacement du fichier d’image de modèle, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-167">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 octets)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="99823-169">Si vous pointez l’attribut de propriété **src** vers un fichier de modèle différent, vous pouvez créer une forme qui est remplie avec un autre modèle.</span><span class="sxs-lookup"><span data-stu-id="99823-169">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="99823-170">En outre, vous pouvez modifier la couleur en spécifiant une valeur différente pour l’attribut de propriété **FillColor** ou **color2** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-170">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 octets)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="99823-172">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="99823-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="99823-173">Remplissage de l’image</span><span class="sxs-lookup"><span data-stu-id="99823-173">Picture Fill</span></span>

<span data-ttu-id="99823-174">Pour dessiner une forme remplie d’image, vous pouvez définir l’attribut de propriété de **type** du `<fill>` sous-élément sur « Frame », puis spécifier d’autres attributs de propriété du `<fill>` sous-élément, tels que **src** et **color2**.</span><span class="sxs-lookup"><span data-stu-id="99823-174">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="99823-175">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="99823-175">**Examples:**</span></span>

<span data-ttu-id="99823-176">Pour créer une forme remplie avec un fichier image, vous pouvez spécifier l’attribut de propriété de **type** « Frame », puis faire pointer l’attribut de propriété **src** vers l’emplacement du fichier image, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="99823-176">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 octets)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="99823-178">Vous pouvez facilement créer une forme remplie avec une autre image en pointant l’attribut de propriété **src** vers un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="99823-178">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="99823-179">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="99823-179">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 