---
title: Utilisation de l’élément Typedeforme
description: Utilisation de l’élément Typedeforme
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Atelier Web, élément Typedeforme
- conception de pages Web, élément Typedeforme
- Langage VML (VML), élément Typedeforme
- VML (langage VML), élément Typedeforme
- Graphics Vector, élément Typedeforme
- élément Typedeforme
- Éléments VML, Typedeforme
- Formes VML, élément Typedeforme
- Langage VML (VML), définition des formes fréquemment utilisées
- VML (langage VML), définition des formes fréquemment utilisées
- graphiques vectoriels, définition des formes fréquemment utilisées
- définition des formes fréquemment utilisées
- Formes VML, définition fréquemment utilisées
- Langage VML (VML), instanciation de copies de formes
- VML (langage VML), instanciation de copies de formes
- graphiques vectoriels, instanciation de copies de formes
- instanciation de copies de formes
- Formes VML, instanciation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463594"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="bcc03-121">Utilisation de l’élément Typedeforme</span><span class="sxs-lookup"><span data-stu-id="bcc03-121">Using the Shapetype Element</span></span>

<span data-ttu-id="bcc03-122">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bcc03-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bcc03-123">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bcc03-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bcc03-124">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="bcc03-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bcc03-125">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="bcc03-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bcc03-126">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bcc03-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bcc03-127">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bcc03-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bcc03-128">Dans cette rubrique, nous allons vous montrer comment utiliser l' `<shapetype>` élément pour définir vos propres formes fréquemment utilisées, puis instancier ou créer des formes à partir du Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="bcc03-129">Si vous souhaitez dessiner de nombreuses formes qui ont des propriétés identiques ou similaires, il serait fastidieux de taper les mêmes attributs de propriété pour chaque forme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="bcc03-130">VML fournit l' `<shapetype>` élément afin que vous puissiez définir un prototype de forme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="bcc03-131">Vous pouvez ensuite utiliser l' `<shape>` élément pour instancier de nombreuses copies de formes à partir du même Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="bcc03-132">Vous pouvez suivre les trois étapes pour définir un Typedeforme, puis instancier une forme à partir du Typedeforme :</span><span class="sxs-lookup"><span data-stu-id="bcc03-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="bcc03-133">Tapez un `<shapetype>` élément et attribuez-lui un nom en spécifiant l’attribut ID.</span><span class="sxs-lookup"><span data-stu-id="bcc03-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="bcc03-134">Décrivez le Typedeforme à l’aide de ses attributs ou de ses sous-éléments de propriété.</span><span class="sxs-lookup"><span data-stu-id="bcc03-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="bcc03-135">Instanciez une forme en tapant un `<shape>` élément et faites référence à l’attribut de type de la forme à l’attribut ID de Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="bcc03-136">Par exemple, vous tapez les lignes suivantes pour créer un Typedeforme nommé « MyShape » :</span><span class="sxs-lookup"><span data-stu-id="bcc03-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="bcc03-137">Ensuite, vous modifiez le format Typedeforme en définissant des attributs de propriété, tels que `fillcolor="red" strokecolor="blue"` .</span><span class="sxs-lookup"><span data-stu-id="bcc03-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="bcc03-138">Vous pouvez aussi utiliser des sous-éléments à l’intérieur de Typedeforme, tels que `<path>` , `<fill>` , `<stroke>` (nous parlerons de ces sous-éléments dans les rubriques ultérieures).</span><span class="sxs-lookup"><span data-stu-id="bcc03-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="bcc03-139">Ensuite, vous instanciez une forme à partir du « MyShape » Typedeforme en spécifiant `type="#MyShape"` , comme illustré dans la représentation VML suivante.</span><span class="sxs-lookup"><span data-stu-id="bcc03-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="bcc03-140">Cette forme hérite de toutes les propriétés de la « MyShape » de Typedeforme et s’affiche dans sa zone conteneur à une taille de 100 par 80.</span><span class="sxs-lookup"><span data-stu-id="bcc03-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="bcc03-141">Vous pouvez instancier une autre forme à partir du « MyShape » de Typedeforme en spécifiant `type="#MyShape"` et en substituant certaines propriétés, telles que `fillcolor="maroon"` , comme indiqué dans la représentation VML suivante.</span><span class="sxs-lookup"><span data-stu-id="bcc03-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="bcc03-142">Cette forme hérite de toutes les propriétés de la « MyShape » de Typedeforme, à l’exception de la propriété FillColor, et s’affiche dans sa zone conteneur à une taille de 70 par 90.</span><span class="sxs-lookup"><span data-stu-id="bcc03-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="bcc03-143">Voici la représentation VML complète de l’exemple précédent :</span><span class="sxs-lookup"><span data-stu-id="bcc03-143">Here is the complete VML representation for the preceding example:</span></span>

![Type1 \-1.gif (477 octets)](images/type1-1.gif)![Type1 \-2.gif (471 octets)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="bcc03-146">Comme vous l’avez appris, quand une forme est instanciée à partir d’un Typedeforme, elle hérite de tous les attributs de propriété du Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="bcc03-147">Vous pouvez remplacer tout ou partie des attributs hérités en redéfinissant les attributs à l’intérieur de l' `<shape>` élément.</span><span class="sxs-lookup"><span data-stu-id="bcc03-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="bcc03-148">N’oubliez pas que l’héritage n’est qu’un seul niveau.</span><span class="sxs-lookup"><span data-stu-id="bcc03-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="bcc03-149">Cela est dû au fait que seul un `<shape>` élément peut référencer un `<shapetype>` élément.</span><span class="sxs-lookup"><span data-stu-id="bcc03-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="bcc03-150">Un `<shapetype>` élément ne peut pas faire référence à un autre `<shapetype>` élément.</span><span class="sxs-lookup"><span data-stu-id="bcc03-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="bcc03-151">En outre, un Typedeforme n’appartient à aucun groupe.</span><span class="sxs-lookup"><span data-stu-id="bcc03-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="bcc03-152">Par conséquent, l' `<shapetype>` élément peut apparaître de lui-même ou à l’intérieur d’un `<group>` élément.</span><span class="sxs-lookup"><span data-stu-id="bcc03-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="bcc03-153">Vous pouvez avoir de nombreuses formes dans différents groupes qui font référence à la même Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="bcc03-154">Si une unité Typedeforme apparaît à l’intérieur d’un groupe, une forme vivant dans un autre groupe peut toujours faire référence à ce Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="bcc03-155">Par exemple, dans la représentation VML suivante, Rect1 et Rect2 sont dans groupa, et Rect3 est dans GroupB.</span><span class="sxs-lookup"><span data-stu-id="bcc03-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="bcc03-156">Les trois rectangles sont instanciés à partir de MyShape Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="bcc03-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="bcc03-157">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span><span class="sxs-lookup"><span data-stu-id="bcc03-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 