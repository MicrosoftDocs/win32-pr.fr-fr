---
title: ViewpointOrigin VML (attribut)
description: ViewpointOrigin VML (attribut)
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad256f0f5d38c6fbbfb5722e803985506efca217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463279"
---
# <a name="vml-viewpointorigin-attribute"></a><span data-ttu-id="fdecd-103">ViewpointOrigin VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="fdecd-103">VML ViewpointOrigin Attribute</span></span>

<span data-ttu-id="fdecd-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fdecd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fdecd-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fdecd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fdecd-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="fdecd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fdecd-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="fdecd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fdecd-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fdecd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fdecd-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fdecd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fdecd-110">Définit l’origine du point de vue dans le cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="fdecd-110">Defines the origin of the viewpoint within the bounding box of the shape.</span></span> <span data-ttu-id="fdecd-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fdecd-111">Read/write.</span></span> <span data-ttu-id="fdecd-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="fdecd-112">**VgVector2D**.</span></span>

<span data-ttu-id="fdecd-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="fdecd-113">**Applies To**</span></span>

[<span data-ttu-id="fdecd-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="fdecd-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="fdecd-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="fdecd-115">**Tag Syntax**</span></span>

<span data-ttu-id="fdecd-116"><o : *Element* viewpointorigin = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="fdecd-116"><o: *element* viewpointorigin=" *expression* "></span></span>

<span data-ttu-id="fdecd-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="fdecd-117">**Script Syntax**</span></span>

<span data-ttu-id="fdecd-118">*Element* . viewpointorigin = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="fdecd-118">*element* .viewpointorigin="*expression*"</span></span>

<span data-ttu-id="fdecd-119">*expression* = *élément*. viewpointorigin</span><span class="sxs-lookup"><span data-stu-id="fdecd-119">*expression*=*element*.viewpointorigin</span></span>

<span data-ttu-id="fdecd-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="fdecd-120">**Remarks**</span></span>

<span data-ttu-id="fdecd-121">Définit le point de vue en fonction des valeurs x et y de la forme d’origine.</span><span class="sxs-lookup"><span data-stu-id="fdecd-121">Defines the viewpoint in terms of the x and y values of the original shape.</span></span> <span data-ttu-id="fdecd-122">Les valeurs x et y sont comprises entre 0,5 et-0,5 (50% à-50% de l’origine de la coordonnée de la forme).</span><span class="sxs-lookup"><span data-stu-id="fdecd-122">The x and y values range from 0.5 to -0.5 (50% to -50% of the shape's coordinate origin).</span></span> <span data-ttu-id="fdecd-123">La valeur par défaut est 0, 0.</span><span class="sxs-lookup"><span data-stu-id="fdecd-123">The default is 0,0.</span></span>

<span data-ttu-id="fdecd-124">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="fdecd-124">*Microsoft Office Extensions Attribute*</span></span>

 

 