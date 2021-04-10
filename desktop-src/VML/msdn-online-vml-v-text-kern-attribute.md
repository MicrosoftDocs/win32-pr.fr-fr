---
title: Attribut VML V-Text-KERN
description: Attribut VML V-Text-KERN
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941200"
---
# <a name="vml-v-text-kern-attribute"></a><span data-ttu-id="c988c-103">Attribut VML V-Text-KERN</span><span class="sxs-lookup"><span data-stu-id="c988c-103">VML V-Text-Kern Attribute</span></span>

<span data-ttu-id="c988c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c988c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c988c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c988c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c988c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c988c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c988c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c988c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c988c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c988c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c988c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c988c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c988c-110">Détermine si le crénage est activé.</span><span class="sxs-lookup"><span data-stu-id="c988c-110">Determines whether kerning is turned on.</span></span> <span data-ttu-id="c988c-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c988c-111">Read/write.</span></span> <span data-ttu-id="c988c-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c988c-112">**VgTriState**.</span></span>

<span data-ttu-id="c988c-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c988c-113">**Applies To**</span></span>

[<span data-ttu-id="c988c-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="c988c-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="c988c-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c988c-115">**Tag Syntax**</span></span>

<span data-ttu-id="c988c-116"><v : *Element* style = "v-Text-Kern : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c988c-116"><v: *element* style="v-text-kern: *expression* "></span></span>

<span data-ttu-id="c988c-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c988c-117">**Script Syntax**</span></span>

<span data-ttu-id="c988c-118">*Element* . style. v-Text-KERN = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c988c-118">*element* .style.v-text-kern="*expression*"</span></span>

<span data-ttu-id="c988c-119">*expression* = *Element*. style. v-Text-KERN</span><span class="sxs-lookup"><span data-stu-id="c988c-119">*expression*=*element*.style.v-text-kern</span></span>

<span data-ttu-id="c988c-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c988c-120">**Remarks**</span></span>

<span data-ttu-id="c988c-121">Si la **valeur est true**, le crénage est activé.</span><span class="sxs-lookup"><span data-stu-id="c988c-121">If **True**, the kerning is turned on.</span></span> <span data-ttu-id="c988c-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="c988c-122">The default is **False**.</span></span> <span data-ttu-id="c988c-123">Le crénage est la suppression de l’espace entre certaines paires de lettres pour compenser les letterformss irréguliers.</span><span class="sxs-lookup"><span data-stu-id="c988c-123">Kerning is the removal of space between certain letter pairs to compensate for uneven letterforms.</span></span> <span data-ttu-id="c988c-124">Par exemple, si le crénage est activé, un espace supplémentaire entre un « T » majuscule et un « i » minuscule serait supprimé.</span><span class="sxs-lookup"><span data-stu-id="c988c-124">For example, if kerning is turned on, extra space between a capital "T" and a lowercase "i" would be removed.</span></span>

<span data-ttu-id="c988c-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c988c-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="c988c-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c988c-126">**Example**</span></span>

<span data-ttu-id="c988c-127">Le crénage est activé.</span><span class="sxs-lookup"><span data-stu-id="c988c-127">Kerning is turned on.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 