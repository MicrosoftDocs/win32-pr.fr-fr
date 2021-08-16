---
title: Rendu Multiple-Pass
description: Le rendu à passe multiple est un processus dans lequel une application parcourt son graphique de scène plusieurs fois afin de produire une sortie à restituer à l’affichage.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242573dea2982f3525082187aad536a407e446c4ce59f116f53b8fa0d40fc582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124207"
---
# <a name="multiple-pass-rendering"></a>Rendu Multiple-Pass

Le rendu à passe multiple est un processus dans lequel une application parcourt son graphique de scène plusieurs fois afin de produire une sortie à restituer à l’affichage. Le rendu à plusieurs passes améliore les performances, car il divise des scènes complexes en tâches qui peuvent s’exécuter simultanément.

Pour effectuer un rendu à passe multiple, vous créez un contexte différé et une liste de commandes pour chaque passe supplémentaire. Tandis que l’application parcourt le graphique de scène, elle enregistre les commandes (par exemple, les commandes de rendu telles que [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) dans un contexte différé. Une fois que l’application a terminé la traversée, elle appelle la méthode [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) sur le contexte différé. Enfin, l’application appelle la méthode [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) sur le contexte immédiat pour exécuter les commandes dans chaque liste de commandes.

Le pseudo-code suivant montre comment effectuer un rendu à passe multiple :

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
> Le contexte immédiat modifie une ressource, qui est liée au contexte immédiat comme une vue de la cible de rendu (RTV); en revanche, chaque contexte différé utilise simplement la ressource, qui est liée au contexte différé comme une vue de ressource de nuanceur (SRV). Pour plus d’informations sur les contextes immédiats et différés, consultez [rendu immédiat et différé](overviews-direct3d-11-render-multi-thread-render.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




