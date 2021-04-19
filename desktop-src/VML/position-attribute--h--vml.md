---
title: Position, attribut (H) (VML)
description: Position, attribut (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513735"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="c7a7b-103">Position, attribut (H) (VML)</span><span class="sxs-lookup"><span data-stu-id="c7a7b-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="c7a7b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c7a7b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c7a7b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c7a7b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c7a7b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c7a7b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c7a7b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c7a7b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c7a7b-110">Spécifie les valeurs thex et y du handle.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="c7a7b-111">**VgVector2D** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="c7a7b-112">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c7a7b-112">**Applies To**</span></span>

<span data-ttu-id="c7a7b-113">[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="c7a7b-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="c7a7b-114">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c7a7b-114">**Tag Syntax**</span></span>

<span data-ttu-id="c7a7b-115"><v : *Element* position = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c7a7b-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="c7a7b-116">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c7a7b-116">**Remarks**</span></span>

<span data-ttu-id="c7a7b-117">les valeurs x et y peuvent être de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="c7a7b-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="c7a7b-118">constant</span><span class="sxs-lookup"><span data-stu-id="c7a7b-118">constant</span></span>
-   <span data-ttu-id="c7a7b-119">formule (par exemple, @2 )</span><span class="sxs-lookup"><span data-stu-id="c7a7b-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="c7a7b-120">ajuster (par exemple, \# 3)</span><span class="sxs-lookup"><span data-stu-id="c7a7b-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="c7a7b-121">centre</span><span class="sxs-lookup"><span data-stu-id="c7a7b-121">center</span></span>
-   <span data-ttu-id="c7a7b-122">côté gauche</span><span class="sxs-lookup"><span data-stu-id="c7a7b-122">topleft</span></span>
-   <span data-ttu-id="c7a7b-123">telle</span><span class="sxs-lookup"><span data-stu-id="c7a7b-123">bottomright</span></span>

<span data-ttu-id="c7a7b-124">Si l’un des types ci-dessus sauf *Adjust* est spécifié, la position du handle est fixe dans cette dimension.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="c7a7b-125">Si une poignée d’ajustement est spécifiée, le descripteur est libre de se déplacer dans cette dimension et la valeur d’ajustement est déterminée par la position de la poignée.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="c7a7b-126">Si un attribut [polaire](msdn-online-vml-polar-attribute.md) est spécifié, l’attribut **position** représente les valeurs de rayon et d’angle du handle au lieu de x et y.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="c7a7b-127">La valeur par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="c7a7b-127">The default value is 0,0.</span></span>

<span data-ttu-id="c7a7b-128">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c7a7b-128">*VML Standard Attribute*</span></span>

 

 