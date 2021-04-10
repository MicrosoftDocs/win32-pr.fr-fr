---
title: Regroupement de formes
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Atelier Web, regroupement de formes
- conception de pages Web, regroupement de formes
- Langage VML (VML), regroupement de formes
- VML (langage VML), regrouper des formes
- graphiques vectoriels, grouper des formes
- Formes VML, regroupement
- regroupement de formes
- Langage VML (VML), élément de groupe
- VML (langage VML), élément de groupe
- Vector Graphics, Group, élément
- élément de groupe
- Éléments VML, groupe
- Langage VML (VML), espace de coordonnées local
- VML (langage VML), espace de coordonnées local
- graphiques vectoriels, espace de coordonnées local
- espace de coordonnées local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031758"
---
# <a name="grouping-shapes"></a><span data-ttu-id="cb88c-120">Regroupement de formes</span><span class="sxs-lookup"><span data-stu-id="cb88c-120">Grouping Shapes</span></span>

<span data-ttu-id="cb88c-121">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cb88c-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cb88c-122">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cb88c-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cb88c-123">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="cb88c-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cb88c-124">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="cb88c-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cb88c-125">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cb88c-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cb88c-126">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cb88c-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cb88c-127">Comme vous l’avez appris, vous pouvez facilement dessiner des formes individuelles à l’aide de VML.</span><span class="sxs-lookup"><span data-stu-id="cb88c-127">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="cb88c-128">Dans cette section, nous allons expliquer les avantages du regroupement de formes et la façon de regrouper des formes.</span><span class="sxs-lookup"><span data-stu-id="cb88c-128">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="cb88c-129">Si vous aviez de nombreuses formes qui devaient être mises à l’échelle, déplacées ou pivotées ensemble, vous pouvez trouver fastidieux de définir les attributs individuellement pour chaque forme.</span><span class="sxs-lookup"><span data-stu-id="cb88c-129">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="cb88c-130">En outre, vous risquez d’obtenir des erreurs.</span><span class="sxs-lookup"><span data-stu-id="cb88c-130">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="cb88c-131">Il serait préférable de regrouper les formes, puis de définir les attributs de l’ensemble du groupe.</span><span class="sxs-lookup"><span data-stu-id="cb88c-131">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="cb88c-132">Dans VML, vous pouvez utiliser l' `<group>` élément pour regrouper de nombreuses formes afin qu’elles puissent être transformées en une seule unité.</span><span class="sxs-lookup"><span data-stu-id="cb88c-132">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="cb88c-133">Par exemple, comme indiqué dans la représentation VML suivante, vous pouvez facilement regrouper deux formes.</span><span class="sxs-lookup"><span data-stu-id="cb88c-133">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="cb88c-134">Lorsque les formes sont regroupées, elles utilisent l' [espace de coordonnées local](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) du groupe.</span><span class="sxs-lookup"><span data-stu-id="cb88c-134">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="cb88c-135">Par conséquent, les formes d’un groupe peuvent être mises à l’échelle et déplacées ensemble.</span><span class="sxs-lookup"><span data-stu-id="cb88c-135">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="cb88c-136">Vous verrez d’autres exemples dans la rubrique utiliser l’espace de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="cb88c-136">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="cb88c-137">À l’intérieur d’un groupe, vous pouvez avoir autant de formes ou de groupes que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="cb88c-137">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="cb88c-138">Lorsqu’un groupe est à l’intérieur d’un autre groupe, il est appelé « groupe imbriqué ».</span><span class="sxs-lookup"><span data-stu-id="cb88c-138">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="cb88c-139">Il n’existe aucune limitation quant aux niveaux d’imbrication.</span><span class="sxs-lookup"><span data-stu-id="cb88c-139">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="cb88c-140">Par exemple, les lignes suivantes illustrent un groupe imbriqué de 3 niveaux.</span><span class="sxs-lookup"><span data-stu-id="cb88c-140">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="cb88c-141">Shape3 et Shape4 sont dans GroupC.</span><span class="sxs-lookup"><span data-stu-id="cb88c-141">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="cb88c-142">Shape2 et GroupC sont dans GroupB.</span><span class="sxs-lookup"><span data-stu-id="cb88c-142">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="cb88c-143">Shape1 et GroupB se trouvent dans groupa.</span><span class="sxs-lookup"><span data-stu-id="cb88c-143">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="cb88c-144">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="cb88c-144">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="cb88c-145">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="cb88c-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="cb88c-146">Résumé</span><span class="sxs-lookup"><span data-stu-id="cb88c-146">Summary</span></span>

<span data-ttu-id="cb88c-147">Vous pouvez utiliser l' `<group>` élément pour regrouper de nombreuses formes afin qu’elles puissent être transformées en une seule unité.</span><span class="sxs-lookup"><span data-stu-id="cb88c-147">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 