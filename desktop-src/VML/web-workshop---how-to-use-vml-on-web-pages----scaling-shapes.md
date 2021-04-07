---
title: Mise à l’échelle des formes
description: Mise à l’échelle des formes
ms.assetid: fe975ebd-9b27-409d-a7c2-ac5ee08d1d4f
keywords:
- Atelier Web, mise à l’échelle des formes
- conception de pages Web, mise à l’échelle des formes
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
ms.openlocfilehash: e2e7c64fdc0eaa32df1f22b06734b366609ee319
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727940"
---
# <a name="scaling-shapes"></a><span data-ttu-id="54b38-115">Mise à l’échelle des formes</span><span class="sxs-lookup"><span data-stu-id="54b38-115">Scaling Shapes</span></span>

<span data-ttu-id="54b38-116">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="54b38-116">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="54b38-117">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="54b38-117">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="54b38-118">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="54b38-118">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="54b38-119">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="54b38-119">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="54b38-120">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="54b38-120">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="54b38-121">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="54b38-121">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="54b38-122">Vous avez appris à dessiner et à colorier des formes sur une page Web à l’aide de VML.</span><span class="sxs-lookup"><span data-stu-id="54b38-122">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="54b38-123">Dans cette rubrique, nous allons vous montrer comment mettre les formes à l’échelle selon la taille de votre choix.</span><span class="sxs-lookup"><span data-stu-id="54b38-123">In this topic, we will illustrate how to scale shapes to any size you want.</span></span>

<span data-ttu-id="54b38-124">VML utilise la même syntaxe que celle définie dans la section [Détails du modèle de rendu visuel](https://www.w3.org/TR/PR-CSS2/visudet.mdl) de la [Spécification CSS2](https://www.w3.org/TR/PR-CSS2/) pour spécifier la taille de la zone conteneur afin que le contenu d’une forme soit rendu (dessiné) dans la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="54b38-124">VML uses the same syntax defined in the [Visual Rendering Model Details](https://www.w3.org/TR/PR-CSS2/visudet.mdl) section of the [CSS2 specification](https://www.w3.org/TR/PR-CSS2/) to specify the size of the containing box so that the contents of a shape will be rendered (drawn) within the containing box.</span></span> <span data-ttu-id="54b38-125">Vous pouvez utiliser les attributs de style de **largeur** et de **hauteur** pour définir la taille de la zone conteneur.</span><span class="sxs-lookup"><span data-stu-id="54b38-125">You can use the **width** and **height** style attributes to define the size of the containing box.</span></span>

<span data-ttu-id="54b38-126">Par exemple, si vous dessinez un ovale et spécifiez **style**= 'width : 75pt ; height : 100pt', l’ovale sera dessiné dans une zone conteneur à une taille de 75 points (largeur) de 100 points (hauteur), comme indiqué dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="54b38-126">For example, if you draw an oval and specify **style**='width:75pt;height:100pt', the oval will be drawn within a containing box at a size of 75 points (width) by 100 points (height), as shown in the following picture:</span></span>

![oval1.gif (660 octets)](images/oval1.gif)


```HTML
<v:oval style='width:75pt;height:100pt'
fillcolor="red" />
```





<span data-ttu-id="54b38-128">Si vous modifiez la taille en **style**= 'width : 120PT ; height : 140pt', l’ovale devient plus grand car il est mis à l’échelle dans la nouvelle zone conteneur à une taille de 120 points (largeur) de 140 points (hauteur), comme illustré dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="54b38-128">If you change the size to **style**='width:120pt;height:140pt', the oval becomes larger because it is scaled within the new containing box at a size of 120 points (width) by 140 points (height), as shown in the following picture:</span></span>

![oval2.gif (966 octets)](images/oval2.gif)


```HTML
<v:oval style='width:120pt;height:140pt'
fillcolor="red" />
```





<span data-ttu-id="54b38-130">Si vous modifiez la taille en **style**= 'width : 60pt ; height : 40pt', l’ovale devient plus petit, car il est mis à l’échelle dans la nouvelle zone conteneur à une taille de 60 points (largeur) de 40 points (hauteur), comme indiqué dans l’image suivante :</span><span class="sxs-lookup"><span data-stu-id="54b38-130">If you change the size to **style**='width:60pt;height:40pt', the oval becomes smaller because it is scaled within the new containing box at a size of 60 points (width) by 40 points (height), as shown in the following picture:</span></span>

![oval3.gif (394 octets)](images/oval3.gif)


```HTML
<v:oval style='width:60pt;height:40pt'
fillcolor="red" />
```





 

 