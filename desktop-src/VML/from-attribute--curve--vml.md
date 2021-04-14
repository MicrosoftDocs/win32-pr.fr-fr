---
title: From, attribut (Curve) (VML)
description: From, attribut (Curve) (VML)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382680"
---
# <a name="from-attribute-curvevml"></a><span data-ttu-id="b35c6-103">From, attribut (Curve) (VML)</span><span class="sxs-lookup"><span data-stu-id="b35c6-103">From Attribute (Curve)(VML)</span></span>

<span data-ttu-id="b35c6-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b35c6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b35c6-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b35c6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b35c6-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b35c6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b35c6-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b35c6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b35c6-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b35c6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b35c6-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b35c6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b35c6-110">Définit le point de départ d’une courbe.</span><span class="sxs-lookup"><span data-stu-id="b35c6-110">Defines the starting point of a curve.</span></span> <span data-ttu-id="b35c6-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b35c6-111">Read/write.</span></span> <span data-ttu-id="b35c6-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="b35c6-112">**VgVector2D**.</span></span>

<span data-ttu-id="b35c6-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b35c6-113">**Applies To**</span></span>

[<span data-ttu-id="b35c6-114">Apprendre</span><span class="sxs-lookup"><span data-stu-id="b35c6-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="b35c6-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b35c6-115">**Tag Syntax**</span></span>

<span data-ttu-id="b35c6-116"><v : *élément* from = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b35c6-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="b35c6-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b35c6-117">**Script Syntax**</span></span>

<span data-ttu-id="b35c6-118">*Element* . from = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b35c6-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="b35c6-119">*expression* = *élément*. from</span><span class="sxs-lookup"><span data-stu-id="b35c6-119">*expression*=*element*.from</span></span>

<span data-ttu-id="b35c6-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b35c6-120">**Remarks**</span></span>

<span data-ttu-id="b35c6-121">Définit le point de départ d’une courbe de Bézier cubique dans l’espace de coordonnées de l’élément parent.</span><span class="sxs-lookup"><span data-stu-id="b35c6-121">Defines the starting point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="b35c6-122">Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié).</span><span class="sxs-lookup"><span data-stu-id="b35c6-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="b35c6-123">La valeur par défaut est 0, 0.</span><span class="sxs-lookup"><span data-stu-id="b35c6-123">Default is 0,0.</span></span>

<span data-ttu-id="b35c6-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b35c6-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="b35c6-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b35c6-125">**Example**</span></span>

<span data-ttu-id="b35c6-126">La courbe est souriante.</span><span class="sxs-lookup"><span data-stu-id="b35c6-126">The curve is smiling.</span></span> <span data-ttu-id="b35c6-127">Elle commence à gauche et se termine à droite.</span><span class="sxs-lookup"><span data-stu-id="b35c6-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="b35c6-128">Les deux points de contrôle sont situés le long de la procédure de façon à extraire la courbe vers le dessous pour obtenir l’apparence d’un sourire.</span><span class="sxs-lookup"><span data-stu-id="b35c6-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 