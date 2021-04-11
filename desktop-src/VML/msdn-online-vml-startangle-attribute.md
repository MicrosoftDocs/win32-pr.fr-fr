---
title: Attribut VML StartAngle
description: Attribut VML StartAngle
ms.assetid: 334ae52a-cde4-427e-8080-ec789b4d9d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e779d343061ef65decb1dd21f615e054d561da28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031485"
---
# <a name="vml-startangle-attribute"></a><span data-ttu-id="6f24c-103">Attribut VML StartAngle</span><span class="sxs-lookup"><span data-stu-id="6f24c-103">VML StartAngle Attribute</span></span>

<span data-ttu-id="6f24c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6f24c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6f24c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6f24c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6f24c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="6f24c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6f24c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="6f24c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6f24c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6f24c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6f24c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6f24c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6f24c-110">Définit le point de départ de l’arc. Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6f24c-110">Defines the starting point of the arc. Read/write.</span></span> <span data-ttu-id="6f24c-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6f24c-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="6f24c-112">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6f24c-112">**Applies To**</span></span>

[<span data-ttu-id="6f24c-113">Arc</span><span class="sxs-lookup"><span data-stu-id="6f24c-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="6f24c-114">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="6f24c-114">**Tag Syntax**</span></span>

<span data-ttu-id="6f24c-115"><v : *Element* endAngle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6f24c-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="6f24c-116">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="6f24c-116">**Script Syntax**</span></span>

<span data-ttu-id="6f24c-117">*Element* . endAngle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6f24c-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="6f24c-118">*expression* = *élément*. endAngle</span><span class="sxs-lookup"><span data-stu-id="6f24c-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="6f24c-119">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="6f24c-119">**Remarks**</span></span>

<span data-ttu-id="6f24c-120">L’arc est défini en tant que trait dessiné le long d’un ovale délimité par les attributs de **style** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="6f24c-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="6f24c-121">Le début du trait est défini par un angle mesuré à partir de l’angle droit (12 heures) dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="6f24c-121">The start of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="6f24c-122">La valeur par défaut est 0 degré.</span><span class="sxs-lookup"><span data-stu-id="6f24c-122">The default value is 0 degrees.</span></span>

<span data-ttu-id="6f24c-123">Attribut standard VML</span><span class="sxs-lookup"><span data-stu-id="6f24c-123">VML Standard Attribute</span></span>

<span data-ttu-id="6f24c-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6f24c-124">**Example**</span></span>

<span data-ttu-id="6f24c-125">L’arc est souriant.</span><span class="sxs-lookup"><span data-stu-id="6f24c-125">The arc is smiling.</span></span> <span data-ttu-id="6f24c-126">Le point de départ est au point de 90 degré d’un ovale inscrit dans le cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="6f24c-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="6f24c-127">Le point de terminaison se trouve au point de 270 de l’ovale.</span><span class="sxs-lookup"><span data-stu-id="6f24c-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 