---
title: FillType VML (attribut)
description: FillType VML (attribut)
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941342"
---
# <a name="vml-filltype-attribute"></a><span data-ttu-id="5f53c-103">FillType VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="5f53c-103">VML FillType Attribute</span></span>

<span data-ttu-id="5f53c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5f53c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5f53c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5f53c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5f53c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="5f53c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5f53c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="5f53c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5f53c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5f53c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5f53c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5f53c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5f53c-110">Définit le type de remplissage utilisé pour l’arrière-plan d’un trait.</span><span class="sxs-lookup"><span data-stu-id="5f53c-110">Defines the type of fill used for the background of a stroke.</span></span> <span data-ttu-id="5f53c-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5f53c-111">Read/write.</span></span> <span data-ttu-id="5f53c-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="5f53c-112">**VgFillType**.</span></span>

<span data-ttu-id="5f53c-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5f53c-113">**Applies To**</span></span>

[<span data-ttu-id="5f53c-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="5f53c-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="5f53c-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="5f53c-115">**Tag Syntax**</span></span>

<span data-ttu-id="5f53c-116"><v : *Element* fillType = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5f53c-116"><v: *element* filltype=" *expression* "></span></span>

<span data-ttu-id="5f53c-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="5f53c-117">**Script Syntax**</span></span>

<span data-ttu-id="5f53c-118">*Element* . fillType = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5f53c-118">*element* .filltype="*expression*"</span></span>

<span data-ttu-id="5f53c-119">*expression* = *élément*. fillType</span><span class="sxs-lookup"><span data-stu-id="5f53c-119">*expression*=*element*.filltype</span></span>

<span data-ttu-id="5f53c-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5f53c-120">**Remarks**</span></span>

<span data-ttu-id="5f53c-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="5f53c-121">Values include:</span></span>



| <span data-ttu-id="5f53c-122">DashStyle</span><span class="sxs-lookup"><span data-stu-id="5f53c-122">DashStyle</span></span> | <span data-ttu-id="5f53c-123">Description</span><span class="sxs-lookup"><span data-stu-id="5f53c-123">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="5f53c-124">Unie</span><span class="sxs-lookup"><span data-stu-id="5f53c-124">Solid</span></span>     | <span data-ttu-id="5f53c-125">Le motif de remplissage est plein.</span><span class="sxs-lookup"><span data-stu-id="5f53c-125">The fill pattern is solid.</span></span> <span data-ttu-id="5f53c-126">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5f53c-126">Default value.</span></span>      |
| <span data-ttu-id="5f53c-127">Tile</span><span class="sxs-lookup"><span data-stu-id="5f53c-127">Tile</span></span>      | <span data-ttu-id="5f53c-128">L’image de remplissage est en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="5f53c-128">The fill image is tiled.</span></span>                       |
| <span data-ttu-id="5f53c-129">Modèle</span><span class="sxs-lookup"><span data-stu-id="5f53c-129">Pattern</span></span>   | <span data-ttu-id="5f53c-130">L’image de remplissage est étirée pour former un modèle.</span><span class="sxs-lookup"><span data-stu-id="5f53c-130">The fill image is stretched to form a pattern.</span></span> |
| <span data-ttu-id="5f53c-131">Frame</span><span class="sxs-lookup"><span data-stu-id="5f53c-131">Frame</span></span>     | <span data-ttu-id="5f53c-132">L’image de remplissage devient une bordure pour la forme.</span><span class="sxs-lookup"><span data-stu-id="5f53c-132">The fill image becomes a border for the shape.</span></span> |



 

<span data-ttu-id="5f53c-133">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="5f53c-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="5f53c-134">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="5f53c-134">**Example**</span></span>

<span data-ttu-id="5f53c-135">Le trait de la forme a une texture en mosaïque créée à partir de l’image cylinder.gif.</span><span class="sxs-lookup"><span data-stu-id="5f53c-135">The stroke of the shape has a tiled texture created from the cylinder.gif image.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 