---
title: ImageAlignShape VML (attribut)
description: ImageAlignShape VML (attribut)
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82aaab9c4c470b41bcf9fdb96ee2c048a7d0b81d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315618"
---
# <a name="vml-imagealignshape-attribute"></a><span data-ttu-id="40155-103">ImageAlignShape VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="40155-103">VML ImageAlignShape Attribute</span></span>

<span data-ttu-id="40155-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="40155-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="40155-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="40155-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="40155-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="40155-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="40155-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="40155-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="40155-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="40155-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="40155-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="40155-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="40155-110">Détermine l’alignement de l’image de trait.</span><span class="sxs-lookup"><span data-stu-id="40155-110">Determines the alignment of the stroke image.</span></span> <span data-ttu-id="40155-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="40155-111">Read/write.</span></span> <span data-ttu-id="40155-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="40155-112">**VgTriState**.</span></span>

<span data-ttu-id="40155-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="40155-113">**Applies To**</span></span>

[<span data-ttu-id="40155-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="40155-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="40155-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="40155-115">**Tag Syntax**</span></span>

<span data-ttu-id="40155-116"><v :</span><span class="sxs-lookup"><span data-stu-id="40155-116"><v:</span></span>

<span data-ttu-id="40155-117">élément *imagealignshape = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="40155-117">element *imagealignshape="* expression *">*</span></span>

<span data-ttu-id="40155-118">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="40155-118">**Script Syntax**</span></span>

<span data-ttu-id="40155-119">Element *. imagealignshape = "* expression *"*</span><span class="sxs-lookup"><span data-stu-id="40155-119">element *.imagealignshape="* expression *"*</span></span>

<span data-ttu-id="40155-120">*=* élément expression *. imagealignshape*</span><span class="sxs-lookup"><span data-stu-id="40155-120">expression *=* element *.imagealignshape*</span></span>

<span data-ttu-id="40155-121">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="40155-121">**Remarks**</span></span>

<span data-ttu-id="40155-122">Si la **valeur est true**, aligne l’image avec la forme, sinon aligne l’image avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="40155-122">If **True**, align the image with the shape, else align the image with the window.</span></span> <span data-ttu-id="40155-123">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="40155-123">The default is **True**.</span></span>

<span data-ttu-id="40155-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="40155-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="40155-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="40155-125">**Example**</span></span>

<span data-ttu-id="40155-126">L’image est alignée avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="40155-126">The image is aligned with the window.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 