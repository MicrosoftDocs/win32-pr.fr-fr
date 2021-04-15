---
title: Dessin de formes de base
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Atelier Web, formes de dessin
- conception de pages Web, dessin de formes
- Langage VML (VML), dessins, formes
- VML (langage VML), formes de dessin
- graphiques vectoriels, formes de dessin
- dessiner des formes
- Formes VML, dessin
- Langage VML (VML), XML
- VML (langage VML), XML
- graphiques vectoriels, XML
- Langage VML (VML), CSS2
- VML (langage VML), CSS2
- graphiques vectoriels, CSS2
- Langage VML (VML), éléments
- VML (langage VML), éléments
- graphiques vectoriels, éléments
- Éléments VML, formes de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463591"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="c1c3a-121">Dessin de formes de base</span><span class="sxs-lookup"><span data-stu-id="c1c3a-121">Drawing Basic Shapes</span></span>

<span data-ttu-id="c1c3a-122">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c1c3a-123">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c1c3a-124">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c1c3a-125">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c1c3a-126">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c1c3a-127">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c1c3a-128">Dans cette rubrique, nous allons vous montrer combien il est facile de dessiner une forme à l’aide de VML.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-128">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="c1c3a-129">Pour créer un ovale rouge sur une page Web, comme illustré dans l’image suivante, vous pouvez dessiner l’ovale à l’aide d’un outil d’édition graphique, enregistrer votre dessin en tant que bitmap, puis insérer l’image bitmap sur votre page Web :</span><span class="sxs-lookup"><span data-stu-id="c1c3a-129">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 octets)](images/oval1.gif)

<span data-ttu-id="c1c3a-131">Vous pouvez également utiliser VML pour dessiner des graphiques.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-131">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="c1c3a-132">Dans l’exemple précédent, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web pour dessiner l’ovale rouge :</span><span class="sxs-lookup"><span data-stu-id="c1c3a-132">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="c1c3a-133">`<v:...>` et `</v:...>` sont les balises de début et de fin dans la [syntaxe XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="c1c3a-133">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="c1c3a-134">fournit des [informations CSS](#css-information).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-134">provides [CSS information](#css-information).</span></span> <span data-ttu-id="c1c3a-135">**Oval** et **FillColor**= "Red" sont des [éléments VML](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-135">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="c1c3a-136">Vous pouvez modifier les graphiques en modifiant simplement leurs attributs de propriété dans VML.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-136">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="c1c3a-137">Dans l’exemple précédent, si vous remplacez `fillcolor="red"` par `fillcolor="blue"` , comme indiqué dans la représentation VML suivante, le ovale rouge passe en bleu :</span><span class="sxs-lookup"><span data-stu-id="c1c3a-137">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="c1c3a-138">Les navigateurs qui prennent en charge le langage VML peuvent afficher et afficher les graphiques représentés dans VML sans avoir à télécharger des fichiers image distincts.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-138">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="c1c3a-139">La plupart des graphiques représentés dans VML sont rendus plus rapidement dans les navigateurs et nécessitent moins d’espace disque et le temps de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-139">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="c1c3a-140">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="c1c3a-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="c1c3a-141">Structure XML</span><span class="sxs-lookup"><span data-stu-id="c1c3a-141">XML Structure</span></span>

<span data-ttu-id="c1c3a-142">Le format VML est mis en forme en fonction des règles de Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-142">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="c1c3a-143">N’importe quel analyseur XML standard peut analyser le VML et transmettre les données résultantes à un processeur spécifique à VML.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-143">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="c1c3a-144">Pour permettre aux navigateurs de savoir comment transférer des données vers un processeur VML spécifique, vous devez taper des informations telles que les [espaces de noms](web-workshop---how-to-use-vml-on-web-pages----appendix.md) et les [objets personnalisés incorporés](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-144">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="c1c3a-145">Vous pouvez ensuite utiliser VML pour taper des graphiques dans la `<BODY>` région, comme vous l’avez fait dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-145">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="c1c3a-146">Le `"v:"` préfixe de chaque balise XML identifie la balise en tant que Vml.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-146">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="c1c3a-147">Le `"v:"` préfixe de la `<BODY>` région doit être cohérent avec `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="c1c3a-147">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="c1c3a-148">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="c1c3a-148">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="c1c3a-149">Informations CSS</span><span class="sxs-lookup"><span data-stu-id="c1c3a-149">CSS Information</span></span>

<span data-ttu-id="c1c3a-150">VML utilise [feuilles de style en cascade, niveau 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) pour déterminer la taille des graphiques et positionner les graphiques sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-150">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="c1c3a-151">Dans l’exemple précédent, nous avons spécifié la taille de l’ovale sous la forme de 100 points (largeur) de 75 points (hauteur) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="c1c3a-151">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="c1c3a-152">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="c1c3a-152">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="c1c3a-153">Éléments VML</span><span class="sxs-lookup"><span data-stu-id="c1c3a-153">VML Elements</span></span>

<span data-ttu-id="c1c3a-154">Dans l’exemple précédent, nous avons utilisé un élément prédéfini VML `<oval>` pour dessiner un ovale.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-154">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="c1c3a-155">Nous avons ensuite utilisé l’attribut de propriété **FillColor** de l' `<oval>` élément pour remplir l’ovale en rouge.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-155">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="c1c3a-156">En se basant sur les balises de [début, les balises de fin et les balises de Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) de la [spécification XML 1,0](https://www.w3.org/TR/REC-xml), les balises d’éléments vides peuvent être utilisées pour tout élément sans contenu.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-156">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="c1c3a-157">Par exemple, comme indiqué dans la représentation VML suivante, il n’y a aucun contenu (sous-élément) dans l' `<oval>` élément.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-157">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="c1c3a-158">(Notez que le **style** et **FillColor** sont les attributs de l' `<oval>` élément ; il ne s’agit pas de sous-éléments.)</span><span class="sxs-lookup"><span data-stu-id="c1c3a-158">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="c1c3a-159">Par conséquent, vous pouvez utiliser la balise d’élément vide, comme indiqué dans la représentation VML suivante, pour représenter la même chose que la ligne ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-159">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="c1c3a-160">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="c1c3a-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="c1c3a-161">Résumé</span><span class="sxs-lookup"><span data-stu-id="c1c3a-161">Summary</span></span>

<span data-ttu-id="c1c3a-162">Vous pouvez utiliser VML pour dessiner des graphiques sur une page Web, puis personnaliser ces graphiques en modifiant simplement leurs attributs de propriété.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-162">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="c1c3a-163">En outre, la plupart des graphiques représentés dans VML sont rendus plus rapidement dans les navigateurs et prennent moins de temps de téléchargement et d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="c1c3a-163">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 