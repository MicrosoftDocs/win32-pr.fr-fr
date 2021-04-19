---
title: Attribut de rendu VML
description: Attribut de rendu VML
ms.assetid: a05e7f6e-4784-4ff8-9deb-0501d3a5658e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70872e823a2d43d6a605fbf07a817473b19a125a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511504"
---
# <a name="vml-render-attribute"></a><span data-ttu-id="be6ad-103">Attribut de rendu VML</span><span class="sxs-lookup"><span data-stu-id="be6ad-103">VML Render Attribute</span></span>

<span data-ttu-id="be6ad-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="be6ad-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="be6ad-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="be6ad-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="be6ad-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="be6ad-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="be6ad-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="be6ad-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="be6ad-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="be6ad-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="be6ad-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="be6ad-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="be6ad-110">Définit le mode de rendu de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="be6ad-110">Defines the rendering mode of the extrusion.</span></span> <span data-ttu-id="be6ad-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="be6ad-111">Read/write.</span></span> <span data-ttu-id="be6ad-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="be6ad-112">**String**.</span></span>

<span data-ttu-id="be6ad-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="be6ad-113">**Applies To**</span></span>

[<span data-ttu-id="be6ad-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="be6ad-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="be6ad-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="be6ad-115">**Tag Syntax**</span></span>

<span data-ttu-id="be6ad-116"><o : *élément* Render = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="be6ad-116"><o: *element* render=" *expression* "></span></span>

<span data-ttu-id="be6ad-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="be6ad-117">**Script Syntax**</span></span>

<span data-ttu-id="be6ad-118">*Element* . Render = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="be6ad-118">*element* .render="*expression*"</span></span>

<span data-ttu-id="be6ad-119">*expression* = *élément*. Render</span><span class="sxs-lookup"><span data-stu-id="be6ad-119">*expression*=*element*.render</span></span>

<span data-ttu-id="be6ad-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="be6ad-120">**Remarks**</span></span>

<span data-ttu-id="be6ad-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="be6ad-121">Values include:</span></span>



| <span data-ttu-id="be6ad-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="be6ad-122">Value</span></span>        | <span data-ttu-id="be6ad-123">Description</span><span class="sxs-lookup"><span data-stu-id="be6ad-123">Description</span></span>                                                   |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="be6ad-124">Solid</span><span class="sxs-lookup"><span data-stu-id="be6ad-124">solid</span></span>        | <span data-ttu-id="be6ad-125">Le rendu affiche une forme unie.</span><span class="sxs-lookup"><span data-stu-id="be6ad-125">Rendering displays a solid shape.</span></span> <span data-ttu-id="be6ad-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="be6ad-126">Default.</span></span>                    |
| <span data-ttu-id="be6ad-127">Wireframe</span><span class="sxs-lookup"><span data-stu-id="be6ad-127">wireframe</span></span>    | <span data-ttu-id="be6ad-128">Le rendu affiche une forme filaire.</span><span class="sxs-lookup"><span data-stu-id="be6ad-128">Rendering displays a wireframe shape.</span></span>                         |
| <span data-ttu-id="be6ad-129">boundingcube</span><span class="sxs-lookup"><span data-stu-id="be6ad-129">boundingcube</span></span> | <span data-ttu-id="be6ad-130">Le rendu affiche le cube englobant qui contient la forme.</span><span class="sxs-lookup"><span data-stu-id="be6ad-130">Rendering displays the bounding cube that contains the shape.</span></span> |



 

<span data-ttu-id="be6ad-131">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="be6ad-131">*Microsoft Office Extensions Attribute*</span></span>

 

 