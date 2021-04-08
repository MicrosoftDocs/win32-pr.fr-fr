---
title: CoordOrigin VML (attribut)
description: CoordOrigin VML (attribut)
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842345"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="2f2df-103">CoordOrigin VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="2f2df-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="2f2df-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2f2df-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2f2df-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2f2df-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2f2df-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2f2df-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2f2df-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2f2df-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2f2df-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2f2df-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2f2df-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2f2df-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2f2df-110">Spécifie l’origine de l’unité de coordonnée du rectangle qui délimite une forme.</span><span class="sxs-lookup"><span data-stu-id="2f2df-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="2f2df-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2f2df-111">Read/write.</span></span> <span data-ttu-id="2f2df-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2f2df-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="2f2df-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2f2df-113">**Applies To**</span></span>

[<span data-ttu-id="2f2df-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="2f2df-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="2f2df-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="2f2df-115">**Tag Syntax**</span></span>

<span data-ttu-id="2f2df-116"><v : *Element* coordorigin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2f2df-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="2f2df-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="2f2df-117">**Script Syntax**</span></span>

<span data-ttu-id="2f2df-118">*Element* . coordorigin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2f2df-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="2f2df-119">*expression* = *élément*. coordorigin</span><span class="sxs-lookup"><span data-stu-id="2f2df-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="2f2df-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="2f2df-120">**Remarks**</span></span>

<span data-ttu-id="2f2df-121">Si cette valeur n’est pas spécifiée, les coordonnées d’origine sont (0,0) dans le coin supérieur gauche du cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="2f2df-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="2f2df-122">La valeur x de **CoordSize** est ajoutée à la valeur x de **CoordOrigin** pour déterminer la plage des valeurs horizontales.</span><span class="sxs-lookup"><span data-stu-id="2f2df-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="2f2df-123">Par exemple, si la valeur x de **CoordOrigin** est-100 et la valeur x de **CoordSize** est 200, les unités horizontales vont de-100 à + 100.</span><span class="sxs-lookup"><span data-stu-id="2f2df-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="2f2df-124">Si la valeur x de **CoordOrigin** est 100 et la valeur x de **CoordSize** est 200, les unités horizontales sont comprises entre 100 et 300, le tout dans le cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="2f2df-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="2f2df-125">Il en va de même pour les valeurs y.</span><span class="sxs-lookup"><span data-stu-id="2f2df-125">The same is true for the y values.</span></span>

<span data-ttu-id="2f2df-126">Notez que cet attribut est un vecteur et que les unités sont du même type que [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2df-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="2f2df-127">Dans les scripts, étant donné qu’il s’agit d’un vecteur 2D, vous pouvez accéder aux valeurs x et y séparément, et vous pouvez également déterminer le type d’unités attendu.</span><span class="sxs-lookup"><span data-stu-id="2f2df-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="2f2df-128">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="2f2df-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="2f2df-129">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2f2df-129">**Example**</span></span>

<span data-ttu-id="2f2df-130">Le centre du cadre englobant sera l’origine (0,0) du tracé de la forme.</span><span class="sxs-lookup"><span data-stu-id="2f2df-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="2f2df-131">Comme **CoordOrigin** est « -500-500 » et **CoordSize** est « 1000 1000 », les unités horizontale et verticale vont de-500 à + 500.</span><span class="sxs-lookup"><span data-stu-id="2f2df-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="2f2df-132">Le coin supérieur gauche du tracé se trouve au centre de la zone englobante définie par les points gauche et supérieur tels que définis par **style**.</span><span class="sxs-lookup"><span data-stu-id="2f2df-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="2f2df-133">[Exemple d’attribut CoordOrigin](/previous-versions/bb229664(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f2df-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="2f2df-134">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="2f2df-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 