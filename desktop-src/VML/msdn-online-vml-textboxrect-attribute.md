---
title: TextBoxRect VML (attribut)
description: TextBoxRect VML (attribut)
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031308"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="c2867-103">TextBoxRect VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="c2867-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="c2867-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c2867-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c2867-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c2867-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c2867-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c2867-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c2867-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c2867-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c2867-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c2867-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c2867-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c2867-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c2867-110">Définit une ou plusieurs zones de texte à l’intérieur d’une forme.</span><span class="sxs-lookup"><span data-stu-id="c2867-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="c2867-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c2867-111">Read/write.</span></span> <span data-ttu-id="c2867-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="c2867-112">**String**.</span></span>

<span data-ttu-id="c2867-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c2867-113">**Applies To**</span></span>

[<span data-ttu-id="c2867-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c2867-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="c2867-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c2867-115">**Tag Syntax**</span></span>

<span data-ttu-id="c2867-116"><v : *Element* textboxrect = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c2867-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="c2867-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c2867-117">**Script Syntax**</span></span>

<span data-ttu-id="c2867-118">*Element* . textboxrect = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c2867-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="c2867-119">*expression* = *élément*. textboxrect</span><span class="sxs-lookup"><span data-stu-id="c2867-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="c2867-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c2867-120">**Remarks**</span></span>

<span data-ttu-id="c2867-121">Une zone de texte est définie par un ou plusieurs ensembles de nombres spécifiant (dans l’ordre) les points gauche, supérieur, droit et inférieur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="c2867-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="c2867-122">Les jeux multiples sont délimités par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="c2867-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="c2867-123">La valeur par défaut est la même valeur de dimension que le rectangle conteneur.</span><span class="sxs-lookup"><span data-stu-id="c2867-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="c2867-124">Si plusieurs zones de texte sont définies, les jeux quadruples délimités par des virgules qui définissent chaque zone de texte sont séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="c2867-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="c2867-125">Normalement, les zones de texte sont des jeux de 1, 2, 3 ou 6 rectangles sur une forme.</span><span class="sxs-lookup"><span data-stu-id="c2867-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="c2867-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c2867-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="c2867-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c2867-127">**Example**</span></span>

<span data-ttu-id="c2867-128">Une zone de texte de 95 unités par unité de 95 est définie et placée 5 unités dans le coin supérieur gauche de la forme.</span><span class="sxs-lookup"><span data-stu-id="c2867-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 