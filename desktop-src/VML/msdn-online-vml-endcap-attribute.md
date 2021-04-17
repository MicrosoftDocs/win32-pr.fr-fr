---
title: Attribut d’extrémité de VML
description: Attribut d’extrémité de VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316416"
---
# <a name="vml-endcap-attribute"></a><span data-ttu-id="15a0b-103">Attribut d’extrémité de VML</span><span class="sxs-lookup"><span data-stu-id="15a0b-103">VML EndCap Attribute</span></span>

<span data-ttu-id="15a0b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="15a0b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="15a0b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="15a0b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="15a0b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="15a0b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="15a0b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="15a0b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="15a0b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="15a0b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="15a0b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="15a0b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="15a0b-110">Définit le style d’extrémité pour la fin d’un trait.</span><span class="sxs-lookup"><span data-stu-id="15a0b-110">Defines the cap style for the end of a stroke.</span></span> <span data-ttu-id="15a0b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="15a0b-111">Read/write.</span></span> <span data-ttu-id="15a0b-112">**VgLineEndCapStyle**.</span><span class="sxs-lookup"><span data-stu-id="15a0b-112">**VgLineEndCapStyle**.</span></span>

<span data-ttu-id="15a0b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="15a0b-113">**Applies To**</span></span>

[<span data-ttu-id="15a0b-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="15a0b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="15a0b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="15a0b-115">**Tag Syntax**</span></span>

<span data-ttu-id="15a0b-116"><v : *Element* reextrémité = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="15a0b-116"><v: *element* endcap=" *expression* "></span></span>

<span data-ttu-id="15a0b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="15a0b-117">**Script Syntax**</span></span>

<span data-ttu-id="15a0b-118">*Element* . Extremity = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="15a0b-118">*element* .endcap="*expression*"</span></span>

<span data-ttu-id="15a0b-119">*expression* = *Element*. extrémité</span><span class="sxs-lookup"><span data-stu-id="15a0b-119">*expression*=*element*.endcap</span></span>

<span data-ttu-id="15a0b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="15a0b-120">**Remarks**</span></span>

<span data-ttu-id="15a0b-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="15a0b-121">Values include:</span></span>

-   <span data-ttu-id="15a0b-122">Plat (par défaut)</span><span class="sxs-lookup"><span data-stu-id="15a0b-122">Flat (default)</span></span>
-   <span data-ttu-id="15a0b-123">Carré</span><span class="sxs-lookup"><span data-stu-id="15a0b-123">Square</span></span>
-   <span data-ttu-id="15a0b-124">Round</span><span class="sxs-lookup"><span data-stu-id="15a0b-124">Round</span></span>

<span data-ttu-id="15a0b-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="15a0b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="15a0b-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="15a0b-126">**Example**</span></span>

<span data-ttu-id="15a0b-127">Une ligne est dessinée avec un embout plat à la fin du trait.</span><span class="sxs-lookup"><span data-stu-id="15a0b-127">A line is drawn with a flat cap on the end of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 