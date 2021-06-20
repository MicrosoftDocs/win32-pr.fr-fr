---
title: Utilisation de l’élément Stroke
description: Cet article décrit l’utilisation de l’élément Stroke de VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Atelier Web, élément Stroke
- conception de pages Web, élément Stroke
- Langage VML (VML), élément Stroke
- VML (langage VML), élément Stroke
- Vector Graphics, élément Stroke
- Stroke, élément
- Éléments VML, trait
- Formes VML, élément Stroke
- Langage VML (VML), attribut de propriété DashStyle
- VML (langage VML), attribut de propriété DashStyle
- Graphics Vector, propriété DashStyle, attribut
- propriété DashStyle (attribut)
- Langage VML (VML), attribut de propriété Opacity
- VML (langage VML), attribut de propriété Opacity
- Graphics Vector, attribut de propriété Opacity
- attribut de propriété Opacity
- Langage VML (VML), attribut de propriété LineStyle
- VML (langage VML), attribut de propriété LineStyle
- Vector Graphics, attribut LineStyle Property
- attribut LineStyle de la propriété
- Langage VML (VML), attribut de propriété joinstyle
- VML (langage VML), attribut de propriété joinstyle
- Graphics Vector, attribut de propriété joinstyle
- attribut de propriété joinstyle
- Langage VML (VML), attribut de propriété fillType
- VML (langage VML), attribut de propriété fillType
- Graphics Vector, attribut de propriété fillType
- attribut de propriété fillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407842"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="b5752-131">Utilisation de l’élément Stroke</span><span class="sxs-lookup"><span data-stu-id="b5752-131">Using the Stroke Element</span></span>

<span data-ttu-id="b5752-132">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b5752-132">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b5752-133">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b5752-133">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b5752-134">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b5752-134">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b5752-135">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b5752-135">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b5752-136">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b5752-136">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b5752-137">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b5752-137">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b5752-138">Utilisation de `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="b5752-138">Using `<stroke>`</span></span>

<span data-ttu-id="b5752-139">Comme vous l’avez appris, vous pouvez utiliser les attributs de propriété **StrokeColor** et **StrokeWeight** d’une forme prédéfinie, telle que `<oval>` , `<line>` ,,, `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --pour spécifier la couleur et le poids du contour d’une forme.</span><span class="sxs-lookup"><span data-stu-id="b5752-139">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="b5752-140">Dans cette rubrique, nous allons illustrer comment dessiner une forme avec un contour plus avancé.</span><span class="sxs-lookup"><span data-stu-id="b5752-140">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="b5752-141">Vous pouvez placer le `<stroke>` sous-élément à l’intérieur de `<shape>` , ou `<shapetype>` , ou n’importe quel élément de forme prédéfini pour décrire comment dessiner le contour de la forme.</span><span class="sxs-lookup"><span data-stu-id="b5752-141">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="b5752-142">Vous pouvez ensuite utiliser les attributs de propriété (par exemple, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [fillType](#filltype) ) du `<stroke>` sous-élément pour personnaliser le plan.</span><span class="sxs-lookup"><span data-stu-id="b5752-142">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="b5752-143">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="b5752-143">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="b5752-144">DashStyle</span><span class="sxs-lookup"><span data-stu-id="b5752-144">dashstyle</span></span>

<span data-ttu-id="b5752-145">Vous pouvez utiliser l’attribut de propriété **DashStyle** du `<stroke>` sous-élément pour dessiner un contour avec différents styles de tirets.</span><span class="sxs-lookup"><span data-stu-id="b5752-145">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="b5752-146">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="b5752-146">**Examples:**</span></span>

<span data-ttu-id="b5752-147">Si vous spécifiez `<v:stroke dashstyle="solid" />` à l’intérieur de l' `<line>` élément, vous pouvez créer une ligne pleine, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-147">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 octets)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="b5752-149">Si vous modifiez l’attribut de propriété **DashStyle** en « dot », vous pouvez créer une ligne en pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-149">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 octets)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="b5752-151">Si vous modifiez l’attribut de propriété **DashStyle** en « Dash », vous pouvez créer une ligne de tirets, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-151">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 octets)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="b5752-153">Si vous modifiez l’attribut de propriété **DashStyle** en « tiret point », vous pouvez créer une ligne avec un style en pointillés et en pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-153">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 octets)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="b5752-155">Si vous modifiez l’attribut de propriété **DashStyle** en « longdash », vous pouvez créer une ligne avec un style Dash long, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-155">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 octets)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="b5752-157">Si vous modifiez l’attribut de propriété **DashStyle** en « longdashdot », vous pouvez créer une ligne avec un style tirets longs et pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-157">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 octets)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="b5752-159">Si vous placez `<v:stroke dashstyle="dashdot" />` à l’intérieur de l' `<rect>` élément, vous pouvez créer un rectangle avec une bordure en pointillés et en pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-159">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 octets)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="b5752-161">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="b5752-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="b5752-162">opacity</span><span class="sxs-lookup"><span data-stu-id="b5752-162">opacity</span></span>

<span data-ttu-id="b5752-163">Vous pouvez utiliser l’attribut de propriété **Opacity** du `<stroke>` sous-élément pour dessiner un contour avec différents styles d’opacité.</span><span class="sxs-lookup"><span data-stu-id="b5752-163">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="b5752-164">La valeur de l’attribut de propriété **Opacity** peut être n’importe quel nombre compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="b5752-164">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="b5752-165">Par défaut, il s’agit de 1, ce qui indique une opacité totale.</span><span class="sxs-lookup"><span data-stu-id="b5752-165">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="b5752-166">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="b5752-166">**Examples:**</span></span>

<span data-ttu-id="b5752-167">La représentation VML suivante crée une ligne avec une opacité complète :</span><span class="sxs-lookup"><span data-stu-id="b5752-167">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 octets)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="b5752-169">Si vous ajoutez `<v:stroke opacity="0.5" />` à l’intérieur de l' `<line>` élément, vous pouvez créer une ligne avec une opacité de 50%, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-169">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 octets)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="b5752-171">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="b5752-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="b5752-172">LineStyle</span><span class="sxs-lookup"><span data-stu-id="b5752-172">linestyle</span></span>

<span data-ttu-id="b5752-173">Vous pouvez utiliser l’attribut de propriété **LineStyle** du `<stroke>` sous-élément pour dessiner un plan avec différents styles de ligne.</span><span class="sxs-lookup"><span data-stu-id="b5752-173">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="b5752-174">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="b5752-174">**Examples:**</span></span>

<span data-ttu-id="b5752-175">Si vous spécifiez `<v:stroke linestyle="single" />` à l’intérieur de l' `<rect>` élément, vous pouvez créer un rectangle avec un seul plan, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-175">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 octets)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="b5752-177">Si vous modifiez l’attribut de propriété **LineStyle** en « thinthin », vous pouvez créer un rectangle avec le contour (1:1:1), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-177">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 octets)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="b5752-179">Si vous modifiez l’attribut de propriété **LineStyle** en « thinthick », vous pouvez créer un rectangle avec le contour (1:1:2), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-179">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 octets)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="b5752-181">Si vous modifiez l’attribut de propriété **LineStyle** en « thickthin », vous pouvez créer un rectangle avec le contour (2:1:1), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-181">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 octets)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="b5752-183">Si vous modifiez l’attribut de propriété **LineStyle** en « thickbetweenthin », vous pouvez créer un rectangle avec le contour (1:1:2:1:1), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-183">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 octets)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="b5752-185">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="b5752-185">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="b5752-186">joinstyle</span><span class="sxs-lookup"><span data-stu-id="b5752-186">joinstyle</span></span>

<span data-ttu-id="b5752-187">Vous pouvez utiliser l’attribut **joinstyle** du `<stroke>` sous-élément pour définir la manière dont les lignes sont jointes.</span><span class="sxs-lookup"><span data-stu-id="b5752-187">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="b5752-188">Par exemple, pour créer une forme qui a la structure de jointures circulaires, comme indiqué dans l’illustration suivante, vous pouvez spécifier `<v:stroke joinstyle="round" />` à l’intérieur de l' `<polyline>` élément, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-188">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 octets)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="b5752-190">Si vous modifiez l’attribut de propriété **joinstyle** en « biseau », vous pouvez créer une forme qui a le contour biseau-Join, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-190">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 octets)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="b5752-192">Si vous affectez à l’attribut de propriété **joinstyle** la valeur « Mitre », vous pouvez créer une forme qui a la structure de jointure Mitre, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-192">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 octets)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="b5752-194">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="b5752-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="b5752-195">fillType</span><span class="sxs-lookup"><span data-stu-id="b5752-195">filltype</span></span>

<span data-ttu-id="b5752-196">Vous pouvez utiliser l’attribut de propriété **fillType** du `<stroke>` sous-élément pour dessiner un contour avec divers effets de remplissage.</span><span class="sxs-lookup"><span data-stu-id="b5752-196">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="b5752-197">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="b5752-197">**Examples:**</span></span>

<span data-ttu-id="b5752-198">Si vous spécifiez `<v:stroke filltype="solid" />` à l’intérieur de l' `<roundrect>` élément, vous pouvez créer un rectangle à coins arrondis avec le contour plein, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-198">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 octets)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="b5752-200">Si vous modifiez l’attribut de propriété **fillType** en « pattern », que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier d’image de modèle et que vous définissez l’attribut de propriété **color2** sur la deuxième couleur du motif, vous pouvez créer un rectangle arrondi avec une structure de motif, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-200">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 octets)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="b5752-202">Si vous modifiez l’attribut de propriété **fillType** en « vignette » et que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier image, vous pouvez créer un rectangle à coins arrondis avec un contour en mosaïque, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-202">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 octets)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="b5752-204">Si vous modifiez l’attribut de propriété **fillType** en « Frame » et que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier image, vous pouvez créer un rectangle à coins arrondis avec un contour d’image, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="b5752-204">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 octets)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="b5752-206">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="b5752-206">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 