---
title: Origin, attribut (Fill) (VML)
description: Origin, attribut (Fill) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382768"
---
# <a name="origin-attribute-fillvml"></a><span data-ttu-id="ddaf1-103">Origin, attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="ddaf1-103">Origin Attribute (Fill)(VML)</span></span>

<span data-ttu-id="ddaf1-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ddaf1-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ddaf1-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ddaf1-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ddaf1-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ddaf1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ddaf1-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ddaf1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ddaf1-110">Définit le centre d’une image de remplissage.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-110">Defines the center of a fill image.</span></span> <span data-ttu-id="ddaf1-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-111">Read/write.</span></span> <span data-ttu-id="ddaf1-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ddaf1-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="ddaf1-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ddaf1-113">**Applies To**</span></span>

[<span data-ttu-id="ddaf1-114">Complète</span><span class="sxs-lookup"><span data-stu-id="ddaf1-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="ddaf1-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="ddaf1-115">**Tag Syntax**</span></span>

<span data-ttu-id="ddaf1-116"><v : *élément* Origin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ddaf1-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="ddaf1-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="ddaf1-117">**Script Syntax**</span></span>

<span data-ttu-id="ddaf1-118">*Element* . Origin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ddaf1-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="ddaf1-119">*expression* = *élément*. Origin</span><span class="sxs-lookup"><span data-stu-id="ddaf1-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="ddaf1-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ddaf1-120">**Remarks**</span></span>

<span data-ttu-id="ddaf1-121">Spécifie un point par rapport à l’angle supérieur gauche de l’image ; ce point est traité comme l’origine de l’image.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-121">Specifies a point relative to the upper left corner of the image; this point is treated as the origin of the image.</span></span> <span data-ttu-id="ddaf1-122">La valeur par défaut est le centre de l’image.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-122">Default is the center of the image.</span></span> <span data-ttu-id="ddaf1-123">Le vecteur est une fraction de la largeur et de la hauteur de l’image.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-123">The vector is a fraction of the width and height of the image.</span></span>

<span data-ttu-id="ddaf1-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="ddaf1-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="ddaf1-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ddaf1-125">**Example**</span></span>

<span data-ttu-id="ddaf1-126">L’image du remplissage est décalée vers la gauche jusqu’au point 50% de la largeur de la forme.</span><span class="sxs-lookup"><span data-stu-id="ddaf1-126">The image of the fill is shifted left to a point 50% of the width of the shape .</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 