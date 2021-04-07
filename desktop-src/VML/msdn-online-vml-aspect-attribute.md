---
title: Attribut aspect VML
description: Attribut aspect VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728333"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="0072a-103">Attribut aspect VML</span><span class="sxs-lookup"><span data-stu-id="0072a-103">VML Aspect Attribute</span></span>

<span data-ttu-id="0072a-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0072a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0072a-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0072a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0072a-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="0072a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0072a-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="0072a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0072a-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0072a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0072a-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0072a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0072a-110">Spécifie la manière dont les proportions de l’image de remplissage sont conservées.</span><span class="sxs-lookup"><span data-stu-id="0072a-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="0072a-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0072a-111">Read/write.</span></span> <span data-ttu-id="0072a-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="0072a-112">**String**.</span></span>

<span data-ttu-id="0072a-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="0072a-113">**Applies To**</span></span>

[<span data-ttu-id="0072a-114">Complète</span><span class="sxs-lookup"><span data-stu-id="0072a-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="0072a-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="0072a-115">**Tag Syntax**</span></span>

<span data-ttu-id="0072a-116"><v : *élément* aspect = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="0072a-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="0072a-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="0072a-117">**Script Syntax**</span></span>

<span data-ttu-id="0072a-118">*Element* . aspect = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0072a-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="0072a-119">*expression* = *Element*. aspect</span><span class="sxs-lookup"><span data-stu-id="0072a-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="0072a-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="0072a-120">**Remarks**</span></span>

<span data-ttu-id="0072a-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="0072a-121">Values include:</span></span>



| <span data-ttu-id="0072a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0072a-122">Value</span></span>   | <span data-ttu-id="0072a-123">Description</span><span class="sxs-lookup"><span data-stu-id="0072a-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="0072a-124">ignore</span><span class="sxs-lookup"><span data-stu-id="0072a-124">ignore</span></span>  | <span data-ttu-id="0072a-125">Ignorer les problèmes d’aspect.</span><span class="sxs-lookup"><span data-stu-id="0072a-125">Ignore aspect issues.</span></span> <span data-ttu-id="0072a-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="0072a-126">Default.</span></span>        |
| <span data-ttu-id="0072a-127">au moins</span><span class="sxs-lookup"><span data-stu-id="0072a-127">atleast</span></span> | <span data-ttu-id="0072a-128">L’image est au moins aussi grande que la **taille**.</span><span class="sxs-lookup"><span data-stu-id="0072a-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="0072a-129">atmost</span><span class="sxs-lookup"><span data-stu-id="0072a-129">atmost</span></span>  | <span data-ttu-id="0072a-130">L’image n’est pas supérieure à la **taille**.</span><span class="sxs-lookup"><span data-stu-id="0072a-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="0072a-131">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="0072a-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="0072a-132">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="0072a-132">**Example**</span></span>

<span data-ttu-id="0072a-133">L’image qui compose le remplissage est supérieure ou égale à une taille de 10 points de 10 points.</span><span class="sxs-lookup"><span data-stu-id="0072a-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 