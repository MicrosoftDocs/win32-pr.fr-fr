---
title: Utilisation de l’élément Path
description: Utilisation de l’élément Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Atelier Web, élément Path
- conception de pages Web, élément Path
- Langage VML (VML), élément Path
- VML (langage VML), élément Path
- Vector Graphics, élément Path
- élément Path
- Éléments VML, chemin d’accès
- Formes VML, élément Path
- Langage VML (VML), personnalisation des contours de forme
- VML (langage VML), personnalisation des contours de forme
- graphiques vectoriels, personnalisation des contours de forme
- Formes VML, personnalisation des plans
- personnalisation des contours de forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729749"
---
# <a name="using-the-path-element"></a><span data-ttu-id="0513d-116">Utilisation de l’élément Path</span><span class="sxs-lookup"><span data-stu-id="0513d-116">Using the Path Element</span></span>

<span data-ttu-id="0513d-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0513d-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0513d-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0513d-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0513d-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="0513d-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0513d-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="0513d-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0513d-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0513d-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0513d-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0513d-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0513d-123">Vous avez appris que vous pouvez utiliser les éléments de forme prédéfinis VML, tels que `<oval>` ,,,,, `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` et `<arc>` pour dessiner une forme.</span><span class="sxs-lookup"><span data-stu-id="0513d-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="0513d-124">Dans cette rubrique, nous allons vous montrer comment utiliser le `<path>` sous-élément pour personnaliser le contour d’une forme.</span><span class="sxs-lookup"><span data-stu-id="0513d-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="0513d-125">Vous pouvez placer le `<path>` sous-élément à l’intérieur de l' `<shape>` `<shapetype>` élément ou.</span><span class="sxs-lookup"><span data-stu-id="0513d-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="0513d-126">Vous pouvez ensuite utiliser les attributs de propriété du `<path>` sous-élément pour personnaliser le contour de la forme.</span><span class="sxs-lookup"><span data-stu-id="0513d-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="0513d-127">Par exemple, pour dessiner la forme personnalisée illustrée dans l’image suivante, vous pouvez utiliser le `<path>` sous-élément pour définir le contour de la forme, comme indiqué dans la représentation VML suivante :</span><span class="sxs-lookup"><span data-stu-id="0513d-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 octets)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="0513d-129">Les valeurs `m 8,65` indiquent que le dessin commence au point (8, 65).</span><span class="sxs-lookup"><span data-stu-id="0513d-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="0513d-130">Les valeurs `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indiquent qu’une ligne droite commence au point actuel (8, 65) et se termine au point donné (72, 65), qui devient le nouveau point actuel.</span><span class="sxs-lookup"><span data-stu-id="0513d-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="0513d-131">Une nouvelle ligne commence au point actuel (72, 65) et se termine au point donné, qui devient le nouveau point actuel, et ainsi de suite, jusqu’au point final (60, 100).</span><span class="sxs-lookup"><span data-stu-id="0513d-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="0513d-132">`x` indique que le chemin d’accès se fermera par une ligne droite qui commence au point actuel (60, 100) et se termine au point d’origine (8, 65).</span><span class="sxs-lookup"><span data-stu-id="0513d-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="0513d-133">`e` indique l’arrêt du dessin.</span><span class="sxs-lookup"><span data-stu-id="0513d-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="0513d-134">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span><span class="sxs-lookup"><span data-stu-id="0513d-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 