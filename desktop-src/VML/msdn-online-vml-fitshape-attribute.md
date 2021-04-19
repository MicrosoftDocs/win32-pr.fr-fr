---
title: FitShape VML (attribut)
description: FitShape VML (attribut)
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b05d7bc31afc52c664217ff21d14b40fd0c27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518032"
---
# <a name="vml-fitshape-attribute"></a><span data-ttu-id="ef025-103">FitShape VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="ef025-103">VML FitShape Attribute</span></span>

<span data-ttu-id="ef025-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ef025-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ef025-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ef025-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ef025-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="ef025-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ef025-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="ef025-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ef025-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ef025-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ef025-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ef025-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ef025-110">Définit si le texte est ajusté au cadre englobant d’une forme.</span><span class="sxs-lookup"><span data-stu-id="ef025-110">Defines whether the text fits bounding box of a shape.</span></span> <span data-ttu-id="ef025-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ef025-111">Read/write.</span></span> <span data-ttu-id="ef025-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="ef025-112">**VgTriState**.</span></span>

<span data-ttu-id="ef025-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ef025-113">**Applies To**</span></span>

[<span data-ttu-id="ef025-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="ef025-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="ef025-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="ef025-115">**Tag Syntax**</span></span>

<span data-ttu-id="ef025-116"><v : *Element* fitshape = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ef025-116"><v: *element* fitshape=" *expression* "></span></span>

<span data-ttu-id="ef025-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="ef025-117">**Script Syntax**</span></span>

<span data-ttu-id="ef025-118">*Element* . fitshape = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ef025-118">*element* .fitshape="*expression*"</span></span>

<span data-ttu-id="ef025-119">*expression* = *élément*. fitshape</span><span class="sxs-lookup"><span data-stu-id="ef025-119">*expression*=*element*.fitshape</span></span>

<span data-ttu-id="ef025-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="ef025-120">**Remarks**</span></span>

<span data-ttu-id="ef025-121">Si la **valeur est true**, étire le texte vers les bords de la zone qui définit la forme entière.</span><span class="sxs-lookup"><span data-stu-id="ef025-121">If **True**, stretches the text out to the edges of the box that defines the entire shape.</span></span> <span data-ttu-id="ef025-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="ef025-122">The default is **False**.</span></span>

<span data-ttu-id="ef025-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="ef025-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ef025-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="ef025-124">**Example**</span></span>

<span data-ttu-id="ef025-125">Le texte est étiré pour s’ajuster à la forme.</span><span class="sxs-lookup"><span data-stu-id="ef025-125">The text will stretch to fit the shape.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 