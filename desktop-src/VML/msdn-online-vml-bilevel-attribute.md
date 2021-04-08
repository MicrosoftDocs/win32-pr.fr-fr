---
title: Attribut de biniveau VML
description: Attribut de biniveau VML
ms.assetid: 5b87e928-6f0a-4b00-833a-3c2add2d5677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263a9d538a76ba0c9b203cbcf04f8413d4286c34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728309"
---
# <a name="vml-bilevel-attribute"></a><span data-ttu-id="fa22e-103">Attribut de biniveau VML</span><span class="sxs-lookup"><span data-stu-id="fa22e-103">VML Bilevel Attribute</span></span>

<span data-ttu-id="fa22e-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fa22e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fa22e-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fa22e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fa22e-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="fa22e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fa22e-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="fa22e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fa22e-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fa22e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fa22e-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fa22e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fa22e-110">Détermine si une image sera affichée en noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="fa22e-110">Determines whether an image will be displayed in black and white.</span></span> <span data-ttu-id="fa22e-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fa22e-111">Read/write.</span></span> <span data-ttu-id="fa22e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="fa22e-112">**VgTriState**.</span></span>

<span data-ttu-id="fa22e-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="fa22e-113">**Applies To**</span></span>

[<span data-ttu-id="fa22e-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="fa22e-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="fa22e-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="fa22e-115">**Tag Syntax**</span></span>

<span data-ttu-id="fa22e-116"><v : *élément* biniveau = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fa22e-116"><v: *element* bilevel=" *expression* "></span></span>

<span data-ttu-id="fa22e-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="fa22e-117">**Script Syntax**</span></span>

<span data-ttu-id="fa22e-118">*Element* . BiLevel = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="fa22e-118">*element* .bilevel="*expression*"</span></span>

<span data-ttu-id="fa22e-119">*expression* = *élément*. biniveau</span><span class="sxs-lookup"><span data-stu-id="fa22e-119">*expression*=*element*.bilevel</span></span>

<span data-ttu-id="fa22e-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="fa22e-120">**Remarks**</span></span>

<span data-ttu-id="fa22e-121">Si la **valeur est true**, l’image sera affichée à l’aide de deux couleurs (noir et blanc).</span><span class="sxs-lookup"><span data-stu-id="fa22e-121">If **True**, the image will be displayed using two colors (black and white).</span></span> <span data-ttu-id="fa22e-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="fa22e-122">The default is **False**.</span></span> <span data-ttu-id="fa22e-123">Cela crée un effet similaire à la postérisation.</span><span class="sxs-lookup"><span data-stu-id="fa22e-123">This creates an effect similar to posterization.</span></span>

<span data-ttu-id="fa22e-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="fa22e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="fa22e-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="fa22e-125">**Example**</span></span>

<span data-ttu-id="fa22e-126">L’image est affichée en noir et blanc uniquement.</span><span class="sxs-lookup"><span data-stu-id="fa22e-126">The image will be displayed in black and white only.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata bilevel="True" src="kids.jpg"/>
   </v:shape>
```



 

 