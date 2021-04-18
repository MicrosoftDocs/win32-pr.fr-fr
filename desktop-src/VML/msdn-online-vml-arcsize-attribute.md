---
title: Attribut VML de VML
description: Attribut VML de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512326"
---
# <a name="vml-arcsize-attribute"></a><span data-ttu-id="42e72-103">Attribut VML de VML</span><span class="sxs-lookup"><span data-stu-id="42e72-103">VML ArcSize Attribute</span></span>

<span data-ttu-id="42e72-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="42e72-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="42e72-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="42e72-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="42e72-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="42e72-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="42e72-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="42e72-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="42e72-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="42e72-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="42e72-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="42e72-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="42e72-110">Définit la quantité d’arrondi pour un rectangle arrondi.</span><span class="sxs-lookup"><span data-stu-id="42e72-110">Defines the amount of roundness for a rounded rectangle.</span></span> <span data-ttu-id="42e72-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="42e72-111">Read/write.</span></span> <span data-ttu-id="42e72-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="42e72-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="42e72-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="42e72-113">**Applies To**</span></span>

[<span data-ttu-id="42e72-114">RoundRect</span><span class="sxs-lookup"><span data-stu-id="42e72-114">RoundRect</span></span>](msdn-online-vml-roundrect-element.md)

<span data-ttu-id="42e72-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="42e72-115">**Tag Syntax**</span></span>

<span data-ttu-id="42e72-116"><v : *élément* d’arcs = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="42e72-116"><v: *element* arcsize=" *expression* "></span></span>

<span data-ttu-id="42e72-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="42e72-117">**Script Syntax**</span></span>

<span data-ttu-id="42e72-118">*Element* . arcs = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="42e72-118">*element* .arcSize="*expression*"</span></span>

<span data-ttu-id="42e72-119">*expression* = *Element*. arcs</span><span class="sxs-lookup"><span data-stu-id="42e72-119">*expression*=*element*.arcSize</span></span>

<span data-ttu-id="42e72-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="42e72-120">**Remarks**</span></span>

<span data-ttu-id="42e72-121">Définit les angles arrondis d’un rectangle à coins arrondis sous la forme d’un pourcentage de la plus petite dimension de la longueur et de la largeur d’un rectangle.</span><span class="sxs-lookup"><span data-stu-id="42e72-121">Defines the rounded corners of a rounded rectangle as a percentage of half the smaller dimension of the length and width of a rectangle.</span></span> <span data-ttu-id="42e72-122">0% aurait des angles carrés et 100% formerait des angles circulaires.</span><span class="sxs-lookup"><span data-stu-id="42e72-122">0% would have square corners, and 100% would form circular corners.</span></span> <span data-ttu-id="42e72-123">Un carré avec une valeur d' **interpolation** de 1,0 est un cercle.</span><span class="sxs-lookup"><span data-stu-id="42e72-123">A square with an **ArcSize** value of 1.0 would be a circle.</span></span> <span data-ttu-id="42e72-124">La valeur par défaut est 0,2 (20%).</span><span class="sxs-lookup"><span data-stu-id="42e72-124">The default value is 0.2 (20%).</span></span>

<span data-ttu-id="42e72-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="42e72-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="42e72-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="42e72-126">**Example**</span></span>

<span data-ttu-id="42e72-127">Le rectangle arrondi est dessiné avec des angles étroits et arrondis.</span><span class="sxs-lookup"><span data-stu-id="42e72-127">The rounded rectangle is drawn with tight-but-rounded corners.</span></span>


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 