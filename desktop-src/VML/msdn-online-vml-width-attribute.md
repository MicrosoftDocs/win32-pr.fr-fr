---
title: Attribut width VML
description: Attribut width VML
ms.assetid: e01c60d4-3c3a-41e5-8c28-6da9533921df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654b3d4917d76b3c8820186b04b2e77537e6a6ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510475"
---
# <a name="vml-width-attribute"></a><span data-ttu-id="a3394-103">Attribut width VML</span><span class="sxs-lookup"><span data-stu-id="a3394-103">VML Width Attribute</span></span>

<span data-ttu-id="a3394-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a3394-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a3394-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a3394-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a3394-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a3394-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a3394-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a3394-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a3394-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a3394-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a3394-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a3394-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a3394-110">Définit la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="a3394-110">Defines the width of the shape.</span></span> <span data-ttu-id="a3394-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a3394-111">Read/write.</span></span> <span data-ttu-id="a3394-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="a3394-112">**String**.</span></span>

<span data-ttu-id="a3394-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a3394-113">**Applies To**</span></span>

[<span data-ttu-id="a3394-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="a3394-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a3394-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a3394-115">**Tag Syntax**</span></span>

<span data-ttu-id="a3394-116"><v : *Element* style = "width : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a3394-116"><v: *element* style="width: *expression* "></span></span>

<span data-ttu-id="a3394-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="a3394-117">**Script Syntax**</span></span>

<span data-ttu-id="a3394-118">*Element* . style. Width = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a3394-118">*element* .style.width="*expression*"</span></span>

<span data-ttu-id="a3394-119">*expression* = *Element*. style. Width</span><span class="sxs-lookup"><span data-stu-id="a3394-119">*expression*=*element*.style.width</span></span>

<span data-ttu-id="a3394-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a3394-120">**Remarks**</span></span>

<span data-ttu-id="a3394-121">L’attribut **Width** est semblable à l’attribut **Width** HTML standard pour les styles.</span><span class="sxs-lookup"><span data-stu-id="a3394-121">The **Width** attribute is similar to the standard HTML **Width** attribute for styles.</span></span>

<span data-ttu-id="a3394-122">Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues.</span><span class="sxs-lookup"><span data-stu-id="a3394-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="a3394-123">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="a3394-123">Values include:</span></span>



| <span data-ttu-id="a3394-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3394-124">Value</span></span>      | <span data-ttu-id="a3394-125">Description</span><span class="sxs-lookup"><span data-stu-id="a3394-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3394-126">Auto</span><span class="sxs-lookup"><span data-stu-id="a3394-126">Auto</span></span>       | <span data-ttu-id="a3394-127">Position par défaut d’un élément dans le Flow de la page.</span><span class="sxs-lookup"><span data-stu-id="a3394-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="a3394-128">units</span><span class="sxs-lookup"><span data-stu-id="a3394-128">units</span></span>      | <span data-ttu-id="a3394-129">Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="a3394-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="a3394-130">Si aucune unité n’est donnée, les pixels (PX) sont pris en compte.</span><span class="sxs-lookup"><span data-stu-id="a3394-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="a3394-131">percentage</span><span class="sxs-lookup"><span data-stu-id="a3394-131">percentage</span></span> | <span data-ttu-id="a3394-132">Valeur exprimée sous la forme d’un pourcentage de la largeur de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="a3394-132">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="a3394-133">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="a3394-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="a3394-134">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="a3394-134">**See Also**</span></span>

[<span data-ttu-id="a3394-135">Unités</span><span class="sxs-lookup"><span data-stu-id="a3394-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="a3394-136">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a3394-136">**Example**</span></span>

<span data-ttu-id="a3394-137">La largeur de la forme est 25.</span><span class="sxs-lookup"><span data-stu-id="a3394-137">The width of the shape is 25.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:25;height:20">
   </v:rect>
```



<span data-ttu-id="a3394-138">[Exemple d’attribut width](/previous-versions/bb264101(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3394-138">[Width Attribute Example](/previous-versions/bb264101(v=vs.85)).</span></span> <span data-ttu-id="a3394-139">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="a3394-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 