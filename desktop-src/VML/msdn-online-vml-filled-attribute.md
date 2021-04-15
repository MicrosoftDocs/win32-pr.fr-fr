---
title: Attribut rempli VML
description: Attribut rempli VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463679"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="b0a16-103">Attribut rempli VML</span><span class="sxs-lookup"><span data-stu-id="b0a16-103">VML Filled Attribute</span></span>

<span data-ttu-id="b0a16-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b0a16-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b0a16-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b0a16-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b0a16-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b0a16-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b0a16-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b0a16-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b0a16-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b0a16-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b0a16-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b0a16-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b0a16-110">Détermine si le tracé fermé est rempli.</span><span class="sxs-lookup"><span data-stu-id="b0a16-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="b0a16-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b0a16-111">Read/write.</span></span> <span data-ttu-id="b0a16-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b0a16-112">**VgTriState**.</span></span>

<span data-ttu-id="b0a16-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b0a16-113">**Applies To**</span></span>

[<span data-ttu-id="b0a16-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="b0a16-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b0a16-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b0a16-115">**Tag Syntax**</span></span>

<span data-ttu-id="b0a16-116"><v : *élément* rempli = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b0a16-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="b0a16-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b0a16-117">**Script Syntax**</span></span>

<span data-ttu-id="b0a16-118">*Element* . refilled = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b0a16-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="b0a16-119">*expression* = *élément*. rempli</span><span class="sxs-lookup"><span data-stu-id="b0a16-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="b0a16-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b0a16-120">**Remarks**</span></span>

<span data-ttu-id="b0a16-121">La valeur est dupliquée à partir de l’attribut **on** de l’élément [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a16-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="b0a16-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b0a16-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="b0a16-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b0a16-123">**Example**</span></span>

<span data-ttu-id="b0a16-124">Le tracé de la forme est rempli.</span><span class="sxs-lookup"><span data-stu-id="b0a16-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="b0a16-125">[Exemple d’attribut rempli](/previous-versions/bb229669(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b0a16-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="b0a16-126">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="b0a16-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 