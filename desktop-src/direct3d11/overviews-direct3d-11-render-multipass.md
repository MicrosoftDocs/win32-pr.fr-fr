---
title: Rendu Multiple-Pass
description: Le rendu à passe multiple est un processus dans lequel une application parcourt son graphique de scène plusieurs fois afin de produire une sortie à restituer à l’affichage.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310442"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="13593-103">Rendu Multiple-Pass</span><span class="sxs-lookup"><span data-stu-id="13593-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="13593-104">Le rendu à passe multiple est un processus dans lequel une application parcourt son graphique de scène plusieurs fois afin de produire une sortie à restituer à l’affichage.</span><span class="sxs-lookup"><span data-stu-id="13593-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="13593-105">Le rendu à plusieurs passes améliore les performances, car il divise des scènes complexes en tâches qui peuvent s’exécuter simultanément.</span><span class="sxs-lookup"><span data-stu-id="13593-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="13593-106">Pour effectuer un rendu à passe multiple, vous créez un contexte différé et une liste de commandes pour chaque passe supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="13593-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="13593-107">Tandis que l’application parcourt le graphique de scène, elle enregistre les commandes (par exemple, les commandes de rendu telles que [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) dans un contexte différé.</span><span class="sxs-lookup"><span data-stu-id="13593-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="13593-108">Une fois que l’application a terminé la traversée, elle appelle la méthode [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) sur le contexte différé.</span><span class="sxs-lookup"><span data-stu-id="13593-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="13593-109">Enfin, l’application appelle la méthode [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) sur le contexte immédiat pour exécuter les commandes dans chaque liste de commandes.</span><span class="sxs-lookup"><span data-stu-id="13593-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="13593-110">Le pseudo-code suivant montre comment effectuer un rendu à passe multiple :</span><span class="sxs-lookup"><span data-stu-id="13593-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="13593-111">Le contexte immédiat modifie une ressource, qui est liée au contexte immédiat comme une vue de la cible de rendu (RTV); en revanche, chaque contexte différé utilise simplement la ressource, qui est liée au contexte différé comme une vue de ressource de nuanceur (SRV).</span><span class="sxs-lookup"><span data-stu-id="13593-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="13593-112">Pour plus d’informations sur les contextes immédiats et différés, consultez [rendu immédiat et différé](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="13593-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="13593-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="13593-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13593-114">Rendu</span><span class="sxs-lookup"><span data-stu-id="13593-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




