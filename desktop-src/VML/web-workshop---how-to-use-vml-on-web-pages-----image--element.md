---
title: Utilisation de l’élément image
description: Cet article décrit l’utilisation de l’élément image dans VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
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
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407802"
---
# <a name="using-the-image-element"></a><span data-ttu-id="0fbb4-144">Utilisation de l’élément image</span><span class="sxs-lookup"><span data-stu-id="0fbb4-144">Using the Image Element</span></span>

<span data-ttu-id="0fbb4-145">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0fbb4-146">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0fbb4-147">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0fbb4-148">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0fbb4-149">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0fbb4-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0fbb4-150">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0fbb4-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0fbb4-151">Utilisation de `<image>`</span><span class="sxs-lookup"><span data-stu-id="0fbb4-151">Using `<image>`</span></span>

<span data-ttu-id="0fbb4-152">Dans cette rubrique, nous allons vous montrer comment utiliser l' `<image>` élément pour afficher des images avec divers effets spéciaux.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="0fbb4-153">Si vous souhaitez afficher une image qui a été chargée à partir d’une source externe, vous devez généralement utiliser l' `<img>` élément fourni en HTML, puis pointer l’attribut de propriété **src** vers l’emplacement du fichier image.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="0fbb4-154">Vous pouvez également utiliser l' `<image>` élément fourni dans Vml.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="0fbb4-155">Lorsque vous utilisez l' `<image>` élément, vous pouvez créer un seul fichier image, puis afficher l’image différemment en modifiant les attributs de propriété de l' `<image>` élément.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="0fbb4-156">En outre, l' `<image>` élément fournit plusieurs effets spéciaux que vous ne pouvez pas effectuer en utilisant simplement l' `<img>` élément HTML, tel que [rognage](#crop), [contraste](#contrast), [luminosité](#brightness), [gamma](#gamma)et [nuances de gris](#grayscale).</span><span class="sxs-lookup"><span data-stu-id="0fbb4-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="0fbb4-157">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0fbb4-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="0fbb4-158">coup</span><span class="sxs-lookup"><span data-stu-id="0fbb4-158">crop</span></span>

<span data-ttu-id="0fbb4-159">Vous pouvez utiliser les attributs de propriété **CropBottom**, **CropTop**, **CropLeft** et **CropRight** de l' `<image>` élément pour afficher différentes images rognées à partir du même fichier image.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="0fbb4-160">La valeur de ces attributs de rognage représente le pourcentage réduit à partir du bord de l’image.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="0fbb4-161">La valeur peut être n’importe quel nombre compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="0fbb4-162">Par défaut, la valeur est définie sur 0, ce qui indique l’absence de rognage à partir du bord.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="0fbb4-163">La valeur 0,1 indique un rognage de 10 pour cent par rapport à la limite, la valeur 0,15 indique un rognage de 15 pour cent à partir du bord, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="0fbb4-164">Par exemple, pour afficher cinq images rognées du même fichier image, vous pouvez utiliser l' `<image>` élément et spécifier différentes valeurs de rognage, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0fbb4-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

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





<span data-ttu-id="0fbb4-170">La première image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , n’a pas de valeur de rognage.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="0fbb4-171">Par conséquent, 100% de l’image d’origine s’affiche à une taille de 100 points par 80 points.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="0fbb4-172">La deuxième image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , a des valeurs de rognage.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="0fbb4-173">`cropbottom="0.2"` indique que 20 pour cent de l’image seront rognés du bas ; `cropright="0.15"` indique que 15% de l’image seront rognés du bord droit.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="0fbb4-174">L’image restante est ensuite affichée à une taille de 85 points de 64 points.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="0fbb4-175">De même, les troisième, quatrième et cinquième images ont des valeurs de rognage.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="0fbb4-176">L’image d’origine est rognée en fonction des valeurs de rognage et est ensuite affichée en fonction de la valeur de largeur et de hauteur.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="0fbb4-177">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0fbb4-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="0fbb4-178">élevé</span><span class="sxs-lookup"><span data-stu-id="0fbb4-178">contrast</span></span>

<span data-ttu-id="0fbb4-179">Vous pouvez utiliser l’attribut de propriété **gain** de l' `<image>` élément pour afficher les différentes images qui ont des paramètres de contraste différents.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="0fbb4-180">La valeur de l’attribut de propriété **gain** peut être n’importe quel nombre.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="0fbb4-181">Par défaut, la valeur est 1, ce qui indique l’utilisation du même contraste que l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="0fbb4-182">La valeur 0 indique aucun contraste.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="0fbb4-183">Plus le nombre est élevé, plus le contraste est élevé.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="0fbb4-184">Par exemple, pour afficher cinq images avec différents paramètres de contraste, vous pouvez utiliser l' `<image>` élément et définir une valeur différente pour l’attribut de propriété **gain** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0fbb4-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image2 \-2.jpg (270 octets)](images/image2-2.jpg)![image2 \-3.jpg (1919 octets)](images/image2-3.jpg)![image2 \-4.jpg (3143 octets)](images/image2-4.jpg)![image2 \-5.jpg (1724 octets)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="0fbb4-190">Lorsque l’attribut de propriété **gain** a la valeur 0, l’image entière est grisée, car il n’y a aucun contraste.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="0fbb4-191">Le contraste est plus perceptible lorsque l’attribut de propriété **gain** a la valeur 3 que lorsqu’il est défini sur 0,5.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="0fbb4-192">Le contraste est inversé lorsque l’attribut de propriété **gain** est défini sur une valeur négative telle que-0,4.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="0fbb4-193">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0fbb4-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="0fbb4-194">luminosité</span><span class="sxs-lookup"><span data-stu-id="0fbb4-194">brightness</span></span>

<span data-ttu-id="0fbb4-195">Vous pouvez utiliser l’attribut de propriété **blacklevel** de l' `<image>` élément pour afficher les différentes images qui ont des paramètres de luminosité différents.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="0fbb4-196">La valeur de l’attribut de propriété **blacklevel** peut être n’importe quelle valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="0fbb4-197">Par défaut, la valeur est 0, ce qui indique que le niveau de luminosité dans l’image d’origine est préservé.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="0fbb4-198">La valeur 1 indique le niveau de luminosité le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="0fbb4-199">Par exemple, pour afficher cinq images qui ont des paramètres de luminosité différents, vous pouvez utiliser l' `<image>` élément et définir une valeur différente pour l’attribut de propriété **blacklevel** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0fbb4-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image3 \-2.jpg (2579 octets)](images/image3-2.jpg)![image3 \-3.jpg (2330 octets)](images/image3-3.jpg)![image3 \-4.jpg (2727 octets)](images/image3-4.jpg)![image3 \-5.jpg (2435 octets)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="0fbb4-205">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0fbb4-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="0fbb4-206">nuances de gris</span><span class="sxs-lookup"><span data-stu-id="0fbb4-206">grayscale</span></span>

<span data-ttu-id="0fbb4-207">Vous pouvez utiliser l’attribut de propriété **nuances de gris** de l' `<image>` élément pour afficher des images avec ou sans nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="0fbb4-208">La valeur de l’attribut de propriété **nuances de gris** peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="0fbb4-209">Par défaut, la valeur est définie sur false afin que l’image s’affiche en couleur.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="0fbb4-210">Si la valeur est définie sur true, l’image sera affichée en nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="0fbb4-211">Par exemple, comme indiqué dans l’image suivante, la première image utilise le paramètre par défaut (false) de l’attribut nuances de gris ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="0fbb4-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="0fbb4-212">Par conséquent, l’image est affichée en couleur.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="0fbb4-213">La deuxième image affecte la valeur true à l’attribut nuances de gris ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="0fbb4-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="0fbb4-214">Par conséquent, l’image est affichée en nuances de gris, comme illustré dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0fbb4-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 octets)](images/image1.jpg)![image4 \-2.jpg (2138 octets)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="0fbb4-217">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="0fbb4-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="0fbb4-218">gamma</span><span class="sxs-lookup"><span data-stu-id="0fbb4-218">gamma</span></span>

<span data-ttu-id="0fbb4-219">Vous pouvez utiliser l’attribut de propriété **gamma** de l' `<image>` élément pour afficher les images qui ont des paramètres gamma différents.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="0fbb4-220">La valeur de l’attribut de propriété gamma peut être n’importe quelle valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="0fbb4-221">Par défaut, la valeur est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="0fbb4-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="0fbb4-222">Par exemple, pour afficher trois images qui ont des paramètres gamma différents, vous pouvez utiliser l' `<image>` élément et définir une valeur différente de l’attribut de propriété **gamma** , comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0fbb4-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 octets)](images/image5-1.jpg)![image5 \-2.jpg (2729 octets)](images/image5-2.jpg)![image5 \-3.jpg (2726 octets)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="0fbb4-226">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="0fbb4-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 