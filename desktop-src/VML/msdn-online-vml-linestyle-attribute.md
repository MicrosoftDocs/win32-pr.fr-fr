---
title: VML (attribut LineStyle)
description: VML (attribut LineStyle)
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e69371e61a3d81f97de0243af19381f36c0555
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727428"
---
# <a name="vml-linestyle-attribute"></a><span data-ttu-id="68c22-103">VML (attribut LineStyle)</span><span class="sxs-lookup"><span data-stu-id="68c22-103">VML LineStyle Attribute</span></span>

<span data-ttu-id="68c22-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="68c22-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="68c22-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="68c22-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="68c22-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="68c22-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="68c22-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="68c22-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="68c22-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="68c22-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="68c22-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="68c22-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="68c22-110">Définit le style de ligne du trait.</span><span class="sxs-lookup"><span data-stu-id="68c22-110">Defines the line style of the stroke.</span></span> <span data-ttu-id="68c22-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="68c22-111">Read/write.</span></span> <span data-ttu-id="68c22-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="68c22-112">**String**.</span></span>

<span data-ttu-id="68c22-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="68c22-113">**Applies To**</span></span>

[<span data-ttu-id="68c22-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="68c22-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="68c22-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="68c22-115">**Tag Syntax**</span></span>

<span data-ttu-id="68c22-116"><v : *élément* LineStyle = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="68c22-116"><v: *element* linestyle=" *expression* "></span></span>

<span data-ttu-id="68c22-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="68c22-117">**Script Syntax**</span></span>

<span data-ttu-id="68c22-118">*Element* . LineStyle = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="68c22-118">*element* .linestyle="*expression*"</span></span>

<span data-ttu-id="68c22-119">*expression* = *Element*. LineStyle</span><span class="sxs-lookup"><span data-stu-id="68c22-119">*expression*=*element*.linestyle</span></span>

<span data-ttu-id="68c22-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="68c22-120">**Remarks**</span></span>

<span data-ttu-id="68c22-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="68c22-121">Values include:</span></span>

-   <span data-ttu-id="68c22-122">Unique (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="68c22-122">Single (default)</span></span>
-   <span data-ttu-id="68c22-123">ThinThin</span><span class="sxs-lookup"><span data-stu-id="68c22-123">ThinThin</span></span>
-   <span data-ttu-id="68c22-124">ThinThick</span><span class="sxs-lookup"><span data-stu-id="68c22-124">ThinThick</span></span>
-   <span data-ttu-id="68c22-125">ThickThin</span><span class="sxs-lookup"><span data-stu-id="68c22-125">ThickThin</span></span>
-   <span data-ttu-id="68c22-126">ThickBetweenThin</span><span class="sxs-lookup"><span data-stu-id="68c22-126">ThickBetweenThin</span></span>

<span data-ttu-id="68c22-127">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="68c22-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="68c22-128">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="68c22-128">**Example**</span></span>

<span data-ttu-id="68c22-129">Une double ligne est dessinée avec deux traits fins.</span><span class="sxs-lookup"><span data-stu-id="68c22-129">A double line is drawn with two thin strokes.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 