---
title: Utilisation de l’élément Shadow
description: Utilisation de l’élément Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Atelier Web, élément Shadow
- conception de pages Web, élément Shadow
- Langage VML (VML), élément Shadow
- VML (langage VML), élément Shadow
- graphiques vectoriels, élément Shadow
- élément Shadow
- Éléments VML, ombre
- Formes VML, élément Shadow
- Langage VML (VML), dessin avec des effets d’ombre
- VML (langage VML), dessin avec des effets d’ombre
- graphiques vectoriels, dessin avec des effets d’ombre
- Formes VML, dessin avec des effets d’ombre
- dessiner avec des effets d’ombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382667"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="d00b6-116">Utilisation de l’élément Shadow</span><span class="sxs-lookup"><span data-stu-id="d00b6-116">Using the Shadow Element</span></span>

<span data-ttu-id="d00b6-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d00b6-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d00b6-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d00b6-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d00b6-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d00b6-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d00b6-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d00b6-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d00b6-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d00b6-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d00b6-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d00b6-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d00b6-123">Dans cette rubrique, nous allons vous montrer comment utiliser le `<shadow>` sous-élément pour dessiner une forme qui a divers effets d’ombre.</span><span class="sxs-lookup"><span data-stu-id="d00b6-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="d00b6-124">Vous pouvez placer le `<shadow>` sous-élément à l’intérieur du `<shape>` , `<shapetype>` ou de n’importe quel élément de forme prédéfini pour dessiner une forme avec une ombre.</span><span class="sxs-lookup"><span data-stu-id="d00b6-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="d00b6-125">Vous pouvez ensuite utiliser les attributs de propriété du `<shadow>` sous-élément pour personnaliser l’ombre.</span><span class="sxs-lookup"><span data-stu-id="d00b6-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="d00b6-126">Par exemple, pour créer une forme avec une ombre, comme illustré dans l’image suivante, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :</span><span class="sxs-lookup"><span data-stu-id="d00b6-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 octets)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="d00b6-128">`on="t"` et `type="perspective"` indiquent d’activer l’ombre à l’aide du type de perspective.</span><span class="sxs-lookup"><span data-stu-id="d00b6-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="d00b6-129">L' **origine** et le **décalage** indiquent où dessiner l’ombre.</span><span class="sxs-lookup"><span data-stu-id="d00b6-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="d00b6-130">`matrix="..."` spécifie la matrice de transformation de perspective.</span><span class="sxs-lookup"><span data-stu-id="d00b6-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="d00b6-131">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span><span class="sxs-lookup"><span data-stu-id="d00b6-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 