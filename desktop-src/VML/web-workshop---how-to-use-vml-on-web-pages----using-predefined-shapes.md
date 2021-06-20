---
title: Utilisation de formes prédéfinies
description: Cet article décrit l’utilisation de formes prédéfinies dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Atelier Web, formes prédéfinies
- conception de pages Web, formes prédéfinies
- Langage VML (VML), formes prédéfinies
- VML (langage VML), formes prédéfinies
- graphiques vectoriels, formes prédéfinies
- Formes VML, prédéfinies
- formes prédéfinies
- Langage VML (VML), Rect, élément
- VML (langage VML), Rect, élément
- Vector Graphics, Rect, élément
- Rect, élément
- Éléments VML, Rect
- Langage VML (VML), élément roundRect
- VML (langage VML), élément roundRect
- Graphics Vector, élément roundRect
- élément roundRect
- Éléments VML, roundRect
- Langage VML (VML), élément de ligne
- VML (langage VML), élément de ligne
- graphique vectoriel, élément Line
- élément Line
- Éléments VML, ligne
- Langage VML (VML), élément Polyline
- VML (langage VML), élément Polyline
- Graphics Vector, élément Polyline
- élément Polyline
- Éléments VML, polyligne
- Langage VML (VML), élément Curve
- VML (langage VML), élément Curve
- graphique vectoriel, élément Curve
- élément Curve
- Éléments VML, courbe
- Langage VML (VML), élément arc
- VML (langage VML), élément arc
- Vector Graphics, élément arc
- élément arc
- Éléments VML, arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407682"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="2a0f9-140">Utilisation de formes prédéfinies</span><span class="sxs-lookup"><span data-stu-id="2a0f9-140">Using Predefined Shapes</span></span>

<span data-ttu-id="2a0f9-141">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-141">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2a0f9-142">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-142">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2a0f9-143">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-143">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2a0f9-144">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-144">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2a0f9-145">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2a0f9-145">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2a0f9-146">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2a0f9-146">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2a0f9-147">Comme vous l’avez appris, vous pouvez utiliser l' `<oval>` élément de VML pour créer un ovale simple.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-147">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="2a0f9-148">VML fournit plusieurs autres éléments prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-148">VML provides several other predefined elements.</span></span> <span data-ttu-id="2a0f9-149">Dans cette rubrique, nous allons vous montrer comment dessiner des graphiques à l’aide de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-149">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="2a0f9-150">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-150">In this topic:</span></span>

-   [<span data-ttu-id="2a0f9-151">rectangulaire</span><span class="sxs-lookup"><span data-stu-id="2a0f9-151">rect</span></span>](#roundrect)
-   [<span data-ttu-id="2a0f9-152">roundrect</span><span class="sxs-lookup"><span data-stu-id="2a0f9-152">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="2a0f9-153">line</span><span class="sxs-lookup"><span data-stu-id="2a0f9-153">line</span></span>](#polyline)
-   [<span data-ttu-id="2a0f9-154">polyligne</span><span class="sxs-lookup"><span data-stu-id="2a0f9-154">polyline</span></span>](#polyline)
-   [<span data-ttu-id="2a0f9-155">courbe</span><span class="sxs-lookup"><span data-stu-id="2a0f9-155">curve</span></span>](#curve)
-   [<span data-ttu-id="2a0f9-156">arc</span><span class="sxs-lookup"><span data-stu-id="2a0f9-156">arc</span></span>](#arc)
-   [<span data-ttu-id="2a0f9-157">Résumé</span><span class="sxs-lookup"><span data-stu-id="2a0f9-157">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="2a0f9-158">rect</span><span class="sxs-lookup"><span data-stu-id="2a0f9-158">rect</span></span>

<span data-ttu-id="2a0f9-159">Vous pouvez utiliser l' `<rect>` élément pour dessiner un rectangle.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-159">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="2a0f9-160">Vous pouvez ensuite personnaliser le rectangle en spécifiant des attributs de propriété différents.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-160">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="2a0f9-161">Par exemple, vous pouvez dessiner un rectangle qui est rempli en bleu en spécifiant **FillColor**= « Blue » et lui attribuer un contour rouge de point 3,5 en spécifiant **StrokeColor**= "Red" **StrokeWeight**= "3.5 PT", comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-161">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 octets)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="2a0f9-163">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="2a0f9-163">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="2a0f9-164">(Remarque : la spécification VML n’a pas de signet pour l' `<rect>` élément.)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-164">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="2a0f9-165">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-165">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="2a0f9-166">roundrect</span><span class="sxs-lookup"><span data-stu-id="2a0f9-166">roundrect</span></span>

<span data-ttu-id="2a0f9-167">Vous pouvez utiliser l' `<roundrect>` élément pour dessiner un rectangle avec des angles arrondis.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-167">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="2a0f9-168">Vous pouvez ensuite personnaliser le rectangle arrondi en spécifiant des attributs de propriété différents.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-168">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="2a0f9-169">Par exemple, vous pouvez dessiner un rectangle qui a des angles arrondis de 30% de la plus petite dimension du rectangle **en spécifiant** la valeur de la fonction de taille de ligne (« 0,3 »), la remplir avec le jaune en spécifiant **FillColor**= « Yellow » et lui attribuer un contour rouge à 2 points en spécifiant **StrokeColor**= "Red" **StrokeWeight**= "2pt</span><span class="sxs-lookup"><span data-stu-id="2a0f9-169">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 octets)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="2a0f9-171">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="2a0f9-171">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="2a0f9-172">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="2a0f9-173">line</span><span class="sxs-lookup"><span data-stu-id="2a0f9-173">line</span></span>

<span data-ttu-id="2a0f9-174">Vous pouvez utiliser l' `<line>` élément pour créer une ligne droite.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-174">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="2a0f9-175">Vous pouvez ensuite personnaliser la ligne en spécifiant des attributs de propriété différents.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-175">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="2a0f9-176">Par exemple, vous pouvez dessiner une ligne horizontale en spécifiant from = "20 points, 20 points" **to**= "100pt, 20 points", puis en la définissant **à** 2 points et en rouge en spécifiant **StrokeColor**= "Red" **StrokeWeight**= "2pt", comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-176">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 octets)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="2a0f9-178">Vous pouvez dessiner une ligne verticale ou diagonale en spécifiant simplement des valeurs différentes pour les attributs **de propriété from** et **to** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-178">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 octets)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="2a0f9-180">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="2a0f9-180">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="2a0f9-181">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-181">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="2a0f9-182">polyligne</span><span class="sxs-lookup"><span data-stu-id="2a0f9-182">polyline</span></span>

<span data-ttu-id="2a0f9-183">Vous pouvez utiliser l' `<polyline>` élément pour définir des formes qui sont créées à partir de segments de ligne connectés.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-183">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="2a0f9-184">Vous pouvez ensuite personnaliser la forme en spécifiant des attributs de propriété différents.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-184">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="2a0f9-185">Par exemple, pour dessiner la forme illustrée dans l’image suivante, vous pouvez taper la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-185">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 octets)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="2a0f9-187">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="2a0f9-187">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="2a0f9-188">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-188">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="2a0f9-189">courbe</span><span class="sxs-lookup"><span data-stu-id="2a0f9-189">curve</span></span>

<span data-ttu-id="2a0f9-190">Vous pouvez utiliser l' `<curve>` élément pour dessiner une courbe de Bézier cubique.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-190">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="2a0f9-191">Vous pouvez ensuite personnaliser la courbe en spécifiant des attributs de propriété différents.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-191">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="2a0f9-192">Par exemple, pour dessiner une courbe comme indiqué dans l’image suivante, vous pouvez taper la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-192">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 octets)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="2a0f9-194">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="2a0f9-194">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="2a0f9-195">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="2a0f9-196">arc</span><span class="sxs-lookup"><span data-stu-id="2a0f9-196">arc</span></span>

<span data-ttu-id="2a0f9-197">Vous pouvez utiliser l' `<arc>` élément pour dessiner un arc qui est défini en tant que segment d’un ovale.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-197">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="2a0f9-198">L’arc est défini par l’intersection de l’ovale avec les vecteurs RADIUS de début et de fin, en fonction des angles.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-198">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="2a0f9-199">Les angles sont calculés à l’aide des propriétés d’un cercle (largeur égale à la hauteur), puis mis à l’échelle de anisotropically à la largeur et à la hauteur souhaitées.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-199">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="2a0f9-200">Par exemple, vous pouvez dessiner un arc qui démarre à 0 degrés et se termine à 90 degrés en spécifiant **startAngle**= "0" **endangle**= "90", comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-200">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 octets)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="2a0f9-202">Vous pouvez modifier l’arc en spécifiant des valeurs **startAngle** et **endAngle** différentes, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="2a0f9-202">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 octets)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 octets)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="2a0f9-205">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="2a0f9-205">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="2a0f9-206">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="2a0f9-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="2a0f9-207">Résumé</span><span class="sxs-lookup"><span data-stu-id="2a0f9-207">Summary</span></span>

<span data-ttu-id="2a0f9-208">Vous pouvez utiliser des éléments prédéfinis VML tels que `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` et `<arc>` pour dessiner facilement des graphiques sur une page Web, puis personnaliser ces graphiques en modifiant simplement leurs attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="2a0f9-208">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 