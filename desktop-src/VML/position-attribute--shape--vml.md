---
title: Position, attribut (Shape) (VML)
description: Position, attribut (Shape) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382763"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="94235-103">Position, attribut (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="94235-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="94235-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="94235-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="94235-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="94235-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="94235-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="94235-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="94235-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="94235-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="94235-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="94235-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="94235-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="94235-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="94235-110">Définit le type de positionnement utilisé pour placer un élément.</span><span class="sxs-lookup"><span data-stu-id="94235-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="94235-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="94235-111">Read/write.</span></span> <span data-ttu-id="94235-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="94235-112">**String**.</span></span>

<span data-ttu-id="94235-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="94235-113">**Applies To**</span></span>

[<span data-ttu-id="94235-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="94235-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="94235-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="94235-115">**Tag Syntax**</span></span>

<span data-ttu-id="94235-116"><v : *Element* style = "position : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="94235-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="94235-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="94235-117">**Script Syntax**</span></span>

<span data-ttu-id="94235-118">*Element* . style. position = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="94235-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="94235-119">*expression* = *Element*. style. position</span><span class="sxs-lookup"><span data-stu-id="94235-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="94235-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="94235-120">**Remarks**</span></span>

<span data-ttu-id="94235-121">L’attribut **position** est semblable à l’attribut **position** HTML standard utilisé avec les feuilles de style.</span><span class="sxs-lookup"><span data-stu-id="94235-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="94235-122">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="94235-122">Values include:</span></span>



| <span data-ttu-id="94235-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="94235-123">Value</span></span>    | <span data-ttu-id="94235-124">Description</span><span class="sxs-lookup"><span data-stu-id="94235-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94235-125">static</span><span class="sxs-lookup"><span data-stu-id="94235-125">static</span></span>   | <span data-ttu-id="94235-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="94235-126">Default.</span></span> <span data-ttu-id="94235-127">L’élément est positionné en fonction du déroulement normal de la page.</span><span class="sxs-lookup"><span data-stu-id="94235-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="94235-128">Les attributs **Top** et **Left** sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="94235-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="94235-129">Si l’objet est ancré en ligne, ce qui se produit uniquement dans Microsoft Word, cette valeur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="94235-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="94235-130">absolute</span><span class="sxs-lookup"><span data-stu-id="94235-130">absolute</span></span> | <span data-ttu-id="94235-131">L’élément est positionné par rapport au parent, à l’aide des attributs **Top** et **Left** .</span><span class="sxs-lookup"><span data-stu-id="94235-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="94235-132">Cette valeur est utilisée par les objets flottants Microsoft Word et Microsoft Excel, ainsi que par les diapositives Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="94235-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="94235-133">relative</span><span class="sxs-lookup"><span data-stu-id="94235-133">relative</span></span> | <span data-ttu-id="94235-134">L’élément est positionné en fonction du déroulement normal de la page, mais les attributs **supérieur** et **gauche** sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="94235-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="94235-135">Le chevauchement des éléments qui se chevauchent est régi par l’attribut **Z-index** .</span><span class="sxs-lookup"><span data-stu-id="94235-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="94235-136">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="94235-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="94235-137">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="94235-137">**Example**</span></span>

<span data-ttu-id="94235-138">La position du rectangle est affichée à l’aide du style *relatif* .</span><span class="sxs-lookup"><span data-stu-id="94235-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="94235-139">[Exemple d’attribut position](/previous-versions/bb264090(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="94235-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="94235-140">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="94235-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 