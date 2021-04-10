---
title: Attribut Z-index VML
description: Attribut Z-index VML
ms.assetid: 54a2c556-e40e-462e-a621-ec07911d5261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc358719f3fa15fa40293e40eef924bd248286c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941056"
---
# <a name="vml-z-index-attribute"></a><span data-ttu-id="d6343-103">Attribut Z-index VML</span><span class="sxs-lookup"><span data-stu-id="d6343-103">VML Z-Index Attribute</span></span>

<span data-ttu-id="d6343-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d6343-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6343-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d6343-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6343-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d6343-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6343-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d6343-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6343-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6343-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6343-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6343-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6343-110">Détermine l’ordre d’affichage des formes qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="d6343-110">Determines the display order of overlapping shapes.</span></span> <span data-ttu-id="d6343-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d6343-111">Read/write.</span></span> <span data-ttu-id="d6343-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="d6343-112">**String**.</span></span>

<span data-ttu-id="d6343-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d6343-113">**Applies To**</span></span>

[<span data-ttu-id="d6343-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="d6343-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="d6343-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d6343-115">**Tag Syntax**</span></span>

<span data-ttu-id="d6343-116"><v : *Element* style = "z-index : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d6343-116"><v: *element* style="z-index: *expression* "></span></span>

<span data-ttu-id="d6343-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d6343-117">**Script Syntax**</span></span>

<span data-ttu-id="d6343-118">*Element* . style. ZIndex = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d6343-118">*element* .style.zindex="*expression*"</span></span>

<span data-ttu-id="d6343-119">*expression* = *Element*. style. ZIndex</span><span class="sxs-lookup"><span data-stu-id="d6343-119">*expression*=*element*.style.zindex</span></span>

<span data-ttu-id="d6343-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d6343-120">**Remarks**</span></span>

<span data-ttu-id="d6343-121">L’attribut **z-index** est similaire à l’attribut **z-index** HTML standard pour les styles.</span><span class="sxs-lookup"><span data-stu-id="d6343-121">The **Z-Index** attribute is similar to the standard HTML **Z-Index** attribute for styles.</span></span>

<span data-ttu-id="d6343-122">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="d6343-122">Values include:</span></span>



| <span data-ttu-id="d6343-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6343-123">Value</span></span> | <span data-ttu-id="d6343-124">Description</span><span class="sxs-lookup"><span data-stu-id="d6343-124">Description</span></span>                                                                                                                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6343-125">Auto</span><span class="sxs-lookup"><span data-stu-id="d6343-125">Auto</span></span>  | <span data-ttu-id="d6343-126">L’ordre dans lequel les formes apparaissent dans la page HTML sera utilisé, de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="d6343-126">The order that the shapes appear in the HTML page will be used, bottom to top.</span></span>                                                                                                                         |
| <span data-ttu-id="d6343-127">order</span><span class="sxs-lookup"><span data-stu-id="d6343-127">order</span></span> | <span data-ttu-id="d6343-128">Nombre qui représente la priorité d’empilage.</span><span class="sxs-lookup"><span data-stu-id="d6343-128">A number that represents the stacking precedence.</span></span> <span data-ttu-id="d6343-129">Une forme avec un nombre plus élevé s’affiche comme si elle wereoverlapping (au début) d’une forme avec un nombre inférieur.</span><span class="sxs-lookup"><span data-stu-id="d6343-129">A shape with a a higher number will be displayed as if it wereoverlapping (in "front" of) a shape with a lower number.</span></span> <span data-ttu-id="d6343-130">Vous pouvez utiliser des nombres négatifs.</span><span class="sxs-lookup"><span data-stu-id="d6343-130">Negative numbers can be used.</span></span> |



 

<span data-ttu-id="d6343-131">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="d6343-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="d6343-132">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="d6343-132">**Example**</span></span>

<span data-ttu-id="d6343-133">La forme rouge s’affiche dans l’avant de la forme bleue, car elle a un index z plus élevé.</span><span class="sxs-lookup"><span data-stu-id="d6343-133">The red shape will be displayed in "front" of the blue shape, because it has a higher z-index.</span></span>


```HTML
   <v:rect id=bluerect fillcolor="blue"
   style="position:relative;top:1;left:1;width:20;height:20;z-index:1">
   </v:rect>
   <v:rect id=redrect fillcolor="red"
   style="position:relative;top:10;left:10;width:20;height:20;z-index:2">
   </v:rect>
```



<span data-ttu-id="d6343-134">[Exemple d’attribut Z-index](/previous-versions/ms530275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d6343-134">[Z-Index Attribute Example](/previous-versions/ms530275(v=vs.85)).</span></span> <span data-ttu-id="d6343-135">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="d6343-135">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 