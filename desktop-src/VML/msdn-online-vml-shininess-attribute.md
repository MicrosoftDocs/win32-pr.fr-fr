---
title: Attribut brillance VML
description: Attribut brillance VML
ms.assetid: 99c301ff-ed61-48ef-95bb-ceaed1a2553c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7a116adeb955c0f3449b374947a3f8121bd848e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315227"
---
# <a name="vml-shininess-attribute"></a><span data-ttu-id="25ec2-103">Attribut brillance VML</span><span class="sxs-lookup"><span data-stu-id="25ec2-103">VML Shininess Attribute</span></span>

<span data-ttu-id="25ec2-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="25ec2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="25ec2-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="25ec2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="25ec2-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="25ec2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="25ec2-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="25ec2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="25ec2-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="25ec2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="25ec2-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="25ec2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="25ec2-110">Définit la concentration de la lumière réfléchie sur une surface d’extrusion.</span><span class="sxs-lookup"><span data-stu-id="25ec2-110">Defines the concentration of the reflected light on an extrusion surface.</span></span> <span data-ttu-id="25ec2-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="25ec2-111">Read/write.</span></span> <span data-ttu-id="25ec2-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="25ec2-112">**VgNumber**.</span></span>

<span data-ttu-id="25ec2-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="25ec2-113">**Applies To**</span></span>

[<span data-ttu-id="25ec2-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="25ec2-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="25ec2-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="25ec2-115">**Tag Syntax**</span></span>

<span data-ttu-id="25ec2-116"><o : *élément* brillance = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="25ec2-116"><o: *element* shininess=" *expression* "></span></span>

<span data-ttu-id="25ec2-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="25ec2-117">**Script Syntax**</span></span>

<span data-ttu-id="25ec2-118">*Element* . brillance = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="25ec2-118">*element* .shininess="*expression*"</span></span>

<span data-ttu-id="25ec2-119">*expression* = *Element*. brillance</span><span class="sxs-lookup"><span data-stu-id="25ec2-119">*expression*=*element*.shininess</span></span>

<span data-ttu-id="25ec2-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="25ec2-120">**Remarks**</span></span>

<span data-ttu-id="25ec2-121">Les valeurs élevées (8-10) se rapprochent de la brillance d’un miroir et les valeurs basses (2-3) se rapprochent d’un effet flou.</span><span class="sxs-lookup"><span data-stu-id="25ec2-121">High values (8-10) would approximate the shininess of a mirror and low values (2-3) would approximate a speckled effect.</span></span> <span data-ttu-id="25ec2-122">Les valeurs de 4-7 sont standard.</span><span class="sxs-lookup"><span data-stu-id="25ec2-122">Values of 4-7 are typical.</span></span> <span data-ttu-id="25ec2-123">Les réflexions ne reflètent pas les autres objets ; seules les sources de lumière de repérage sont reflétées.</span><span class="sxs-lookup"><span data-stu-id="25ec2-123">Reflections do not mirror other objects; only pinpoint light sources are reflected.</span></span> <span data-ttu-id="25ec2-124">La valeur par défaut est 5.</span><span class="sxs-lookup"><span data-stu-id="25ec2-124">Default value is 5.</span></span>

<span data-ttu-id="25ec2-125">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="25ec2-125">*Microsoft Office Extensions Attribute*</span></span>

 

 