---
title: Concepts DirectComposition
description: Cette section fournit une vue d’ensemble conceptuelle de DirectComposition.
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030016"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="5a9c6-103">Concepts DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5a9c6-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="5a9c6-104">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="5a9c6-105">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="5a9c6-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="5a9c6-106">Cette section fournit une vue d’ensemble conceptuelle de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5a9c6-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="5a9c6-107">In this section</span></span>



| <span data-ttu-id="5a9c6-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5a9c6-108">Topic</span></span>                                                                     | <span data-ttu-id="5a9c6-109">Description</span><span class="sxs-lookup"><span data-stu-id="5a9c6-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a9c6-110">Concepts de base</span><span class="sxs-lookup"><span data-stu-id="5a9c6-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="5a9c6-111">Cette rubrique fournit une vue d’ensemble des concepts de base de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="5a9c6-112">Objets bitmap</span><span class="sxs-lookup"><span data-stu-id="5a9c6-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="5a9c6-113">Cette rubrique décrit les types de contenu de bitmap que DirectComposition prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="5a9c6-114">Surface de la composition</span><span class="sxs-lookup"><span data-stu-id="5a9c6-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="5a9c6-115">Cette rubrique décrit les types de surfaces que DirectComposition prend en charge.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5a9c6-116">Transformations</span><span class="sxs-lookup"><span data-stu-id="5a9c6-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="5a9c6-117">Cette rubrique décrit la prise en charge par DirectComposition des transformations affines (linéaire) à deux dimensions (2D) et décrit les types de transformations pris en charge par DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="5a9c6-118">Effets</span><span class="sxs-lookup"><span data-stu-id="5a9c6-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="5a9c6-119">Cette rubrique présente les principes de base des effets DirectComposition et décrit les types d’effets pris en charge par DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="5a9c6-120">Animation</span><span class="sxs-lookup"><span data-stu-id="5a9c6-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="5a9c6-121">Cette rubrique décrit les principes fondamentaux de l’animation DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="5a9c6-122">Portion</span><span class="sxs-lookup"><span data-stu-id="5a9c6-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="5a9c6-123">Cette rubrique décrit la prise en charge DirectComposition pour les éléments visuels de découpage.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="5a9c6-124">Architecture et composants</span><span class="sxs-lookup"><span data-stu-id="5a9c6-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="5a9c6-125">Cette rubrique décrit les composants qui composent DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="5a9c6-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="5a9c6-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a9c6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9c6-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="5a9c6-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





