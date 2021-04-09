---
title: Attribut de hauteur VML
description: Attribut de hauteur VML
ms.assetid: 5667ddc5-c840-40d8-894e-58396f56e0fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41751e4863fdb128dbbedf2e3abf8e7f0a6736d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101840"
---
# <a name="vml-height-attribute"></a><span data-ttu-id="e9162-103">Attribut de hauteur VML</span><span class="sxs-lookup"><span data-stu-id="e9162-103">VML Height Attribute</span></span>

<span data-ttu-id="e9162-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e9162-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e9162-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e9162-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e9162-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e9162-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e9162-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e9162-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e9162-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e9162-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e9162-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e9162-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e9162-110">Spécifie la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="e9162-110">Specifies the height of the shape.</span></span> <span data-ttu-id="e9162-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e9162-111">Read/write.</span></span> <span data-ttu-id="e9162-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="e9162-112">**String**.</span></span>

<span data-ttu-id="e9162-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e9162-113">**Applies To**</span></span>

[<span data-ttu-id="e9162-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="e9162-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e9162-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="e9162-115">**Tag Syntax**</span></span>

<span data-ttu-id="e9162-116"><v : *Element* style = "height : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e9162-116"><v: *element* style="height: *expression* "></span></span>

<span data-ttu-id="e9162-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="e9162-117">**Script Syntax**</span></span>

<span data-ttu-id="e9162-118">*Element* . style. Height = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e9162-118">*element* .style.height="*expression*"</span></span>

<span data-ttu-id="e9162-119">*expression* = *Element*. style. Height</span><span class="sxs-lookup"><span data-stu-id="e9162-119">*expression*=*element*.style.height</span></span>

<span data-ttu-id="e9162-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="e9162-120">**Remarks**</span></span>

<span data-ttu-id="e9162-121">L’attribut **Height** est semblable à l’attribut **Height** HTML standard pour les styles.</span><span class="sxs-lookup"><span data-stu-id="e9162-121">The **Height** attribute is similar to the standard HTML **Height** attribute for styles.</span></span>

<span data-ttu-id="e9162-122">Les unités peuvent être mappées à l’élément parent ou peuvent être en unités absolues.</span><span class="sxs-lookup"><span data-stu-id="e9162-122">Units may be mapped to the parent element or may be in absolute units.</span></span>

<span data-ttu-id="e9162-123">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="e9162-123">Values include:</span></span>



| <span data-ttu-id="e9162-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9162-124">Value</span></span>      | <span data-ttu-id="e9162-125">Description</span><span class="sxs-lookup"><span data-stu-id="e9162-125">Description</span></span>                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9162-126">Auto</span><span class="sxs-lookup"><span data-stu-id="e9162-126">Auto</span></span>       | <span data-ttu-id="e9162-127">Position par défaut d’un élément dans le Flow de la page.</span><span class="sxs-lookup"><span data-stu-id="e9162-127">Default position of an element in the flow of the page.</span></span>                                                                                                          |
| <span data-ttu-id="e9162-128">units</span><span class="sxs-lookup"><span data-stu-id="e9162-128">units</span></span>      | <span data-ttu-id="e9162-129">Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="e9162-129">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="e9162-130">Si aucune unité n’est donnée, les pixels (PX) sont pris en compte.</span><span class="sxs-lookup"><span data-stu-id="e9162-130">If no units are given, pixels (px) is assumed.</span></span> |
| <span data-ttu-id="e9162-131">percentage</span><span class="sxs-lookup"><span data-stu-id="e9162-131">percentage</span></span> | <span data-ttu-id="e9162-132">Valeur exprimée sous la forme d’un pourcentage de la hauteur de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="e9162-132">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                   |



 

<span data-ttu-id="e9162-133">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="e9162-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="e9162-134">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="e9162-134">**See Also**</span></span>

[<span data-ttu-id="e9162-135">Unités</span><span class="sxs-lookup"><span data-stu-id="e9162-135">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="e9162-136">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e9162-136">**Example**</span></span>

<span data-ttu-id="e9162-137">La hauteur de la forme est définie sur 30.</span><span class="sxs-lookup"><span data-stu-id="e9162-137">The height of the shape is set to 30.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:30">
   </v:rect>
```



<span data-ttu-id="e9162-138">[Exemple d’attribut Height](/previous-versions/bb229671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e9162-138">[Height Attribute Example](/previous-versions/bb229671(v=vs.85)).</span></span> <span data-ttu-id="e9162-139">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="e9162-139">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 