---
title: Exemples DirectComposition
description: Les exemples d’applications suivants montrent comment utiliser Microsoft DirectComposition \ 32 ; Et illustrent ses fonctionnalités.
ms.assetid: E2794CE7-20A3-4388-B1DC-D9822C970774
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889ceb9a6f9383930b9231c9c19a2b610fba2815
ms.sourcegitcommit: 38c86be0218ed38d0f14db3df107db29827b6269
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381777"
---
# <a name="directcomposition-samples"></a><span data-ttu-id="3e7f7-103">Exemples DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3e7f7-103">DirectComposition samples</span></span>

> [!NOTE]
> <span data-ttu-id="3e7f7-104">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="3e7f7-105">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="3e7f7-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="3e7f7-106">Les exemples d’applications suivants montrent comment utiliser l’API Microsoft DirectComposition et illustrer ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-106">The following sample applications show how to use the Microsoft DirectComposition API and demonstrate its capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3e7f7-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3e7f7-107">In this section</span></span>



| <span data-ttu-id="3e7f7-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3e7f7-108">Topic</span></span>                                                                                                                                 | <span data-ttu-id="3e7f7-109">Description</span><span class="sxs-lookup"><span data-stu-id="3e7f7-109">Description</span></span>                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e7f7-110">Exemple de fenêtre enfant en couches DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3e7f7-110">DirectComposition layered child window sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionLayeredChildWindow)<br/>                           | <span data-ttu-id="3e7f7-111">Montre comment utiliser DirectComposition pour animer l’image bitmap d’une fenêtre enfant en couches.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-111">Demonstrates how to use DirectComposition to animate the bitmap of a layered child window.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="3e7f7-112">Exemple de gestion de l’animation DirectComposition avec le gestionnaire d’animations Windows v2</span><span class="sxs-lookup"><span data-stu-id="3e7f7-112">Managing DirectComposition animation with Windows Animation Manager v2 sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)<br/> | <span data-ttu-id="3e7f7-113">Montre comment le gestionnaire d’animations Windows v2 peut être utilisé pour générer des courbes d’animation (fonctions) qui peuvent être consommées par DirectComposition ? pour créer des transitions animées dans une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-113">Demonstrates how Windows Animation Manager v2 can be used to generate animation curves (functions) that can be consumed by DirectComposition? to create animated transitions in a desktop application.</span></span> <br/>                                                            |
| [<span data-ttu-id="3e7f7-114">Exemple DirectComposition Effects with Direct2D bitmap content</span><span class="sxs-lookup"><span data-stu-id="3e7f7-114">DirectComposition effects with Direct2D bitmap content sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionEffects)<br/>                                                     | <span data-ttu-id="3e7f7-115">Montre comment utiliser DirectComposition pour appliquer des animations et des effets aux visuels qui ont du contenu bitmap Direct2D.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-115">Demonstrates how to use DirectComposition to apply animations and effects to visuals that have Direct2D bitmap content.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="3e7f7-116">DirectComposition arrière et exemple de traitement par lot D2D</span><span class="sxs-lookup"><span data-stu-id="3e7f7-116">DirectComposition Backface and D2D Batching sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DCompV2BackfaceandD2DBatching)<br/>                  | <span data-ttu-id="3e7f7-117">Montre comment utiliser l’API DirectComposition pour appliquer une visibilité de face arrière à un élément visuel pour afficher et masquer le côté arrière d’un visuel DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-117">Demonstrates how to use the DirectComposition API to apply backface visibility to a visual element to show and hide the back side of a DirectComposition visual.</span></span> <span data-ttu-id="3e7f7-118">Cet exemple illustre également une optimisation des performances du traitement par lot des appels BeginDraw/EndDraw D2D.</span><span class="sxs-lookup"><span data-stu-id="3e7f7-118">This sample also demonstrates a performance optimization of batching D2D BeginDraw/EndDraw calls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="3e7f7-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e7f7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e7f7-120">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="3e7f7-120">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





