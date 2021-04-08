---
title: From, attribut (Line) (VML)
description: From, attribut (Line) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730005"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="898aa-103">From, attribut (Line) (VML)</span><span class="sxs-lookup"><span data-stu-id="898aa-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="898aa-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="898aa-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="898aa-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="898aa-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="898aa-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="898aa-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="898aa-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="898aa-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="898aa-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="898aa-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="898aa-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="898aa-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="898aa-110">Définit le point de départ d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="898aa-110">Defines the starting point of a line.</span></span> <span data-ttu-id="898aa-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="898aa-111">Read/write.</span></span> <span data-ttu-id="898aa-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="898aa-112">**VgVector2D**.</span></span>

<span data-ttu-id="898aa-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="898aa-113">**Applies To**</span></span>

[<span data-ttu-id="898aa-114">Ligne</span><span class="sxs-lookup"><span data-stu-id="898aa-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="898aa-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="898aa-115">**Tag Syntax**</span></span>

<span data-ttu-id="898aa-116"><v : *élément* from = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="898aa-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="898aa-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="898aa-117">**Script Syntax**</span></span>

<span data-ttu-id="898aa-118">*Element* . from = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="898aa-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="898aa-119">*expression* = *élément*. from</span><span class="sxs-lookup"><span data-stu-id="898aa-119">*expression*=*element*.from</span></span>

<span data-ttu-id="898aa-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="898aa-120">**Remarks**</span></span>

<span data-ttu-id="898aa-121">Définit le point de départ de la ligne dans l’espace de coordonnées de l’élément parent. Si le parent n’est pas un élément VML, l' [unité](msdn-online-vml-units.md) par défaut est un pixel (mais dans, cm, mm, PT, PC peut également être spécifié).</span><span class="sxs-lookup"><span data-stu-id="898aa-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="898aa-122">La valeur par défaut est 0, 0.</span><span class="sxs-lookup"><span data-stu-id="898aa-122">Default is 0,0.</span></span>

<span data-ttu-id="898aa-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="898aa-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="898aa-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="898aa-124">**Example**</span></span>

<span data-ttu-id="898aa-125">La ligne commence à un emplacement de 10 points vers le haut et de 10 points à droite du coin supérieur gauche de l’espace parent.</span><span class="sxs-lookup"><span data-stu-id="898aa-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 