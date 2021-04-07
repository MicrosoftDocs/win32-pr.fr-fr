---
title: Attribut Flip VML
description: Attribut Flip VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730148"
---
# <a name="vml-flip-attribute"></a><span data-ttu-id="3d8b0-103">Attribut Flip VML</span><span class="sxs-lookup"><span data-stu-id="3d8b0-103">VML Flip Attribute</span></span>

<span data-ttu-id="3d8b0-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3d8b0-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3d8b0-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3d8b0-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3d8b0-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3d8b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3d8b0-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3d8b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3d8b0-110">Change l’orientation d’une forme.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-110">Switches the orientation of a shape.</span></span> <span data-ttu-id="3d8b0-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-111">Read/write.</span></span> <span data-ttu-id="3d8b0-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-112">**String**.</span></span>

<span data-ttu-id="3d8b0-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3d8b0-113">**Applies To**</span></span>

[<span data-ttu-id="3d8b0-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="3d8b0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3d8b0-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="3d8b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="3d8b0-116"><v : *Element* style = "Flip : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3d8b0-116"><v: *element* style="flip: *expression* "></span></span>

<span data-ttu-id="3d8b0-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="3d8b0-117">**Script Syntax**</span></span>

<span data-ttu-id="3d8b0-118">*Element* . style. Flip = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3d8b0-118">*element* .style.flip="*expression*"</span></span>

<span data-ttu-id="3d8b0-119">*expression* = *Element*. style. Flip</span><span class="sxs-lookup"><span data-stu-id="3d8b0-119">*expression*=*element*.style.flip</span></span>

<span data-ttu-id="3d8b0-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="3d8b0-120">**Remarks**</span></span>

<span data-ttu-id="3d8b0-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="3d8b0-121">Values include:</span></span>



| <span data-ttu-id="3d8b0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d8b0-122">Value</span></span> | <span data-ttu-id="3d8b0-123">Description</span><span class="sxs-lookup"><span data-stu-id="3d8b0-123">Description</span></span>                                           |
|-------|-------------------------------------------------------|
| <span data-ttu-id="3d8b0-124">x</span><span class="sxs-lookup"><span data-stu-id="3d8b0-124">x</span></span>     | <span data-ttu-id="3d8b0-125">Retournez le long de l’axe y, en inversant les coordonnées *x*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-125">Flip along the y-axis, reversing the *x*-coordinates.</span></span> |
| <span data-ttu-id="3d8b0-126">y</span><span class="sxs-lookup"><span data-stu-id="3d8b0-126">y</span></span>     | <span data-ttu-id="3d8b0-127">Retournez le long de l’axe *x*, en inversant les coordonnées y.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-127">Flip along the *x*-axis, reversing the y-coordinates.</span></span> |
| <span data-ttu-id="3d8b0-128">xy</span><span class="sxs-lookup"><span data-stu-id="3d8b0-128">xy</span></span>    | <span data-ttu-id="3d8b0-129">Retournez le long de l’axe y et de l’axe *x*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-129">Flip along both the y- and *x*-axis.</span></span>                  |
| <span data-ttu-id="3d8b0-130">yx</span><span class="sxs-lookup"><span data-stu-id="3d8b0-130">yx</span></span>    | <span data-ttu-id="3d8b0-131">Retournez sur l’axe des *x* et de l’axe des *y*.</span><span class="sxs-lookup"><span data-stu-id="3d8b0-131">Flip along both the *x*- and *y*-axis.</span></span>                |



 

<span data-ttu-id="3d8b0-132">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="3d8b0-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="3d8b0-133">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="3d8b0-133">**See Also**</span></span>

[<span data-ttu-id="3d8b0-134">VgFlipOrientation</span><span class="sxs-lookup"><span data-stu-id="3d8b0-134">VgFlipOrientation</span></span>](msdn-online-vector-markup-language-object-model-reference.md)

<span data-ttu-id="3d8b0-135">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="3d8b0-135">**Example**</span></span>

<span data-ttu-id="3d8b0-136">La forme est retournée le long de l’axe *y* en inversant les coordonnées *x* .</span><span class="sxs-lookup"><span data-stu-id="3d8b0-136">The shape is flipped along the *y* -axis by reversing the *x* -coordinates.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



<span data-ttu-id="3d8b0-137">[Exemple d’attribut Flip](/previous-versions/bb229670(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3d8b0-137">[Flip Attribute Example](/previous-versions/bb229670(v=vs.85)).</span></span> <span data-ttu-id="3d8b0-138">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="3d8b0-138">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 