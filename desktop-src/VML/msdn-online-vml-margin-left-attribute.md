---
title: Attribut Margin-Left VML
description: Attribut Margin-Left VML
ms.assetid: 65488c47-06c2-4a8f-8d29-4837865465f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f98900e862f22f31ad444bc6fb6f372627eca1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315803"
---
# <a name="vml-margin-left-attribute"></a><span data-ttu-id="b8c31-103">Attribut Margin-Left VML</span><span class="sxs-lookup"><span data-stu-id="b8c31-103">VML Margin-Left Attribute</span></span>

<span data-ttu-id="b8c31-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b8c31-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b8c31-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b8c31-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b8c31-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b8c31-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b8c31-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b8c31-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b8c31-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b8c31-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b8c31-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b8c31-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b8c31-110">Spécifie le bord gauche du rectangle conteneur de la forme par rapport au point d’ancrage de la forme.</span><span class="sxs-lookup"><span data-stu-id="b8c31-110">Specifies the left edge of the shape's containing rectangle relative to the shape anchor.</span></span> <span data-ttu-id="b8c31-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b8c31-111">Read/write.</span></span> <span data-ttu-id="b8c31-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="b8c31-112">**String**.</span></span>

<span data-ttu-id="b8c31-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b8c31-113">**Applies To**</span></span>

[<span data-ttu-id="b8c31-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="b8c31-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b8c31-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b8c31-115">**Tag Syntax**</span></span>

<span data-ttu-id="b8c31-116"><v : *Element* style = "margin-left : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b8c31-116"><v: *element* style="margin-left: *expression* "></span></span>

<span data-ttu-id="b8c31-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b8c31-117">**Script Syntax**</span></span>

<span data-ttu-id="b8c31-118">*Element* . style. MarginLeft = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b8c31-118">*element* .style.marginleft="*expression*"</span></span>

<span data-ttu-id="b8c31-119">*expression* = *Element*. style. MarginLeft</span><span class="sxs-lookup"><span data-stu-id="b8c31-119">*expression*=*element*.style.marginleft</span></span>

<span data-ttu-id="b8c31-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b8c31-120">**Remarks**</span></span>

<span data-ttu-id="b8c31-121">L’attribut **margin-left** est semblable à l’attribut de **marge HTML standard-Left** utilisé avec les feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="b8c31-121">The **Margin-Left** attribute is similar to the standard HTML **Margin-Left** attribute used with style sheets.</span></span>

<span data-ttu-id="b8c31-122">Notez que la procédure **MarginLeft** est utilisée à la place de la **marge gauche** pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="b8c31-122">Note that **marginleft** is used instead of **margin-left** for scripting.</span></span> <span data-ttu-id="b8c31-123">Notez également que si la **position** est **absolue**, la marge n’apparaîtra pas pour changer.</span><span class="sxs-lookup"><span data-stu-id="b8c31-123">Also note that if the **position** is **absolute**, the margin will not appear to change.</span></span>

<span data-ttu-id="b8c31-124">Cette propriété est utilisée au lieu de **gauche** pour les formes dans Microsoft Word et Microsoft Excel qui flottent dans une position relative à un point d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="b8c31-124">This property is used instead of **Left** for shapes in Microsoft Word and Microsoft Excel that are floating in a position relative to an anchor point.</span></span>

<span data-ttu-id="b8c31-125">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="b8c31-125">Values include:</span></span>



| <span data-ttu-id="b8c31-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8c31-126">Value</span></span>      | <span data-ttu-id="b8c31-127">Description</span><span class="sxs-lookup"><span data-stu-id="b8c31-127">Description</span></span>                                                                                                                                                                                       |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c31-128">Auto</span><span class="sxs-lookup"><span data-stu-id="b8c31-128">Auto</span></span>       | <span data-ttu-id="b8c31-129">Position par défaut d’un élément dans le Flow de la page.</span><span class="sxs-lookup"><span data-stu-id="b8c31-129">Default position of an element in the flow of the page.</span></span>                                                                                                                                           |
| <span data-ttu-id="b8c31-130">units</span><span class="sxs-lookup"><span data-stu-id="b8c31-130">units</span></span>      | <span data-ttu-id="b8c31-131">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8c31-131">Default.</span></span> <span data-ttu-id="b8c31-132">Nombre avec un indicateur d’unités absolues (cm, mm, in, PT, PC ou px) ou un indicateur d’unités relatives (em ou ex).</span><span class="sxs-lookup"><span data-stu-id="b8c31-132">A number with an absolute units designator (cm, mm, in, pt, pc, or px) or a relative units designator (em or ex).</span></span> <span data-ttu-id="b8c31-133">Si aucune unité n’est donnée, les pixels (PX) sont pris en compte.</span><span class="sxs-lookup"><span data-stu-id="b8c31-133">If no units are given, pixels (px) is assumed.</span></span> <span data-ttu-id="b8c31-134">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="b8c31-134">The default value is 0.</span></span> |
| <span data-ttu-id="b8c31-135">percentage</span><span class="sxs-lookup"><span data-stu-id="b8c31-135">percentage</span></span> | <span data-ttu-id="b8c31-136">Valeur exprimée sous la forme d’un pourcentage de la hauteur de l’objet parent.</span><span class="sxs-lookup"><span data-stu-id="b8c31-136">Value expressed as a percentage of the parent object's height.</span></span>                                                                                                                                    |



 

<span data-ttu-id="b8c31-137">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b8c31-137">*VML Standard Attribute*</span></span>

<span data-ttu-id="b8c31-138">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="b8c31-138">**See Also**</span></span>

[<span data-ttu-id="b8c31-139">Unités</span><span class="sxs-lookup"><span data-stu-id="b8c31-139">Units</span></span>](msdn-online-vml-units.md)

<span data-ttu-id="b8c31-140">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b8c31-140">**Example**</span></span>

<span data-ttu-id="b8c31-141">La marge de gauche est définie à 25 pixels.</span><span class="sxs-lookup"><span data-stu-id="b8c31-141">The left margin is set to 25 pixels.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;margin-left:25px">
   </v:rect>
```



<span data-ttu-id="b8c31-142">[Exemple d’attribut margin-left](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span><span class="sxs-lookup"><span data-stu-id="b8c31-142">[Margin-Left Attribute Example](/previous-versions/visualstudio/design-tools/expression-studio-3/ee371308(v=expression.40)#examples).</span></span> <span data-ttu-id="b8c31-143">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="b8c31-143">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 