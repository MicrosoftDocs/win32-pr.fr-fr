---
title: Utilisation de l’espace de coordonnées local
description: Utilisation de l’espace de coordonnées local
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Atelier Web, espace de coordonnées local
- conception de pages Web, espace de coordonnées local
- Langage VML (VML), espace de coordonnées local
- VML (langage VML), espace de coordonnées local
- graphiques vectoriels, espace de coordonnées local
- espace de coordonnées local
- Formes VML, espace de coordonnées local
- Langage VML (VML), regroupement de formes
- VML (langage VML), regrouper des formes
- graphiques vectoriels, grouper des formes
- Formes VML, regroupement
- regroupement de formes
- Langage VML (VML), mise à l’échelle des formes
- VML (langage VML), mise à l’échelle des formes
- graphiques vectoriels, mise à l’échelle des formes
- Formes VML, mise à l’échelle
- mise à l’échelle des formes
- Langage VML (VML), formes de dimensionnement
- VML (langage VML), formes de redimensionnement
- graphiques vectoriels, formes de dimensionnement
- Formes VML, redimensionnement
- dimensionnement des formes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729733"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="21949-125">Utilisation de l’espace de coordonnées local</span><span class="sxs-lookup"><span data-stu-id="21949-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="21949-126">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="21949-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="21949-127">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="21949-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="21949-128">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="21949-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="21949-129">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="21949-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="21949-130">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="21949-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="21949-131">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="21949-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="21949-132">Comme vous l’avez appris, vous pouvez spécifier les attributs de style de **largeur** et de **hauteur** pour définir la taille d’une zone conteneur dans laquelle le contenu d’une forme ou d’un groupe sera rendu.</span><span class="sxs-lookup"><span data-stu-id="21949-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="21949-133">Dans cette rubrique, nous allons expliquer l’espace de coordonnées local et la façon dont il est utilisé dans VML pour mettre à l’échelle des formes.</span><span class="sxs-lookup"><span data-stu-id="21949-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="21949-134">Si vous avez été invité à dessiner un rectangle de 1 pouce sur un morceau de papier de grille, la première chose à faire est de commencer (le point d’origine).</span><span class="sxs-lookup"><span data-stu-id="21949-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="21949-135">Ensuite, vous devez déterminer comment mapper un pouce aux cellules du papier de la grille (coordonnée).</span><span class="sxs-lookup"><span data-stu-id="21949-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="21949-136">De même, lorsque le contenu d’une forme ou d’un groupe est rendu à l’intérieur de sa zone conteneur sur une page Web, le point d’origine et la coordonnée doivent être définis.</span><span class="sxs-lookup"><span data-stu-id="21949-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="21949-137">VML fournit un espace de coordonnées local pour permettre à chaque forme ou groupe de définir son propre point et sa coordonnée d’origine.</span><span class="sxs-lookup"><span data-stu-id="21949-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="21949-138">Si vous ne spécifiez pas d’espace de coordonnées, celui par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="21949-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="21949-139">Par défaut, l’origine commence dans l’angle supérieur gauche de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="21949-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="21949-140">Par exemple, la représentation VML de l’ovale rouge illustré ci-dessous ne spécifie pas les attributs de propriété **coordsize** et **coordorigin** .</span><span class="sxs-lookup"><span data-stu-id="21949-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="21949-141">Par conséquent, un espace de coordonnées local par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="21949-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="21949-142">La taille de l’ovale est de 100 points (largeur) par 75 points (hauteur).</span><span class="sxs-lookup"><span data-stu-id="21949-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="21949-143">Vous pouvez redimensionner l’ovale en spécifiant une largeur ou une hauteur différente, comme vous l’avez appris dans la rubrique mettre à l' [échelle les formes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .</span><span class="sxs-lookup"><span data-stu-id="21949-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 octets)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="21949-145">Lorsque la forme devient plus complexe, ou lorsque vous souhaitez regrouper plusieurs formes et les mettre à l’échelle, vous devez utiliser la fonctionnalité d’espace de coordonnées locale fournie dans VML.</span><span class="sxs-lookup"><span data-stu-id="21949-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="21949-146">Pour chaque forme ou groupe, vous pouvez utiliser les attributs de propriété **coordsize** et **coordorigin** pour définir l’espace de coordonnées local de la forme ou du groupe.</span><span class="sxs-lookup"><span data-stu-id="21949-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="21949-147">L’attribut **coordsize** spécifie le nombre d’unités le long de la largeur et la hauteur de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="21949-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="21949-148">L’attribut **coordorigin** définit la coordonnée dans l’angle supérieur gauche de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="21949-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="21949-149">Toutes les informations relatives à la position (telles que la largeur, la hauteur, la gauche, le haut, le chemin d’accès, etc.) sont exprimées en termes d’unité dans l’espace de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="21949-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="21949-150">Par exemple, comme indiqué dans la représentation VML suivante, `width: 100pt; height: 100pt;` définit la taille de la zone conteneur pour que la forme soit 100 points de 100 points.</span><span class="sxs-lookup"><span data-stu-id="21949-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 octets)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="21949-152">`coordsize="21600,21600"` définit la taille de l’espace de coordonnées local pour la forme sur 21600 unités par 21600 unités.</span><span class="sxs-lookup"><span data-stu-id="21949-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="21949-153">Par conséquent, une unité dans l’espace de coordonnées local est équivalente au point 1/216.</span><span class="sxs-lookup"><span data-stu-id="21949-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="21949-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` définit le contour de la forme sous forme de losange.</span><span class="sxs-lookup"><span data-stu-id="21949-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="21949-155">Comme nous l’avons appris, toutes les informations relatives à la position (telles que la largeur, la hauteur, la gauche, le haut, le chemin d’accès, etc.) sont exprimées en termes d’unité dans l’espace de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="21949-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="21949-156">Par conséquent, 10800 dans le `<path>` signifie 10800 unités, ce qui équivaut à 50 points.</span><span class="sxs-lookup"><span data-stu-id="21949-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="21949-157">Lorsque vous souhaitez redimensionner cette forme de losange, il vous suffit de spécifier une largeur ou une hauteur différente. vous n’êtes pas obligé de modifier une valeur dans le `<path>` .</span><span class="sxs-lookup"><span data-stu-id="21949-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="21949-158">Pour cette forme complexe, si vous n’avez pas utilisé la fonctionnalité espace de coordonnées local, vous devez modifier chaque valeur dans le `<path>` chaque fois que vous souhaitez la redimensionner.</span><span class="sxs-lookup"><span data-stu-id="21949-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="21949-159">Par exemple, vous pouvez mettre à l’échelle la forme en losange en spécifiant simplement une largeur ou une hauteur différente, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="21949-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 octets)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="21949-161">Vous pouvez également utiliser l’espace de coordonnées local dans l' `<group>` élément afin que le contenu de toutes les formes dans le groupe soit mis à l’échelle ensemble en fonction de la même coordonnée.</span><span class="sxs-lookup"><span data-stu-id="21949-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="21949-162">Ensuite, chaque fois que vous souhaitez mettre à l’échelle ou déplacer un groupe de formes, modifiez simplement la largeur et la hauteur, ou les paramètres **coordsize** et **coordorigin** du groupe.</span><span class="sxs-lookup"><span data-stu-id="21949-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="21949-163">Par exemple, dans la représentation VML suivante, `<v:group style='... width:200pt;height:200pt;'>` définit la taille de la zone conteneur pour que le groupe soit 200 points de 200 points.</span><span class="sxs-lookup"><span data-stu-id="21949-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 octets)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="21949-165">`coordsize="1000,1000"` définit la taille de l’espace de coordonnées local pour que le groupe soit de 1000 unités par unité de 1000.</span><span class="sxs-lookup"><span data-stu-id="21949-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="21949-166">Par conséquent, 1 unité dans l’espace de coordonnées local est équivalente au point 1/5.</span><span class="sxs-lookup"><span data-stu-id="21949-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="21949-167">`coordorigin="-500,-500"` définit l’angle supérieur gauche de la zone conteneur sur « -500,-500 ».</span><span class="sxs-lookup"><span data-stu-id="21949-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="21949-168">Par conséquent, le système de coordonnées à l’intérieur de la zone conteneur est compris entre-500 et 500 le long de l’axe x, et-500 à 500 le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="21949-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="21949-169">En d’autres termes, le centre de la zone conteneur a la valeur « 0,0 ».</span><span class="sxs-lookup"><span data-stu-id="21949-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="21949-170">`<v:oval style='... width:400;height:300;'>` définit la taille de la zone conteneur pour l’ovale rouge sur 400 unités (largeur) par 300 unités (hauteur).</span><span class="sxs-lookup"><span data-stu-id="21949-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="21949-171">Étant donné qu’une unité dans l’espace de coordonnées local est équivalente au point 1/5, la taille de la zone conteneur pour l’ovale rouge est de 80 points (largeur) de 60 points (hauteur).</span><span class="sxs-lookup"><span data-stu-id="21949-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="21949-172">De même, la taille de la zone conteneur pour le roundRect vert est de 50 points (largeur) de 40 points (hauteur).</span><span class="sxs-lookup"><span data-stu-id="21949-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="21949-173">Lorsque vous souhaitez redimensionner l’ovale rouge et le roundRect vert, modifiez simplement `<v:group style='... width:200pt;height:200pt;'>` .</span><span class="sxs-lookup"><span data-stu-id="21949-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="21949-174">C’est-ce que vous n’avez pas besoin de modifier individuellement la taille des deux formes.</span><span class="sxs-lookup"><span data-stu-id="21949-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="21949-175">Par exemple, si vous remplacez `<v:group style='... width:200pt;height:200pt;'>` par `<v:group style='... width:300pt;height:300pt;'>` , les formes deviennent plus volumineuses, comme illustré dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="21949-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 octets)](images/cord4.gif)



<span data-ttu-id="21949-177">Vous remarquerez également que les formes se trouvent différemment.</span><span class="sxs-lookup"><span data-stu-id="21949-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="21949-178">Cela est dû au fait que les formes sont dessinées à partir de « 0, 0 », qui se trouve au centre de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="21949-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="21949-179">Étant donné que vous augmentez la taille de la zone conteneur, le centre de la zone conteneur est également déplacé.</span><span class="sxs-lookup"><span data-stu-id="21949-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="21949-180">Si vous remplacez `coordorigin="-500,-500"` par `coordorigin="0,0"` , comme indiqué dans l’image suivante, vous remarquerez que l’ovale rouge et le roundRect vert sont déplacés vers le nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="21949-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="21949-181">Cela est dû au fait que « 0, 0 » se trouve désormais dans l’angle supérieur gauche de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="21949-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 octets)](images/cord5.gif)



<span data-ttu-id="21949-183">Il est également important de noter que la zone conteneur n’établit pas de zone de découpage.</span><span class="sxs-lookup"><span data-stu-id="21949-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="21949-184">Les graphiques peuvent être dessinés en dehors des limites de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="21949-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="21949-185">La zone conteneur sert simplement à mapper l’espace de coordonnées local à l’espace de page.</span><span class="sxs-lookup"><span data-stu-id="21949-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="21949-186">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span><span class="sxs-lookup"><span data-stu-id="21949-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 