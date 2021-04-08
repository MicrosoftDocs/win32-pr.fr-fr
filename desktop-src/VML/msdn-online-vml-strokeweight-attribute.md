---
title: StrokeWeight VML (attribut)
description: StrokeWeight VML (attribut)
ms.assetid: 364882b2-e5f4-4a86-b7d7-352f8780ebdc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8da9f7220315b066676f2439f37b97250cc7c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728069"
---
# <a name="vml-strokeweight-attribute"></a><span data-ttu-id="a1438-103">StrokeWeight VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="a1438-103">VML StrokeWeight Attribute</span></span>

<span data-ttu-id="a1438-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a1438-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a1438-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a1438-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a1438-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a1438-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a1438-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a1438-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a1438-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a1438-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a1438-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a1438-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a1438-110">Définit l’épaisseur du pinceau qui dessine le tracé d’une forme.</span><span class="sxs-lookup"><span data-stu-id="a1438-110">Defines the brush thickness that strokes the path of a shape.</span></span> <span data-ttu-id="a1438-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a1438-111">Read/write.</span></span> <span data-ttu-id="a1438-112">**VGLength**.</span><span class="sxs-lookup"><span data-stu-id="a1438-112">**VGLength**.</span></span>

<span data-ttu-id="a1438-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a1438-113">**Applies To**</span></span>

[<span data-ttu-id="a1438-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="a1438-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a1438-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a1438-115">**Tag Syntax**</span></span>

<span data-ttu-id="a1438-116"><v : *Element* StrokeWeight = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a1438-116"><v: *element* strokeweight=" *expression* "></span></span>

<span data-ttu-id="a1438-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="a1438-117">**Script Syntax**</span></span>

<span data-ttu-id="a1438-118">*Element* . StrokeWeight = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a1438-118">*element* .strokeweight="*expression*"</span></span>

<span data-ttu-id="a1438-119">*expression* = *élément*. StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="a1438-119">*expression*=*element*.strokeweight</span></span>

<span data-ttu-id="a1438-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a1438-120">**Remarks**</span></span>

<span data-ttu-id="a1438-121">La valeur est dupliquée à partir de l’attribut **Weight** de l’élément **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="a1438-121">The value is duplicated from the **Weight** attribute of the **Stroke** element.</span></span> <span data-ttu-id="a1438-122">Si un nombre est spécifié, mais qu’aucune unité n’est ajoutée, l’unité de mesure par défaut est l’UME.</span><span class="sxs-lookup"><span data-stu-id="a1438-122">If a number is specified, but no units are added, the default unit of measurement is the Emu.</span></span> <span data-ttu-id="a1438-123">Si aucune valeur n’est spécifiée, la valeur par défaut est 1 pixel (1px).</span><span class="sxs-lookup"><span data-stu-id="a1438-123">If no value is specified, the default is 1 pixel (1px).</span></span>

<span data-ttu-id="a1438-124">Pour les scripts, toutefois, l’unité de mesure par défaut est en points.</span><span class="sxs-lookup"><span data-stu-id="a1438-124">For scripting, however, the default unit of measurement is in points.</span></span>

<span data-ttu-id="a1438-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="a1438-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="a1438-126">**Voir aussi**</span><span class="sxs-lookup"><span data-stu-id="a1438-126">**See Also**</span></span>

<span data-ttu-id="a1438-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span><span class="sxs-lookup"><span data-stu-id="a1438-127">[Stroke](msdn-online-vml-stroke-element.md), [IVgLength](msdn-online-vml-vglength.md), [Units](msdn-online-vml-units.md)</span></span>

<span data-ttu-id="a1438-128">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a1438-128">**Example**</span></span>

<span data-ttu-id="a1438-129">L’épaisseur du trait de la forme est 1 point.</span><span class="sxs-lookup"><span data-stu-id="a1438-129">The stroke weight of the shape is 1 point.</span></span>


```HTML
   <v:shape id="rect01" strokeweight="1pt"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="a1438-130">[Exemple d’attribut StrokeWeight](/previous-versions/bb264095(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a1438-130">[StrokeWeight Attribute Example](/previous-versions/bb264095(v=vs.85)).</span></span> <span data-ttu-id="a1438-131">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="a1438-131">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 