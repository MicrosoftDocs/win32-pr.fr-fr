---
title: Utilisation de l’élément Stroke
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
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
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316355"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="3ea00-132">Utilisation de l’élément Stroke</span><span class="sxs-lookup"><span data-stu-id="3ea00-132">Using the Stroke Element</span></span>

<span data-ttu-id="3ea00-133">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ea00-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ea00-134">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3ea00-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ea00-135">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3ea00-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ea00-136">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3ea00-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ea00-137">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ea00-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ea00-138">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ea00-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ea00-139">Utilisation de `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="3ea00-139">Using `<stroke>`</span></span>

<span data-ttu-id="3ea00-140">Comme vous l’avez appris, vous pouvez utiliser les attributs de propriété **StrokeColor** et **StrokeWeight** d’une forme prédéfinie, telle que `<oval>` , `<line>` ,,, `<polyline>` `<curve>` `<rect>` , `<roundrect>` , `<arc>` --pour spécifier la couleur et le poids du contour d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3ea00-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="3ea00-141">Dans cette rubrique, nous allons illustrer comment dessiner une forme avec un contour plus avancé.</span><span class="sxs-lookup"><span data-stu-id="3ea00-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="3ea00-142">Vous pouvez placer le `<stroke>` sous-élément à l’intérieur de `<shape>` , ou `<shapetype>` , ou n’importe quel élément de forme prédéfini pour décrire comment dessiner le contour de la forme.</span><span class="sxs-lookup"><span data-stu-id="3ea00-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="3ea00-143">Vous pouvez ensuite utiliser les attributs de propriété (par exemple, [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [fillType](#filltype) ) du `<stroke>` sous-élément pour personnaliser le plan.</span><span class="sxs-lookup"><span data-stu-id="3ea00-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="3ea00-144">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="3ea00-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="3ea00-145">DashStyle</span><span class="sxs-lookup"><span data-stu-id="3ea00-145">dashstyle</span></span>

<span data-ttu-id="3ea00-146">Vous pouvez utiliser l’attribut de propriété **DashStyle** du `<stroke>` sous-élément pour dessiner un contour avec différents styles de tirets.</span><span class="sxs-lookup"><span data-stu-id="3ea00-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="3ea00-147">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="3ea00-147">**Examples:**</span></span>

<span data-ttu-id="3ea00-148">Si vous spécifiez `<v:stroke dashstyle="solid" />` à l’intérieur de l' `<line>` élément, vous pouvez créer une ligne pleine, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 octets)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="3ea00-150">Si vous modifiez l’attribut de propriété **DashStyle** en « dot », vous pouvez créer une ligne en pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 octets)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="3ea00-152">Si vous modifiez l’attribut de propriété **DashStyle** en « Dash », vous pouvez créer une ligne de tirets, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 octets)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="3ea00-154">Si vous modifiez l’attribut de propriété **DashStyle** en « tiret point », vous pouvez créer une ligne avec un style en pointillés et en pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 octets)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="3ea00-156">Si vous modifiez l’attribut de propriété **DashStyle** en « longdash », vous pouvez créer une ligne avec un style Dash long, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 octets)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="3ea00-158">Si vous modifiez l’attribut de propriété **DashStyle** en « longdashdot », vous pouvez créer une ligne avec un style tirets longs et pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 octets)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="3ea00-160">Si vous placez `<v:stroke dashstyle="dashdot" />` à l’intérieur de l' `<rect>` élément, vous pouvez créer un rectangle avec une bordure en pointillés et en pointillés, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 octets)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="3ea00-162">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="3ea00-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="3ea00-163">opacity</span><span class="sxs-lookup"><span data-stu-id="3ea00-163">opacity</span></span>

<span data-ttu-id="3ea00-164">Vous pouvez utiliser l’attribut de propriété **Opacity** du `<stroke>` sous-élément pour dessiner un contour avec différents styles d’opacité.</span><span class="sxs-lookup"><span data-stu-id="3ea00-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="3ea00-165">La valeur de l’attribut de propriété **Opacity** peut être n’importe quel nombre compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="3ea00-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="3ea00-166">Par défaut, il s’agit de 1, ce qui indique une opacité totale.</span><span class="sxs-lookup"><span data-stu-id="3ea00-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="3ea00-167">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="3ea00-167">**Examples:**</span></span>

<span data-ttu-id="3ea00-168">La représentation VML suivante crée une ligne avec une opacité complète :</span><span class="sxs-lookup"><span data-stu-id="3ea00-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 octets)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="3ea00-170">Si vous ajoutez `<v:stroke opacity="0.5" />` à l’intérieur de l' `<line>` élément, vous pouvez créer une ligne avec une opacité de 50%, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 octets)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="3ea00-172">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="3ea00-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="3ea00-173">LineStyle</span><span class="sxs-lookup"><span data-stu-id="3ea00-173">linestyle</span></span>

<span data-ttu-id="3ea00-174">Vous pouvez utiliser l’attribut de propriété **LineStyle** du `<stroke>` sous-élément pour dessiner un plan avec différents styles de ligne.</span><span class="sxs-lookup"><span data-stu-id="3ea00-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="3ea00-175">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="3ea00-175">**Examples:**</span></span>

<span data-ttu-id="3ea00-176">Si vous spécifiez `<v:stroke linestyle="single" />` à l’intérieur de l' `<rect>` élément, vous pouvez créer un rectangle avec un seul plan, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 octets)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="3ea00-178">Si vous modifiez l’attribut de propriété **LineStyle** en « thinthin », vous pouvez créer un rectangle avec le contour (1:1:1), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 octets)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="3ea00-180">Si vous modifiez l’attribut de propriété **LineStyle** en « thinthick », vous pouvez créer un rectangle avec le contour (1:1:2), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 octets)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="3ea00-182">Si vous modifiez l’attribut de propriété **LineStyle** en « thickthin », vous pouvez créer un rectangle avec le contour (2:1:1), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 octets)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="3ea00-184">Si vous modifiez l’attribut de propriété **LineStyle** en « thickbetweenthin », vous pouvez créer un rectangle avec le contour (1:1:2:1:1), comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 octets)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="3ea00-186">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="3ea00-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="3ea00-187">joinstyle</span><span class="sxs-lookup"><span data-stu-id="3ea00-187">joinstyle</span></span>

<span data-ttu-id="3ea00-188">Vous pouvez utiliser l’attribut **joinstyle** du `<stroke>` sous-élément pour définir la manière dont les lignes sont jointes.</span><span class="sxs-lookup"><span data-stu-id="3ea00-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="3ea00-189">Par exemple, pour créer une forme qui a la structure de jointures circulaires, comme indiqué dans l’illustration suivante, vous pouvez spécifier `<v:stroke joinstyle="round" />` à l’intérieur de l' `<polyline>` élément, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 octets)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="3ea00-191">Si vous modifiez l’attribut de propriété **joinstyle** en « biseau », vous pouvez créer une forme qui a le contour biseau-Join, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 octets)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="3ea00-193">Si vous affectez à l’attribut de propriété **joinstyle** la valeur « Mitre », vous pouvez créer une forme qui a la structure de jointure Mitre, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 octets)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="3ea00-195">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="3ea00-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="3ea00-196">fillType</span><span class="sxs-lookup"><span data-stu-id="3ea00-196">filltype</span></span>

<span data-ttu-id="3ea00-197">Vous pouvez utiliser l’attribut de propriété **fillType** du `<stroke>` sous-élément pour dessiner un contour avec divers effets de remplissage.</span><span class="sxs-lookup"><span data-stu-id="3ea00-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="3ea00-198">**Exemples :**</span><span class="sxs-lookup"><span data-stu-id="3ea00-198">**Examples:**</span></span>

<span data-ttu-id="3ea00-199">Si vous spécifiez `<v:stroke filltype="solid" />` à l’intérieur de l' `<roundrect>` élément, vous pouvez créer un rectangle à coins arrondis avec le contour plein, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 octets)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="3ea00-201">Si vous modifiez l’attribut de propriété **fillType** en « pattern », que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier d’image de modèle et que vous définissez l’attribut de propriété **color2** sur la deuxième couleur du motif, vous pouvez créer un rectangle arrondi avec une structure de motif, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 octets)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="3ea00-203">Si vous modifiez l’attribut de propriété **fillType** en « vignette » et que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier image, vous pouvez créer un rectangle à coins arrondis avec un contour en mosaïque, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 octets)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="3ea00-205">Si vous modifiez l’attribut de propriété **fillType** en « Frame » et que vous pointez l’attribut de propriété **src** sur l’emplacement du fichier image, vous pouvez créer un rectangle à coins arrondis avec un contour d’image, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="3ea00-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 octets)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="3ea00-207">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="3ea00-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 