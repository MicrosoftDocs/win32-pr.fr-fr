---
title: Attribut type (extrusion) (VML)
description: Attribut type (extrusion) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842502"
---
# <a name="type-attribute-extrusionvml"></a><span data-ttu-id="9f9bf-103">Attribut type (extrusion) (VML)</span><span class="sxs-lookup"><span data-stu-id="9f9bf-103">Type Attribute (Extrusion)(VML)</span></span>

<span data-ttu-id="9f9bf-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9f9bf-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9f9bf-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9f9bf-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9f9bf-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9f9bf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9f9bf-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9f9bf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9f9bf-110">Définit la façon dont la forme est extrudée.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-110">Defines the way that the shape is extruded.</span></span> <span data-ttu-id="9f9bf-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-111">Read/write.</span></span> <span data-ttu-id="9f9bf-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-112">**String**.</span></span>

<span data-ttu-id="9f9bf-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9f9bf-113">**Applies To**</span></span>

[<span data-ttu-id="9f9bf-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="9f9bf-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="9f9bf-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9f9bf-115">**Tag Syntax**</span></span>

<span data-ttu-id="9f9bf-116"><o : type d' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="9f9bf-116"><o: *element* type=" *expression* "></span></span>

<span data-ttu-id="9f9bf-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="9f9bf-117">**Script Syntax**</span></span>

<span data-ttu-id="9f9bf-118">*Element* . type = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9f9bf-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="9f9bf-119">*expression* = *Element*. type</span><span class="sxs-lookup"><span data-stu-id="9f9bf-119">*expression*=*element*.type</span></span>

<span data-ttu-id="9f9bf-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9f9bf-120">**Remarks**</span></span>

<span data-ttu-id="9f9bf-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="9f9bf-121">Values include:</span></span>



| <span data-ttu-id="9f9bf-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f9bf-122">Value</span></span>       | <span data-ttu-id="9f9bf-123">Description</span><span class="sxs-lookup"><span data-stu-id="9f9bf-123">Description</span></span>                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9bf-124">parallel</span><span class="sxs-lookup"><span data-stu-id="9f9bf-124">parallel</span></span>    | <span data-ttu-id="9f9bf-125">L’extrusion est rendue afin que le centre de projection soit éloigné à l’infini. autrement dit, les lignes d’extrusion ne convergent pas (contrairement aux projections de perspective).</span><span class="sxs-lookup"><span data-stu-id="9f9bf-125">Extrusion is rendered so that the center of projection is infinitely far away; that is, the extrusion lines do not converge (unlike perspective projections).</span></span> <span data-ttu-id="9f9bf-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-126">Default.</span></span> |
| <span data-ttu-id="9f9bf-127">perspective</span><span class="sxs-lookup"><span data-stu-id="9f9bf-127">perspective</span></span> | <span data-ttu-id="9f9bf-128">L’extrusion est rendue au centre de projection, qui est le même que le point de fuite pour les objets non pivotés.</span><span class="sxs-lookup"><span data-stu-id="9f9bf-128">Extrusion is rendered to a center of projection, which is the same as the vanishing point for unrotated objects.</span></span>                                                       |



 

<span data-ttu-id="9f9bf-129">**Attribut extensions Microsoft Office**</span><span class="sxs-lookup"><span data-stu-id="9f9bf-129">**Microsoft Office Extensions Attribute**</span></span>

 

 