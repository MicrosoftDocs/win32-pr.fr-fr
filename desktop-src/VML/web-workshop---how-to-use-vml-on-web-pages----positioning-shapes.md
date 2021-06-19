---
title: Positionnement des formes
description: Cet article décrit les formes de positionnement dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Atelier Web, positionnement des formes
- conception de pages Web, positionnement des formes
- Langage VML (VML), positionnement des formes
- VML (langage VML), positionnement des formes
- graphiques vectoriels, positionner des formes
- Formes VML, positionnement
- positionnement des formes
- Langage VML (VML), style de position statique
- VML (langage VML), style de position statique
- graphiques vectoriels, style de position statique
- style de position statique
- Langage VML (VML), style de position relative
- VML (langage VML), style de position relative
- graphiques vectoriels, style de position relative
- style de position relative
- Langage VML (VML), style de position absolue
- VML (langage VML), style de position absolue
- graphiques vectoriels, style de position absolue
- style de position absolue
- Langage VML (VML), style de position de l’index z
- VML (langage VML), style de position de l’index z
- graphiques vectoriels, style de position de l’index z
- style de position de l’index z
- Langage VML (VML), style de la position de rotation
- VML (langage VML), style de position de rotation
- graphiques vectoriels, style de position de rotation
- style de position de rotation
- Langage VML (VML), retourner le style de position
- VML (langage VML), retourner le style de position
- graphiques vectoriels, retourner le style de position
- retourner le style de position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407712"
---
# <a name="positioning-shapes"></a><span data-ttu-id="a7bdf-134">Positionnement des formes</span><span class="sxs-lookup"><span data-stu-id="a7bdf-134">Positioning Shapes</span></span>

<span data-ttu-id="a7bdf-135">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-135">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a7bdf-136">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-136">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a7bdf-137">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-137">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a7bdf-138">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-138">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a7bdf-139">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a7bdf-139">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a7bdf-140">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a7bdf-140">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a7bdf-141">Vous avez appris à dessiner et à colorier des formes sur une page Web à l’aide de VML.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-141">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="a7bdf-142">Dans cette rubrique, vous allez utiliser VML pour positionner les graphiques avec précision sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-142">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="a7bdf-143">VML utilise la même syntaxe que celle définie dans les sections [Model Model](https://www.w3.org/TR/PR-CSS2/box.mdl) et [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) de [CSS2](https://www.w3.org/TR/PR-CSS2/) pour positionner les formes sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-143">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="a7bdf-144">Vous pouvez utiliser [static](#static), [relative](#relative)ou [Absolute](#absolute) pour déterminer où se trouve le point de base sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-144">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="a7bdf-145">Vous pouvez ensuite utiliser les attributs de style **supérieur** et **gauche** pour spécifier le décalage à partir du point de base auquel la zone conteneur pour la forme est positionnée.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-145">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="a7bdf-146">Vous pouvez également utiliser [z-index](#z-index) pour spécifier l’ordre de plan des formes sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-146">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="a7bdf-147">En outre, VML fournit une [rotation](#rotation) et un [retournement](#flip) pour faire pivoter ou retourner des formes.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-147">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="a7bdf-148">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="a7bdf-148">In this topic:</span></span>

-   [<span data-ttu-id="a7bdf-149">static</span><span class="sxs-lookup"><span data-stu-id="a7bdf-149">static</span></span>](#static)
-   [<span data-ttu-id="a7bdf-150">relative</span><span class="sxs-lookup"><span data-stu-id="a7bdf-150">relative</span></span>](#relative)
-   [<span data-ttu-id="a7bdf-151">absolute</span><span class="sxs-lookup"><span data-stu-id="a7bdf-151">absolute</span></span>](#absolute)
-   [<span data-ttu-id="a7bdf-152">index z</span><span class="sxs-lookup"><span data-stu-id="a7bdf-152">z-index</span></span>](#z-index)
-   [<span data-ttu-id="a7bdf-153">CRIC</span><span class="sxs-lookup"><span data-stu-id="a7bdf-153">rotation</span></span>](#rotation)
-   [<span data-ttu-id="a7bdf-154">flip</span><span class="sxs-lookup"><span data-stu-id="a7bdf-154">flip</span></span>](#flip)
-   [<span data-ttu-id="a7bdf-155">Résumé</span><span class="sxs-lookup"><span data-stu-id="a7bdf-155">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="a7bdf-156">static</span><span class="sxs-lookup"><span data-stu-id="a7bdf-156">static</span></span>

<span data-ttu-id="a7bdf-157">Le style de position par défaut est static, ce qui indique aux navigateurs de positionner la forme au point actuel (le point de base) dans le déroulement du texte et d’ignorer les paramètres dans les attributs de style **supérieur** et **gauche** .</span><span class="sxs-lookup"><span data-stu-id="a7bdf-157">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="a7bdf-158">Par exemple, dans la représentation VML suivante, l’ovale rouge est positionné juste après le texte « début de la forme : », comme illustré dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="a7bdf-158">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![Shape1 \-ps.gif (2123 octets)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="a7bdf-160">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="a7bdf-161">relative</span><span class="sxs-lookup"><span data-stu-id="a7bdf-161">relative</span></span>

<span data-ttu-id="a7bdf-162">L’affectation de la valeur « relative » à l’attribut de style position vous permet de placer la zone conteneur avec un décalage à partir du point actuel (le point de base) dans le déroulement du texte.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-162">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="a7bdf-163">Le décalage est déterminé par les paramètres dans les attributs de style **supérieur** et **gauche** .</span><span class="sxs-lookup"><span data-stu-id="a7bdf-163">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="a7bdf-164">N’oubliez pas que la zone conteneur positionnée sur relative occupe de l’espace dans le texte.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-164">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="a7bdf-165">Par exemple, dans la représentation VML suivante, l’ovale rouge est positionné à 20 points à partir de la gauche et 10 points à partir du haut par rapport au point actuel dans le texte, comme illustré dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="a7bdf-165">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 octets)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="a7bdf-167">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-167">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="a7bdf-168">absolute</span><span class="sxs-lookup"><span data-stu-id="a7bdf-168">absolute</span></span>

<span data-ttu-id="a7bdf-169">La définition de l’attribut de style position sur « Absolute » vous permet de placer la zone conteneur sur une distance exacte de l’angle supérieur gauche (le point de base) de son élément parent (l’élément positionné qui contient la forme).</span><span class="sxs-lookup"><span data-stu-id="a7bdf-169">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="a7bdf-170">Sachez que la zone conteneur qui est positionnée comme absolue n’occupe pas de place dans le texte.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-170">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="a7bdf-171">Par exemple, dans la représentation VML suivante, l’ovale rouge est contenu dans l' `<body>` élément (la page Web entière); par conséquent, le point de base se trouve dans l’angle supérieur gauche de la page Web.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-171">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="a7bdf-172">La zone conteneur pour l’ovale est positionnée exactement à 20 points à partir de la gauche et de 10 points à partir du haut, par rapport à l’angle supérieur gauche de la page Web, comme illustré dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="a7bdf-172">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 octets)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="a7bdf-174">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-174">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="a7bdf-175">z-index</span><span class="sxs-lookup"><span data-stu-id="a7bdf-175">z-index</span></span>

<span data-ttu-id="a7bdf-176">Il est possible de positionner une forme qui chevauche une autre forme.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-176">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="a7bdf-177">Normalement, le graphique qui est listé en dernier dans le code HTML apparaît en haut.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-177">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="a7bdf-178">Dans VML, vous pouvez contrôler l’ordre de plan à l’aide de l’attribut de style **z-index** .</span><span class="sxs-lookup"><span data-stu-id="a7bdf-178">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="a7bdf-179">La valeur de cet attribut peut être zéro, un entier positif ou un entier négatif.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-179">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="a7bdf-180">Le graphique qui a une plus grande valeur d’index z est affiché en haut du graphique qui a une plus petite valeur d’index z.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-180">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="a7bdf-181">Lorsque les deux graphiques ont la même valeur z-index, le graphique qui est listé en dernier dans le code HTML apparaît en haut.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-181">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="a7bdf-182">Par exemple, dans la représentation VML suivante, l’ovale rouge s’affiche en haut du rectangle bleu.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-182">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="a7bdf-183">Cela est dû au fait que la valeur z-index de l’ovale rouge est supérieure à la valeur z-index du rectangle bleu.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-183">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 octets)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="a7bdf-185">Si vous modifiez l’index z, comme indiqué dans la représentation VML suivante, l’ovale rouge se déplacera en arrière-plan du rectangle bleu.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-185">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 octets)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="a7bdf-187">Si vous fournissez un entier négatif, vous pouvez utiliser z-index pour positionner les graphiques derrière le texte normal, comme indiqué dans la représentation VML suivante.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-187">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 octets)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="a7bdf-189">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="a7bdf-190">CRIC</span><span class="sxs-lookup"><span data-stu-id="a7bdf-190">rotation</span></span>

<span data-ttu-id="a7bdf-191">Vous pouvez utiliser l’attribut de style de **rotation** pour spécifier le nombre de degrés d’activation d’une forme sur son axe.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-191">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="a7bdf-192">Une valeur positive indique une rotation dans le sens des aiguilles d’une montre ; une valeur négative indique une rotation dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-192">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="a7bdf-193">Par exemple, si vous spécifiez **style**= '... rotation : 90 ', vous pouvez faire pivoter la forme de 90 degrés dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-193">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="a7bdf-194">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="a7bdf-195">flip</span><span class="sxs-lookup"><span data-stu-id="a7bdf-195">flip</span></span>

<span data-ttu-id="a7bdf-196">Vous pouvez utiliser l’attribut **Flip** style pour retourner une forme sur son axe x ou y, conformément au tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="a7bdf-196">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="a7bdf-197">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7bdf-197">Value</span></span> | <span data-ttu-id="a7bdf-198">Description</span><span class="sxs-lookup"><span data-stu-id="a7bdf-198">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="a7bdf-199">x</span><span class="sxs-lookup"><span data-stu-id="a7bdf-199">x</span></span>     | <span data-ttu-id="a7bdf-200">Retourner la forme pivotée autour de l’axe y (inversement x ordonnés)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-200">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="a7bdf-201">y</span><span class="sxs-lookup"><span data-stu-id="a7bdf-201">y</span></span>     | <span data-ttu-id="a7bdf-202">Retourner la forme pivotée autour de l’axe x (inverser les ordonnées y)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-202">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="a7bdf-203">X et y peuvent être spécifiés dans la propriété Flip.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-203">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="a7bdf-204">Par exemple, si vous tapez **style**= '... Flip : x y', vous allez retourner la forme sur ses axes x et y.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-204">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="a7bdf-205">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="a7bdf-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="a7bdf-206">Résumé</span><span class="sxs-lookup"><span data-stu-id="a7bdf-206">Summary</span></span>

<span data-ttu-id="a7bdf-207">En fonction de ce que vous avez appris, vous pouvez positionner précisément une forme sur une page Web en procédant comme suit :</span><span class="sxs-lookup"><span data-stu-id="a7bdf-207">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="a7bdf-208">Décidez où vous souhaitez que la forme apparaisse sur une page Web et la taille de la forme.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-208">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="a7bdf-209">Spécifiez **style**= 'position : relative (ou relative) 'pour déterminer le point de base.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-209">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="a7bdf-210">Utilisez **Left** et **Top** pour spécifier le décalage à partir du point de base.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-210">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="a7bdf-211">Utilisez la **largeur** et la **hauteur** pour spécifier la taille de la zone conteneur pour la forme.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-211">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="a7bdf-212">Utilisez **z-index** pour spécifier l’ordre de plan de la forme.</span><span class="sxs-lookup"><span data-stu-id="a7bdf-212">Use **z-index** to specify the z-order of the shape.</span></span>

 

 