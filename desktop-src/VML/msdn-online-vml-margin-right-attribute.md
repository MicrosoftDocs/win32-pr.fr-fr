---
title: Attribut Margin-Right VML
description: Attribut Margin-Right VML
ms.assetid: 7b635bea-df3f-4a24-aa22-cfca95575599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5529257a0e21c8a8f8c7a1a2f8381c10a6e3b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031832"
---
# <a name="vml-margin-right-attribute"></a><span data-ttu-id="d537b-103">Attribut Margin-Right VML</span><span class="sxs-lookup"><span data-stu-id="d537b-103">VML Margin-Right Attribute</span></span>

<span data-ttu-id="d537b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d537b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d537b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d537b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d537b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d537b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d537b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d537b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d537b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d537b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d537b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d537b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d537b-110">Spécifie le bord droit du rectangle conteneur de la forme par rapport au point d’ancrage de la forme.</span><span class="sxs-lookup"><span data-stu-id="d537b-110">Specifies the right edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="d537b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d537b-111">Read/write.</span></span> <span data-ttu-id="d537b-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="d537b-112">**String**.</span></span>

<span data-ttu-id="d537b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d537b-113">**Applies To**</span></span>

[<span data-ttu-id="d537b-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="d537b-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d537b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d537b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d537b-116"><v : *Element* style = "margin-right : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d537b-116"><v: *element* style="margin-right: *expression* "></span></span>

<span data-ttu-id="d537b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d537b-117">**Script Syntax**</span></span>

<span data-ttu-id="d537b-118">*Element* . style. marginRight = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d537b-118">*element* .style.marginright="*expression*"</span></span>

<span data-ttu-id="d537b-119">*expression* = *Element*. style. marginRight</span><span class="sxs-lookup"><span data-stu-id="d537b-119">*expression*=*element*.style.marginright</span></span>

<span data-ttu-id="d537b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d537b-120">**Remarks**</span></span>

<span data-ttu-id="d537b-121">L’attribut **margin-right** est semblable à l’attribut Margin HTML standard **-Right** utilisé avec les feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="d537b-121">The **Margin-Right** attribute is similar to the standard HTML **Margin-Right** attribute used with style sheets.</span></span>

<span data-ttu-id="d537b-122">Notez que **marginRight** est utilisé à la place de **margin-right** pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="d537b-122">Note that **marginright** is used instead of **margin-right** for scripting.</span></span> <span data-ttu-id="d537b-123">Notez également que si la **position** est **absolue**, la marge n’apparaîtra pas pour changer.</span><span class="sxs-lookup"><span data-stu-id="d537b-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="d537b-124">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="d537b-124">Values include:</span></span>



| <span data-ttu-id="d537b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d537b-125">Value</span></span>      | <span data-ttu-id="d537b-126">Description</span><span class="sxs-lookup"><span data-stu-id="d537b-126">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d537b-127">Auto</span><span class="sxs-lookup"><span data-stu-id="d537b-127">Auto</span></span>       | <span data-ttu-id="d537b-128">Position par défaut d’un élément dans le Flow de la page.</span><span class="sxs-lookup"><span data-stu-id="d537b-128">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="d537b-129">units</span><span class="sxs-lookup"><span data-stu-id="d537b-129">units</span></span>      | <span data-ttu-id="d537b-130">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="d537b-130">Default.</span></span> <span data-ttu-id="d537b-131">Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="d537b-131">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="d537b-132">Si aucune unité n’est donnée, les pixels (PX) sont pris en compte.</span><span class="sxs-lookup"><span data-stu-id="d537b-132">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="d537b-133">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="d537b-133">The default value is 0.</span></span> |
| <span data-ttu-id="d537b-134">percentage</span><span class="sxs-lookup"><span data-stu-id="d537b-134">percentage</span></span> | <span data-ttu-id="d537b-135">Valeur exprimée sous la forme d’un pourcentage de la hauteur de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="d537b-135">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="d537b-136">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="d537b-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="d537b-137">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="d537b-137">**See Also**</span></span>

[<span data-ttu-id="d537b-138">Unités</span><span class="sxs-lookup"><span data-stu-id="d537b-138">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="d537b-139">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="d537b-139">**Example**</span></span>

<span data-ttu-id="d537b-140">La marge de droite est définie à 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="d537b-140">The right margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-right:25px">
   </v:rect>
```



<span data-ttu-id="d537b-141">[Exemple d’attribut margin-right](/previous-versions/bb229677(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d537b-141">[Margin-Right Attribute Example](/previous-versions/bb229677(v=vs.85)).</span></span> <span data-ttu-id="d537b-142">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="d537b-142">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 