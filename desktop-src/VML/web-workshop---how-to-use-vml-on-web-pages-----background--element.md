---
title: Utilisation de l’élément background
description: Utilisation de l’élément background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Atelier Web, élément d’arrière-plan
- conception de pages Web, élément d’arrière-plan
- Langage VML (VML), élément d’arrière-plan
- VML (langage VML), élément d’arrière-plan
- graphiques vectoriels, élément d’arrière-plan
- élément d’arrière-plan
- Éléments VML, arrière-plan
- Formes VML, élément d’arrière-plan
- Langage VML (VML), personnalisation des arrière-plans
- VML (langage VML), personnalisation des arrière-plans
- graphiques vectoriels, personnalisation des arrière-plans
- Formes VML, personnaliser les arrière-plans
- personnalisation des arrière-plans
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842393"
---
# <a name="using-the-background-element"></a><span data-ttu-id="88f5b-116">Utilisation de l’élément background</span><span class="sxs-lookup"><span data-stu-id="88f5b-116">Using the Background Element</span></span>

<span data-ttu-id="88f5b-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="88f5b-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="88f5b-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="88f5b-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="88f5b-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="88f5b-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="88f5b-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="88f5b-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="88f5b-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="88f5b-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="88f5b-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="88f5b-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="88f5b-123">Dans cette rubrique, nous allons illustrer comment personnaliser l’arrière-plan d’une page Web à l’aide de l' `<background>` élément fourni dans Vml.</span><span class="sxs-lookup"><span data-stu-id="88f5b-123">In this topic, we will illustrate how you can customize the background of a Web page by using the `<background>` element provided in VML.</span></span>

<span data-ttu-id="88f5b-124">Comme vous l’avez appris dans la rubrique [use `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , vous pouvez placer le `<fill>` sous-élément à l’intérieur de `<shape>` , `<shapetype>` ou tout élément de forme prédéfini pour décrire comment remplir la forme.</span><span class="sxs-lookup"><span data-stu-id="88f5b-124">As you've learned from the [Use `<fill>`](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) topic, you can place the `<fill>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span>

<span data-ttu-id="88f5b-125">De même, vous pouvez placer le `<fill>` sous-élément à l’intérieur de l' `<background>` élément pour décrire comment remplir l’arrière-plan d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="88f5b-125">Similarly, you can place the `<fill>` sub-element inside the `<background>` element to describe how to fill the background of a Web page.</span></span> <span data-ttu-id="88f5b-126">Vous pouvez ensuite utiliser les attributs de propriété du `<fill>` sous-élément pour personnaliser l’effet de remplissage, tel que le [remplissage dégradé](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), le [remplissage de motif](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)ou le remplissage de l' [image](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span><span class="sxs-lookup"><span data-stu-id="88f5b-126">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), [pattern fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), or [picture fill](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).</span></span>

<span data-ttu-id="88f5b-127">Par exemple, pour dessiner un arrière-plan dégradé rempli, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :</span><span class="sxs-lookup"><span data-stu-id="88f5b-127">For example, to draw a gradient-filled background, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





<span data-ttu-id="88f5b-128">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span><span class="sxs-lookup"><span data-stu-id="88f5b-128">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858389) .</span></span>

 

 