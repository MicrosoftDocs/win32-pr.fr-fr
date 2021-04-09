---
title: Utilisation de l’élément TextPath
description: Utilisation de l’élément TextPath
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- Atelier Web, élément TextPath
- conception de pages Web, élément TextPath
- Langage VML (VML), élément TextPath
- VML (langage VML), élément TextPath
- Graphics Vector, élément TextPath
- élément TextPath
- Éléments VML, TextPath
- Formes VML, élément TextPath
- Langage VML (VML), dessin de texte
- VML (langage VML), dessin de texte
- graphiques vectoriels, dessiner du texte VML
- dessiner du texte
- Formes VML, dessiner du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c032d14307dc07ec56911f4c5cc45a4c69664
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102264"
---
# <a name="using-the-textpath-element"></a><span data-ttu-id="8eb36-116">Utilisation de l’élément TextPath</span><span class="sxs-lookup"><span data-stu-id="8eb36-116">Using the Textpath Element</span></span>

<span data-ttu-id="8eb36-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8eb36-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8eb36-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8eb36-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8eb36-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="8eb36-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8eb36-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="8eb36-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8eb36-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8eb36-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8eb36-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8eb36-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8eb36-123">Dans cette rubrique, nous allons vous montrer comment utiliser l' `<textpath>` élément pour dessiner du texte avec différents styles.</span><span class="sxs-lookup"><span data-stu-id="8eb36-123">In this topic, we will illustrate how to use the `<textpath>` element to draw text with various styles.</span></span>

<span data-ttu-id="8eb36-124">Vous pouvez placer le `<textpath>` sous-élément à l’intérieur `<shape>` ou `<shapetype>` pour dessiner du texte.</span><span class="sxs-lookup"><span data-stu-id="8eb36-124">You can place the `<textpath>` sub-element inside `<shape>` or `<shapetype>` to draw text.</span></span> <span data-ttu-id="8eb36-125">Vous pouvez ensuite utiliser les attributs de propriété du `<textpath>` sous-élément pour personnaliser le texte.</span><span class="sxs-lookup"><span data-stu-id="8eb36-125">You can then use the property attributes of the `<textpath>` sub-element to customize the text.</span></span> <span data-ttu-id="8eb36-126">Vous pouvez également utiliser le `<formulas>` sous-élément pour définir le contour du texte.</span><span class="sxs-lookup"><span data-stu-id="8eb36-126">You can also use the `<formulas>` sub-element to define the outline of the text.</span></span>

<span data-ttu-id="8eb36-127">Par exemple, pour créer le texte affiché dans l’image suivante, vous pouvez taper la représentation VML ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="8eb36-127">For example, to create the text shown in the following picture, you can type the VML representation below.</span></span> <span data-ttu-id="8eb36-128">Notez que nous utilisons l' `<shapetype>` élément pour définir un prototype pour le contour du texte.</span><span class="sxs-lookup"><span data-stu-id="8eb36-128">Notice that we use the `<shapetype>` element to define a prototype for the outline of the text.</span></span> <span data-ttu-id="8eb36-129">Nous instancions ensuite deux formes à partir du même Typedeforme.</span><span class="sxs-lookup"><span data-stu-id="8eb36-129">We then instantiate two shapes from the same shapetype.</span></span> <span data-ttu-id="8eb36-130">Vous pouvez simplement modifier l’attribut de propriété de **chaîne** pour afficher un texte différent.</span><span class="sxs-lookup"><span data-stu-id="8eb36-130">You can simply change the **string** property attribute to display different text.</span></span>

![Shape1 \-1.gif (4898 octets)](images/shape1-1t.gif)

![Shape1 \-2.gif (2789 octets)](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





<span data-ttu-id="8eb36-133">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span><span class="sxs-lookup"><span data-stu-id="8eb36-133">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858398) .</span></span>

 

 