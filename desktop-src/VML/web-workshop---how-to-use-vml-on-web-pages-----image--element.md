---
title: Utilisation de l’élément image
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Atelier Web, élément image
- conception de pages Web, élément image
- Langage VML (VML), élément image
- VML (langage VML), élément image
- graphismes vectoriels, élément image
- élément d’image
- Éléments VML, image
- Formes VML, élément image
- Langage VML (VML), attributs de propriété de rognage
- VML (langage VML), attributs de propriété de rognage
- graphiques vectoriels, attributs de propriété de rognage
- Formes VML, attributs de propriété de rognage
- attributs de propriété de rognage
- Langage VML (VML), attribut de propriété gain
- VML (langage VML), attribut de propriété gain
- graphiques vectoriels, attribut de propriété gain
- Formes VML, attribut de propriété gain
- propriété gain (attribut)
- Langage VML (VML), contraste
- VML (langage VML), contraste
- graphiques vectoriels, contraste
- Formes VML, contraste
- Langage VML (VML), attribut de propriété blacklevel
- VML (langage VML), attribut de propriété blacklevel
- Graphics Vector, attribut de propriété blacklevel
- Formes VML, attribut de propriété blacklevel
- attribut de propriété blacklevel
- Langage VML (VML), luminosité
- VML (langage VML), luminosité
- graphiques vectoriels, luminosité
- Formes VML, luminosité
- Langage VML (VML), attribut de propriété nuances de gris
- VML (langage VML), attribut de propriété de nuances de gris
- graphique vectoriel, attribut de propriété nuances de gris
- Formes VML, attribut de propriété nuances de gris
- attribut de propriété nuances de gris
- Langage VML (VML), attribut de propriété gamma
- VML (langage VML), attribut de propriété gamma
- Graphics Vector, attribut de propriété gamma
- Formes VML, attribut de propriété gamma
- attribut de propriété gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508089"
---
# <a name="using-the-image-element"></a><span data-ttu-id="d2ff1-145">Utilisation de l’élément image</span><span class="sxs-lookup"><span data-stu-id="d2ff1-145">Using the Image Element</span></span>

<span data-ttu-id="d2ff1-146">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-146">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d2ff1-147">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-147">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d2ff1-148">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-148">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d2ff1-149">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-149">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d2ff1-150">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d2ff1-150">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d2ff1-151">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d2ff1-151">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d2ff1-152">Utilisation de `<image>`</span><span class="sxs-lookup"><span data-stu-id="d2ff1-152">Using `<image>`</span></span>

<span data-ttu-id="d2ff1-153">Dans cette rubrique, nous allons vous montrer comment utiliser l' `<image>` élément pour afficher des images avec divers effets spéciaux.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-153">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="d2ff1-154">Si vous souhaitez afficher une image qui a été chargée à partir d’une source externe, vous devez généralement utiliser l' `<img>` élément fourni en HTML, puis pointer l’attribut de propriété **src** vers l’emplacement du fichier image.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-154">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="d2ff1-155">Vous pouvez également utiliser l' `<image>` élément fourni dans Vml.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-155">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="d2ff1-156">Lorsque vous utilisez l' `<image>` élément, vous pouvez créer un seul fichier image, puis afficher l’image différemment en modifiant les attributs de propriété de l' `<image>` élément.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-156">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="d2ff1-157">En outre, l' `<image>` élément fournit plusieurs effets spéciaux que vous ne pouvez pas effectuer en utilisant simplement l' `<img>` élément HTML, tel que [rognage](#crop), [contraste](#contrast), [luminosité](#brightness), [gamma](#gamma)et [nuances de gris](#grayscale).</span><span class="sxs-lookup"><span data-stu-id="d2ff1-157">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="d2ff1-158">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="d2ff1-158">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="d2ff1-159">coup</span><span class="sxs-lookup"><span data-stu-id="d2ff1-159">crop</span></span>

<span data-ttu-id="d2ff1-160">Vous pouvez utiliser les attributs de propriété **CropBottom**, **CropTop**, **CropLeft** et **CropRight** de l' `<image>` élément pour afficher différentes images rognées à partir du même fichier image.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-160">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="d2ff1-161">La valeur de ces attributs de rognage représente le pourcentage réduit à partir du bord de l’image.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-161">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="d2ff1-162">La valeur peut être n’importe quel nombre compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-162">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="d2ff1-163">Par défaut, la valeur est définie sur 0, ce qui indique l’absence de rognage à partir du bord.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-163">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="d2ff1-164">La valeur 0,1 indique un rognage de 10 pour cent par rapport à la limite, la valeur 0,15 indique un rognage de 15 pour cent à partir du bord, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-164">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="d2ff1-165">Par exemple, pour afficher cinq images rognées du même fichier image, vous pouvez utiliser l' `<image>` élément et spécifier différentes valeurs de rognage, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="d2ff1-165">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image1 \-2.jpg (1969 octets)](images/image1-2.jpg)![image1 \-3.jpg (1148 octets)](images/image1-3.jpg)![image1 \-4.jpg (1686 octets)](images/image1-4.jpg)![image1 \-5.jpg (1364 octets)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="d2ff1-171">La première image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , n’a pas de valeur de rognage.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-171">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="d2ff1-172">Par conséquent, 100% de l’image d’origine s’affiche à une taille de 100 points par 80 points.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-172">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="d2ff1-173">La deuxième image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , a des valeurs de rognage.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-173">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="d2ff1-174">`cropbottom="0.2"` indique que 20 pour cent de l’image seront rognés du bas ; `cropright="0.15"` indique que 15% de l’image seront rognés du bord droit.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-174">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="d2ff1-175">L’image restante est ensuite affichée à une taille de 85 points de 64 points.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-175">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="d2ff1-176">De même, les troisième, quatrième et cinquième images ont des valeurs de rognage.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-176">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="d2ff1-177">L’image d’origine est rognée en fonction des valeurs de rognage et est ensuite affichée en fonction de la valeur de largeur et de hauteur.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-177">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="d2ff1-178">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="d2ff1-178">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="d2ff1-179">élevé</span><span class="sxs-lookup"><span data-stu-id="d2ff1-179">contrast</span></span>

<span data-ttu-id="d2ff1-180">Vous pouvez utiliser l’attribut de propriété **gain** de l' `<image>` élément pour afficher les différentes images qui ont des paramètres de contraste différents.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-180">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="d2ff1-181">La valeur de l’attribut de propriété **gain** peut être n’importe quel nombre.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-181">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="d2ff1-182">Par défaut, la valeur est 1, ce qui indique l’utilisation du même contraste que l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-182">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="d2ff1-183">La valeur 0 indique aucun contraste.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-183">The value 0 indicates no contrast.</span></span> <span data-ttu-id="d2ff1-184">Plus le nombre est élevé, plus le contraste est élevé.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-184">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="d2ff1-185">Par exemple, pour afficher cinq images avec différents paramètres de contraste, vous pouvez utiliser l' `<image>` élément et définir une valeur différente pour l’attribut de propriété **gain** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="d2ff1-185">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image2 \-2.jpg (270 octets)](images/image2-2.jpg)![image2 \-3.jpg (1919 octets)](images/image2-3.jpg)![image2 \-4.jpg (3143 octets)](images/image2-4.jpg)![image2 \-5.jpg (1724 octets)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="d2ff1-191">Lorsque l’attribut de propriété **gain** a la valeur 0, l’image entière est grisée, car il n’y a aucun contraste.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-191">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="d2ff1-192">Le contraste est plus perceptible lorsque l’attribut de propriété **gain** a la valeur 3 que lorsqu’il est défini sur 0,5.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-192">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="d2ff1-193">Le contraste est inversé lorsque l’attribut de propriété **gain** est défini sur une valeur négative telle que-0,4.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-193">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="d2ff1-194">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="d2ff1-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="d2ff1-195">luminosité</span><span class="sxs-lookup"><span data-stu-id="d2ff1-195">brightness</span></span>

<span data-ttu-id="d2ff1-196">Vous pouvez utiliser l’attribut de propriété **blacklevel** de l' `<image>` élément pour afficher les différentes images qui ont des paramètres de luminosité différents.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-196">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="d2ff1-197">La valeur de l’attribut de propriété **blacklevel** peut être n’importe quelle valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-197">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="d2ff1-198">Par défaut, la valeur est 0, ce qui indique que le niveau de luminosité dans l’image d’origine est préservé.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-198">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="d2ff1-199">La valeur 1 indique le niveau de luminosité le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-199">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="d2ff1-200">Par exemple, pour afficher cinq images qui ont des paramètres de luminosité différents, vous pouvez utiliser l' `<image>` élément et définir une valeur différente pour l’attribut de propriété **blacklevel** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="d2ff1-200">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image3 \-2.jpg (2579 octets)](images/image3-2.jpg)![image3 \-3.jpg (2330 octets)](images/image3-3.jpg)![image3 \-4.jpg (2727 octets)](images/image3-4.jpg)![image3 \-5.jpg (2435 octets)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="d2ff1-206">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="d2ff1-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="d2ff1-207">nuances de gris</span><span class="sxs-lookup"><span data-stu-id="d2ff1-207">grayscale</span></span>

<span data-ttu-id="d2ff1-208">Vous pouvez utiliser l’attribut de propriété **nuances de gris** de l' `<image>` élément pour afficher des images avec ou sans nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-208">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="d2ff1-209">La valeur de l’attribut de propriété **nuances de gris** peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-209">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="d2ff1-210">Par défaut, la valeur est définie sur false afin que l’image s’affiche en couleur.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-210">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="d2ff1-211">Si la valeur est définie sur true, l’image sera affichée en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-211">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="d2ff1-212">Par exemple, comme indiqué dans l’image suivante, la première image utilise le paramètre par défaut (false) de l’attribut nuances de gris ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="d2ff1-212">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="d2ff1-213">Par conséquent, l’image est affichée en couleur.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-213">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="d2ff1-214">La deuxième image affecte la valeur true à l’attribut nuances de gris ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="d2ff1-214">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="d2ff1-215">Par conséquent, l’image est affichée en nuances de gris, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="d2ff1-215">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image4 \-2.jpg (2138 octets)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="d2ff1-218">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="d2ff1-218">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="d2ff1-219">gamma</span><span class="sxs-lookup"><span data-stu-id="d2ff1-219">gamma</span></span>

<span data-ttu-id="d2ff1-220">Vous pouvez utiliser l’attribut de propriété **gamma** de l' `<image>` élément pour afficher les images qui ont des paramètres gamma différents.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-220">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="d2ff1-221">La valeur de l’attribut de propriété gamma peut être n’importe quelle valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-221">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="d2ff1-222">Par défaut, la valeur est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="d2ff1-222">By default, the value is set to 1.</span></span>

<span data-ttu-id="d2ff1-223">Par exemple, pour afficher trois images qui ont des paramètres gamma différents, vous pouvez utiliser l' `<image>` élément et définir une valeur différente de l’attribut de propriété **gamma** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="d2ff1-223">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 octets)](images/image5-1.jpg)![image5 \-2.jpg (2729 octets)](images/image5-2.jpg)![image5 \-3.jpg (2726 octets)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="d2ff1-227">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="d2ff1-227">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 