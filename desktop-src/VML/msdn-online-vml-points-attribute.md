---
title: Attribut points VML
description: Attribut points VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031335"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="7d980-103">Attribut points VML</span><span class="sxs-lookup"><span data-stu-id="7d980-103">VML Points Attribute</span></span>

<span data-ttu-id="7d980-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7d980-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7d980-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7d980-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7d980-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="7d980-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7d980-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="7d980-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7d980-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7d980-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7d980-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7d980-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7d980-110">Définit un ensemble de points qui composent une polyligne.</span><span class="sxs-lookup"><span data-stu-id="7d980-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="7d980-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7d980-111">Read/write.</span></span> <span data-ttu-id="7d980-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="7d980-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="7d980-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7d980-113">**Applies To**</span></span>

[<span data-ttu-id="7d980-114">Polyligne</span><span class="sxs-lookup"><span data-stu-id="7d980-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="7d980-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="7d980-115">**Tag Syntax**</span></span>

<span data-ttu-id="7d980-116"><v : *Element* points = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7d980-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="7d980-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="7d980-117">**Script Syntax**</span></span>

<span data-ttu-id="7d980-118">*Element* . points = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="7d980-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="7d980-119">*expression* = *Element*. points</span><span class="sxs-lookup"><span data-stu-id="7d980-119">*expression*=*element*.points</span></span>

<span data-ttu-id="7d980-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="7d980-120">**Remarks**</span></span>

<span data-ttu-id="7d980-121">Définit un ensemble de segments de ligne droite composés d’une série de points.</span><span class="sxs-lookup"><span data-stu-id="7d980-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="7d980-122">Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié).</span><span class="sxs-lookup"><span data-stu-id="7d980-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="7d980-123">La valeur par défaut est « 0, 0 10, 10 ».</span><span class="sxs-lookup"><span data-stu-id="7d980-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="7d980-124">Notez que les virgules ne sont pas requises, mais qu’elles facilitent la lisibilité.</span><span class="sxs-lookup"><span data-stu-id="7d980-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="7d980-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="7d980-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="7d980-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="7d980-126">**Example**</span></span>

<span data-ttu-id="7d980-127">La polyligne commence au point 10, 10 et se termine à 100 100, avec les valeurs de points.</span><span class="sxs-lookup"><span data-stu-id="7d980-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 