---
title: CoordSize VML (attribut)
description: CoordSize VML (attribut)
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509658"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="b0e25-103">CoordSize VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="b0e25-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="b0e25-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b0e25-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b0e25-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b0e25-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b0e25-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b0e25-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b0e25-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b0e25-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b0e25-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b0e25-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b0e25-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b0e25-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b0e25-110">Spécifie les unités horizontales et verticales du rectangle qui délimite une forme.</span><span class="sxs-lookup"><span data-stu-id="b0e25-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="b0e25-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b0e25-111">Read/write.</span></span> <span data-ttu-id="b0e25-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="b0e25-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="b0e25-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b0e25-113">**Applies To**</span></span>

[<span data-ttu-id="b0e25-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="b0e25-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b0e25-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b0e25-115">**Tag Syntax**</span></span>

<span data-ttu-id="b0e25-116"><v : *Element* coordsize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b0e25-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="b0e25-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b0e25-117">**Script Syntax**</span></span>

<span data-ttu-id="b0e25-118">*Element* . coordsize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b0e25-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="b0e25-119">*expression* = *élément*. coordsize</span><span class="sxs-lookup"><span data-stu-id="b0e25-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="b0e25-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b0e25-120">**Remarks**</span></span>

<span data-ttu-id="b0e25-121">S’il n’est pas spécifié, la taille de la coordonnée est identique à celle du cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="b0e25-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="b0e25-122">Notez que cet attribut est un vecteur et que les unités sont relatives à la longueur et à la largeur du rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="b0e25-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="b0e25-123">Notez également que le mappage entre **coordsize** et le cadre englobant peut être transformé en anisotrope.</span><span class="sxs-lookup"><span data-stu-id="b0e25-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="b0e25-124">Assurez-vous que les **coordsize Width** et **coordsize Height** sont identiques à la largeur et à la **hauteur** du **style** si vous ne souhaitez pas déformer la forme.</span><span class="sxs-lookup"><span data-stu-id="b0e25-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="b0e25-125">Dans les scripts, étant donné qu’il s’agit d’un vecteur 2D, vous pouvez accéder aux valeurs x et y séparément, et vous pouvez également déterminer le type d’unités attendu.</span><span class="sxs-lookup"><span data-stu-id="b0e25-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="b0e25-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b0e25-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="b0e25-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b0e25-127">**Example**</span></span>

<span data-ttu-id="b0e25-128">La forme est supérieure à 100 points et 100 points de large, mais chaque unité horizontale et verticale dans l’espace de coordonnées est 1/10 d’un point.</span><span class="sxs-lookup"><span data-stu-id="b0e25-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="b0e25-129">[Exemple d’attribut CoordSize](/previous-versions/bb229665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0e25-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="b0e25-130">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="b0e25-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 