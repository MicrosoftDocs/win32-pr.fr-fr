---
title: EndAngle VML (attribut)
description: EndAngle VML (attribut)
ms.assetid: fc8276dc-8f61-42f4-b405-e92ca31e4637
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b22f157a1ccfc2337baa0bb5de747332bb78d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316361"
---
# <a name="vml-endangle-attribute"></a><span data-ttu-id="9a8c0-103">EndAngle VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="9a8c0-103">VML EndAngle Attribute</span></span>

<span data-ttu-id="9a8c0-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9a8c0-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9a8c0-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9a8c0-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9a8c0-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9a8c0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9a8c0-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9a8c0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9a8c0-110">Définit le point de terminaison de l’arc. Lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-110">Defines the endpoint of the arc. Read/write.</span></span> <span data-ttu-id="9a8c0-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9a8c0-111">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="9a8c0-112">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9a8c0-112">**Applies To**</span></span>

[<span data-ttu-id="9a8c0-113">Arc</span><span class="sxs-lookup"><span data-stu-id="9a8c0-113">Arc</span></span>](msdn-online-vml-arc-element.md)

<span data-ttu-id="9a8c0-114">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9a8c0-114">**Tag Syntax**</span></span>

<span data-ttu-id="9a8c0-115"><v : *Element* endAngle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9a8c0-115"><v: *element* endangle=" *expression* "></span></span>

<span data-ttu-id="9a8c0-116">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="9a8c0-116">**Script Syntax**</span></span>

<span data-ttu-id="9a8c0-117">*Element* . endAngle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9a8c0-117">*element* .endAngle="*expression*"</span></span>

<span data-ttu-id="9a8c0-118">*expression* = *élément*. endAngle</span><span class="sxs-lookup"><span data-stu-id="9a8c0-118">*expression*=*element*.endAngle</span></span>

<span data-ttu-id="9a8c0-119">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9a8c0-119">**Remarks**</span></span>

<span data-ttu-id="9a8c0-120">L’arc est défini en tant que trait dessiné le long d’un ovale délimité par les attributs de **style** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-120">The arc is defined as a stroke drawn along an oval bounded by the **Style** attributes of a shape.</span></span> <span data-ttu-id="9a8c0-121">La fin du trait est définie par un angle mesuré à partir de l’angle droit (12 heures) dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-121">The end of the stroke is defined by an angle measured from straight up (12 o'clock) clockwise.</span></span> <span data-ttu-id="9a8c0-122">La valeur par défaut est 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-122">The default value is 90 degrees.</span></span>

<span data-ttu-id="9a8c0-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="9a8c0-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9a8c0-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9a8c0-124">**Example**</span></span>

<span data-ttu-id="9a8c0-125">L’arc est souriant.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-125">The arc is smiling.</span></span> <span data-ttu-id="9a8c0-126">Le point de départ est au point de 90 degré d’un ovale inscrit dans le cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-126">The start point is at the 90-degree point of an oval inscribed inside the shape bounding box.</span></span> <span data-ttu-id="9a8c0-127">Le point de terminaison se trouve au point de 270 de l’ovale.</span><span class="sxs-lookup"><span data-stu-id="9a8c0-127">The end point is at the 270-degree point of the oval.</span></span>


```HTML
   <v:arc id="myarc"
   style="position:relative;top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```



 

 