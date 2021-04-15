---
title: Attribut VML à gauche
description: Attribut VML à gauche
ms.assetid: a0558d24-c0a5-48ef-9042-743d6eab6f86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17810d7635d4b8194f2bd2df258a900cb534581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463599"
---
# <a name="vml-left-attribute"></a><span data-ttu-id="36d13-103">Attribut VML à gauche</span><span class="sxs-lookup"><span data-stu-id="36d13-103">VML Left Attribute</span></span>

<span data-ttu-id="36d13-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="36d13-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="36d13-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="36d13-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="36d13-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="36d13-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="36d13-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="36d13-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="36d13-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="36d13-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="36d13-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="36d13-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="36d13-110">Détermine la position de la forme par rapport à l’élément à gauche dans le Workflow.</span><span class="sxs-lookup"><span data-stu-id="36d13-110">Determines the position of the shape relative to the element left of it in the document flow.</span></span> <span data-ttu-id="36d13-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="36d13-111">Read/write.</span></span> <span data-ttu-id="36d13-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="36d13-112">**String**.</span></span>

<span data-ttu-id="36d13-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="36d13-113">**Applies To**</span></span>

[<span data-ttu-id="36d13-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="36d13-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="36d13-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="36d13-115">**Tag Syntax**</span></span>

<span data-ttu-id="36d13-116"><v : *Element* style = "left : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="36d13-116"><v: *element* style="left: *expression* "></span></span>

<span data-ttu-id="36d13-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="36d13-117">**Script Syntax**</span></span>

<span data-ttu-id="36d13-118">*Element* . style. Left = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="36d13-118">*element* .style.left="*expression*"</span></span>

<span data-ttu-id="36d13-119">*expression* = *Element*. style. Left</span><span class="sxs-lookup"><span data-stu-id="36d13-119">*expression*=*element*.style.left</span></span>

<span data-ttu-id="36d13-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="36d13-120">**Remarks**</span></span>

<span data-ttu-id="36d13-121">L’attribut **Left** est semblable à l’attribut HTML standard **Left** pour les styles.</span><span class="sxs-lookup"><span data-stu-id="36d13-121">The **Left** attribute is similar to the standard HTML **Left** attribute for styles.</span></span>

<span data-ttu-id="36d13-122">Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues.</span><span class="sxs-lookup"><span data-stu-id="36d13-122">Units may be mapped to the parent element or may be in absolute units.</span></span> <span data-ttu-id="36d13-123">Cet attribut ne sera pas écrit pour les formes ancrées en ligne.</span><span class="sxs-lookup"><span data-stu-id="36d13-123">This attribute will not be written out for shapes anchored inline.</span></span>

<span data-ttu-id="36d13-124">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="36d13-124">Values include:</span></span>



| <span data-ttu-id="36d13-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="36d13-125">Value</span></span>      | <span data-ttu-id="36d13-126">Description</span><span class="sxs-lookup"><span data-stu-id="36d13-126">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d13-127">Auto</span><span class="sxs-lookup"><span data-stu-id="36d13-127">Auto</span></span>       | <span data-ttu-id="36d13-128">Position par défaut d’un élément dans le Flow de la page.</span><span class="sxs-lookup"><span data-stu-id="36d13-128">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="36d13-129">units</span><span class="sxs-lookup"><span data-stu-id="36d13-129">units</span></span>      | <span data-ttu-id="36d13-130">Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="36d13-130">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="36d13-131">Si aucune unité n’est donnée, les pixels (PX) sont pris en compte.</span><span class="sxs-lookup"><span data-stu-id="36d13-131">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="36d13-132">percentage</span><span class="sxs-lookup"><span data-stu-id="36d13-132">percentage</span></span> | <span data-ttu-id="36d13-133">Valeur exprimée sous la forme d’un pourcentage de la largeur de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="36d13-133">Value expressed as a percentage of the parent object's width.</span></span>                                                                                                    |



 

<span data-ttu-id="36d13-134">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="36d13-134">*VML Standard Attribute*</span></span>

<span data-ttu-id="36d13-135">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="36d13-135">**See Also**</span></span>

[<span data-ttu-id="36d13-136">Unités</span><span class="sxs-lookup"><span data-stu-id="36d13-136">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="36d13-137">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="36d13-137">**Example**</span></span>

<span data-ttu-id="36d13-138">La valeur de gauche de la forme est définie sur 1 dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="36d13-138">The left value of the shape is set to 1 in the example below.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="36d13-139">[Exemple d’attribut Left](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span><span class="sxs-lookup"><span data-stu-id="36d13-139">[Left Attribute Example](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/examples/x_left.md).</span></span> <span data-ttu-id="36d13-140">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="36d13-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 