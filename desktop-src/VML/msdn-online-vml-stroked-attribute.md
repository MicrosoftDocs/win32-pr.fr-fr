---
title: Attribut Stroke VML
description: Attribut Stroke VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102273"
---
# <a name="vml-stroked-attribute"></a><span data-ttu-id="ed7b8-103">Attribut Stroke VML</span><span class="sxs-lookup"><span data-stu-id="ed7b8-103">VML Stroked Attribute</span></span>

<span data-ttu-id="ed7b8-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ed7b8-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ed7b8-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ed7b8-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ed7b8-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ed7b8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ed7b8-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ed7b8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ed7b8-110">Définit si le chemin d’accès doit être rayé.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-110">Defines whether the path will be stroked.</span></span> <span data-ttu-id="ed7b8-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-111">Read/write.</span></span> <span data-ttu-id="ed7b8-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span><span class="sxs-lookup"><span data-stu-id="ed7b8-112">[VgTriState](msdn-online-vml-vgtristate.md) .</span></span>

<span data-ttu-id="ed7b8-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ed7b8-113">**Applies To**</span></span>

[<span data-ttu-id="ed7b8-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="ed7b8-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ed7b8-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="ed7b8-115">**Tag Syntax**</span></span>

<span data-ttu-id="ed7b8-116"><v : *élément* rayé = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ed7b8-116"><v: *element* stroked=" *expression* "></span></span>

<span data-ttu-id="ed7b8-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="ed7b8-117">**Script Syntax**</span></span>

<span data-ttu-id="ed7b8-118">*Element* . stroked = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ed7b8-118">*element* .stroked="*expression*"</span></span>

<span data-ttu-id="ed7b8-119">*expression* = *élément*. traitd</span><span class="sxs-lookup"><span data-stu-id="ed7b8-119">*expression*=*element*.stroked</span></span>

<span data-ttu-id="ed7b8-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ed7b8-120">**Remarks**</span></span>

<span data-ttu-id="ed7b8-121">La valeur est dupliquée à partir de l’attribut **on** de l’élément [Stroke](msdn-online-vml-stroke-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ed7b8-121">The value is duplicated from the **On** attribute of the [Stroke](msdn-online-vml-stroke-element.md) element.</span></span>

<span data-ttu-id="ed7b8-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="ed7b8-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="ed7b8-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ed7b8-123">**Example**</span></span>

<span data-ttu-id="ed7b8-124">Le tracé de la forme est rayé.</span><span class="sxs-lookup"><span data-stu-id="ed7b8-124">The shape path is stroked.</span></span>


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="ed7b8-125">[Exemple d’attribut rayé](/previous-versions/bb264094(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ed7b8-125">[Stroked Attribute Example](/previous-versions/bb264094(v=vs.85)).</span></span> <span data-ttu-id="ed7b8-126">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="ed7b8-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 