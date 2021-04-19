---
title: Utilisation de DirectComposition
description: Cette section décrit les meilleures pratiques pour l’utilisation de Microsoft DirectComposition \ 32 ; Et montre comment utiliser l’API pour accomplir plusieurs tâches courantes.
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106517986"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="92e4d-103">Utilisation de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="92e4d-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="92e4d-104">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="92e4d-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="92e4d-105">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="92e4d-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="92e4d-106">Cette section décrit les meilleures pratiques pour l’utilisation de l’API Microsoft DirectComposition et montre comment utiliser l’API pour accomplir plusieurs tâches courantes.</span><span class="sxs-lookup"><span data-stu-id="92e4d-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92e4d-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="92e4d-107">In this section</span></span>



| <span data-ttu-id="92e4d-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="92e4d-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="92e4d-109">Description</span><span class="sxs-lookup"><span data-stu-id="92e4d-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92e4d-110">Meilleures pratiques pour DirectComposition</span><span class="sxs-lookup"><span data-stu-id="92e4d-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="92e4d-111">Cette rubrique décrit les meilleures pratiques pour l’utilisation de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="92e4d-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="92e4d-112">Comment initialiser DirectComposition</span><span class="sxs-lookup"><span data-stu-id="92e4d-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="92e4d-113">Cette rubrique montre comment créer et initialiser l’ensemble minimal d’objets DirectComposition nécessaires pour créer une composition simple.</span><span class="sxs-lookup"><span data-stu-id="92e4d-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="92e4d-114">Comment créer une arborescence d’éléments visuels simple</span><span class="sxs-lookup"><span data-stu-id="92e4d-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="92e4d-115">Cette rubrique montre comment créer une arborescence d’éléments visuels DirectComposition simple.</span><span class="sxs-lookup"><span data-stu-id="92e4d-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="92e4d-116">L’exemple de cette rubrique génère et compose une arborescence d’éléments visuels qui se compose d’un visuel racine et de trois visuels enfants.</span><span class="sxs-lookup"><span data-stu-id="92e4d-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="92e4d-117">Comment découper un objet Rectangle</span><span class="sxs-lookup"><span data-stu-id="92e4d-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="92e4d-118">Cette rubrique montre comment utiliser un objet clip rectangle pour découper un élément visuel ou une arborescence d’éléments visuels.</span><span class="sxs-lookup"><span data-stu-id="92e4d-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="92e4d-119">Comment appliquer des transformations 2D</span><span class="sxs-lookup"><span data-stu-id="92e4d-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="92e4d-120">Cette rubrique montre comment appliquer des transformations 2D à un visuel à l’aide de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="92e4d-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="92e4d-121">Comment appliquer des effets</span><span class="sxs-lookup"><span data-stu-id="92e4d-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="92e4d-122">Cette rubrique montre comment utiliser DirectComposition pour appliquer des effets et des transformations 3D à un visuel.</span><span class="sxs-lookup"><span data-stu-id="92e4d-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="92e4d-123">Comment appliquer des animations</span><span class="sxs-lookup"><span data-stu-id="92e4d-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="92e4d-124">Cette rubrique montre comment animer les propriétés d’un visuel à l’aide de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="92e4d-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="92e4d-125">Comment animer l’image bitmap d’une fenêtre enfant en couches</span><span class="sxs-lookup"><span data-stu-id="92e4d-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="92e4d-126">Cette rubrique explique comment créer et animer un visuel qui utilise l’image bitmap d’une fenêtre enfant en couches comme contenu du visuel.</span><span class="sxs-lookup"><span data-stu-id="92e4d-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="92e4d-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92e4d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92e4d-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="92e4d-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





