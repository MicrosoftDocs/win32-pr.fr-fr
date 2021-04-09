---
title: Attribut de facette VML
description: Attribut de facette VML
ms.assetid: 6b874d79-a34e-45f7-bbbf-44d652410b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d4fec254ff3e6af35d82cd45146c201701555b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101844"
---
# <a name="vml-facet-attribute"></a><span data-ttu-id="6e907-103">Attribut de facette VML</span><span class="sxs-lookup"><span data-stu-id="6e907-103">VML Facet Attribute</span></span>

<span data-ttu-id="6e907-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6e907-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6e907-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6e907-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6e907-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="6e907-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6e907-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="6e907-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6e907-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6e907-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6e907-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6e907-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6e907-110">Définit le nombre de facettes utilisées pour décrire les surfaces courbes d’une extrusion.</span><span class="sxs-lookup"><span data-stu-id="6e907-110">Defines the number of facets used to describe curved surfaces of an extrusion.</span></span> <span data-ttu-id="6e907-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6e907-111">Read/write.</span></span> <span data-ttu-id="6e907-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e907-112">**VgNumber**.</span></span>

<span data-ttu-id="6e907-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6e907-113">**Applies To**</span></span>

[<span data-ttu-id="6e907-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="6e907-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="6e907-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="6e907-115">**Tag Syntax**</span></span>

<span data-ttu-id="6e907-116"><o : *élément* facette = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6e907-116"><o: *element* facet=" *expression* "></span></span>

<span data-ttu-id="6e907-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="6e907-117">**Script Syntax**</span></span>

<span data-ttu-id="6e907-118">*Element* . facette = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6e907-118">*element* .facet="*expression*"</span></span>

<span data-ttu-id="6e907-119">*expression* = *élément*. facette</span><span class="sxs-lookup"><span data-stu-id="6e907-119">*expression*=*element*.facet</span></span>

<span data-ttu-id="6e907-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="6e907-120">**Remarks**</span></span>

<span data-ttu-id="6e907-121">Définit la façon dont un moteur de rendu se rapproche de l’extrusion.</span><span class="sxs-lookup"><span data-stu-id="6e907-121">Defines the way that a rendering engine will approximate the extrusion.</span></span> <span data-ttu-id="6e907-122">Un nombre inférieur indique une tolérance de rendu inférieure pour le moteur de rendu et génère plus de facettes.</span><span class="sxs-lookup"><span data-stu-id="6e907-122">A lower number will indicate a lower rendering tolerance to the rendering engine and will yield more facets.</span></span> <span data-ttu-id="6e907-123">Des nombres plus élevés feront apparaître l’extrusion plus à facettes.</span><span class="sxs-lookup"><span data-stu-id="6e907-123">Higher numbers will make the extrusion appear more faceted.</span></span> <span data-ttu-id="6e907-124">La valeur par défaut est 30 000.</span><span class="sxs-lookup"><span data-stu-id="6e907-124">The default value is 30,000.</span></span>

<span data-ttu-id="6e907-125">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="6e907-125">*Microsoft Office Extensions Attribute*</span></span>

 

 