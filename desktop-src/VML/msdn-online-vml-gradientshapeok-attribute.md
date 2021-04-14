---
title: GradientShapeOK VML (attribut)
description: GradientShapeOK VML (attribut)
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382672"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="2eb21-103">GradientShapeOK VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="2eb21-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="2eb21-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2eb21-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2eb21-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2eb21-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2eb21-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2eb21-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2eb21-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2eb21-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2eb21-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2eb21-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2eb21-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2eb21-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2eb21-110">Détermine si un tracé de dégradé est constitué de chemins d’accès concentriques répétés.</span><span class="sxs-lookup"><span data-stu-id="2eb21-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="2eb21-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2eb21-111">Read/write.</span></span> <span data-ttu-id="2eb21-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="2eb21-112">**VgTriState**.</span></span>

<span data-ttu-id="2eb21-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2eb21-113">**Applies To**</span></span>

[<span data-ttu-id="2eb21-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2eb21-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="2eb21-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="2eb21-115">**Tag Syntax**</span></span>

<span data-ttu-id="2eb21-116"><v : *Element* gradientshapeok = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2eb21-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="2eb21-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="2eb21-117">**Script Syntax**</span></span>

<span data-ttu-id="2eb21-118">*Element* . gradientshapeok = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2eb21-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="2eb21-119">*expression* = *élément*. gradientshapeok</span><span class="sxs-lookup"><span data-stu-id="2eb21-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="2eb21-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="2eb21-120">**Remarks**</span></span>

<span data-ttu-id="2eb21-121">Si la **valeur est true**, le tracé est rempli avec un dégradé concentrique en utilisant le chemin d’accès comme forme répétée du dégradé. La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="2eb21-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="2eb21-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="2eb21-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="2eb21-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2eb21-123">**Example**</span></span>

<span data-ttu-id="2eb21-124">Le tracé est rempli avec un remplissage dégradé concentrique constitué de rectangles répétés.</span><span class="sxs-lookup"><span data-stu-id="2eb21-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 