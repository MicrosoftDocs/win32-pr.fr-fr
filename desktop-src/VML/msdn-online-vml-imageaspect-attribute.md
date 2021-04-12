---
title: ImageAspect VML (attribut)
description: ImageAspect VML (attribut)
ms.assetid: 9ae58a76-f097-4feb-9008-ab6212bae8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b873f7577907acb6d8f88f0290117651077b3c55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315617"
---
# <a name="vml-imageaspect-attribute"></a><span data-ttu-id="7e690-103">ImageAspect VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="7e690-103">VML ImageAspect Attribute</span></span>

<span data-ttu-id="7e690-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7e690-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7e690-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7e690-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7e690-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="7e690-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7e690-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="7e690-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7e690-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7e690-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7e690-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7e690-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7e690-110">Définit la manière dont les proportions de l’image du trait sont conservées.</span><span class="sxs-lookup"><span data-stu-id="7e690-110">Defines how the stroke image aspect ratio will be preserved.</span></span> <span data-ttu-id="7e690-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7e690-111">Read/write.</span></span> <span data-ttu-id="7e690-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="7e690-112">**String**.</span></span>

<span data-ttu-id="7e690-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7e690-113">**Applies To**</span></span>

[<span data-ttu-id="7e690-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="7e690-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7e690-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="7e690-115">**Tag Syntax**</span></span>

<span data-ttu-id="7e690-116"><v :</span><span class="sxs-lookup"><span data-stu-id="7e690-116"><v:</span></span>

<span data-ttu-id="7e690-117">élément *imageaspect = "* expression *" >*</span><span class="sxs-lookup"><span data-stu-id="7e690-117">element *imageaspect="* expression *">*</span></span>

<span data-ttu-id="7e690-118">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="7e690-118">**Script Syntax**</span></span>

<span data-ttu-id="7e690-119">Element *. imageaspect = "* expression *"*</span><span class="sxs-lookup"><span data-stu-id="7e690-119">element *.imageaspect="* expression *"*</span></span>

<span data-ttu-id="7e690-120">*=* élément expression *. imageaspect*</span><span class="sxs-lookup"><span data-stu-id="7e690-120">expression *=* element *.imageaspect*</span></span>

<span data-ttu-id="7e690-121">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="7e690-121">**Remarks**</span></span>

<span data-ttu-id="7e690-122">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="7e690-122">Values include:</span></span>



| <span data-ttu-id="7e690-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e690-123">Value</span></span>   | <span data-ttu-id="7e690-124">Description</span><span class="sxs-lookup"><span data-stu-id="7e690-124">Description</span></span>                                |
|---------|--------------------------------------------|
| <span data-ttu-id="7e690-125">Ignorer</span><span class="sxs-lookup"><span data-stu-id="7e690-125">Ignore</span></span>  | <span data-ttu-id="7e690-126">Ignorer les problèmes d’aspect.</span><span class="sxs-lookup"><span data-stu-id="7e690-126">Ignore aspect issues.</span></span>                      |
| <span data-ttu-id="7e690-127">Au moins</span><span class="sxs-lookup"><span data-stu-id="7e690-127">AtLeast</span></span> | <span data-ttu-id="7e690-128">L’image est au moins aussi grande que la fonction **ImageSize**.</span><span class="sxs-lookup"><span data-stu-id="7e690-128">Image is at least as big as **ImageSize**.</span></span> |
| <span data-ttu-id="7e690-129">AtMost</span><span class="sxs-lookup"><span data-stu-id="7e690-129">AtMost</span></span>  | <span data-ttu-id="7e690-130">L’image n’est pas **supérieure à image**.</span><span class="sxs-lookup"><span data-stu-id="7e690-130">Image is no bigger than **ImageSize**.</span></span>     |



 

<span data-ttu-id="7e690-131">Dans chaque cas, l’attribut **ImageSize** est ajusté pour conserver l’aspect de l’image.</span><span class="sxs-lookup"><span data-stu-id="7e690-131">In each case, the **ImageSize** attribute will be adjusted to preserve the aspect of the image.</span></span>

<span data-ttu-id="7e690-132">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="7e690-132">*VML Standard Attribute*</span></span>

<span data-ttu-id="7e690-133">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="7e690-133">**Example**</span></span>

<span data-ttu-id="7e690-134">L’image du trait sera au moins aussi grande que la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="7e690-134">The stroke image will be at least as big as the image size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imageaspect="AtLeast"/>
   </v:shape>
```



 

 