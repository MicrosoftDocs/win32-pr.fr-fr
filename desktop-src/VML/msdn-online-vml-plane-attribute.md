---
title: Attribut plan VML
description: Attribut plan VML
ms.assetid: e1de630b-8e25-4052-b316-251046f73e98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f279f008adf8f12f78d6edd790cc533678adc9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941091"
---
# <a name="vml-plane-attribute"></a><span data-ttu-id="d0e22-103">Attribut plan VML</span><span class="sxs-lookup"><span data-stu-id="d0e22-103">VML Plane Attribute</span></span>

<span data-ttu-id="d0e22-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d0e22-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d0e22-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d0e22-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d0e22-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d0e22-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d0e22-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d0e22-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d0e22-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d0e22-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d0e22-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d0e22-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d0e22-110">Spécifie le plan perpendiculaire à l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="d0e22-110">Specifies the plane that is at right angles to the extrusion.</span></span> <span data-ttu-id="d0e22-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d0e22-111">Read/write.</span></span> <span data-ttu-id="d0e22-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="d0e22-112">**String**.</span></span>

<span data-ttu-id="d0e22-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d0e22-113">**Applies To**</span></span>

[<span data-ttu-id="d0e22-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="d0e22-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="d0e22-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d0e22-115">**Tag Syntax**</span></span>

<span data-ttu-id="d0e22-116"><o : plan de l' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="d0e22-116"><o: *element* plane=" *expression* "></span></span>

<span data-ttu-id="d0e22-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d0e22-117">**Script Syntax**</span></span>

<span data-ttu-id="d0e22-118">*Element* . plan = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d0e22-118">*element* .plane="*expression*"</span></span>

<span data-ttu-id="d0e22-119">*expression* = *élément*. plan</span><span class="sxs-lookup"><span data-stu-id="d0e22-119">*expression*=*element*.plane</span></span>

<span data-ttu-id="d0e22-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d0e22-120">**Remarks**</span></span>

<span data-ttu-id="d0e22-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="d0e22-121">Values include:</span></span>



| <span data-ttu-id="d0e22-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0e22-122">Value</span></span> | <span data-ttu-id="d0e22-123">Description</span><span class="sxs-lookup"><span data-stu-id="d0e22-123">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="d0e22-124">xy</span><span class="sxs-lookup"><span data-stu-id="d0e22-124">xy</span></span>    | <span data-ttu-id="d0e22-125">L’extrusion est perpendiculaire au plan XY.</span><span class="sxs-lookup"><span data-stu-id="d0e22-125">Extrusion is at right angles to the xy -plane.</span></span> <span data-ttu-id="d0e22-126">Default</span><span class="sxs-lookup"><span data-stu-id="d0e22-126">Default</span></span> |
| <span data-ttu-id="d0e22-127">ZX</span><span class="sxs-lookup"><span data-stu-id="d0e22-127">zx</span></span>    | <span data-ttu-id="d0e22-128">L’extrusion est perpendiculaire au plan ZX.</span><span class="sxs-lookup"><span data-stu-id="d0e22-128">Extrusion is at right angles to the zx -plane.</span></span>         |
| <span data-ttu-id="d0e22-129">YZ</span><span class="sxs-lookup"><span data-stu-id="d0e22-129">yz</span></span>    | <span data-ttu-id="d0e22-130">L’extrusion est perpendiculaire au plan YZ.</span><span class="sxs-lookup"><span data-stu-id="d0e22-130">Extrusion is at right angles to the yz -plane.</span></span>         |



 

<span data-ttu-id="d0e22-131">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="d0e22-131">*Microsoft Office Extensions Attribute*</span></span>

 

 