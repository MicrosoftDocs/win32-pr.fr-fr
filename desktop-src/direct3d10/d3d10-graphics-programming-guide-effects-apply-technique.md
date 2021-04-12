---
description: Avec les constantes, les textures et l’état du nuanceur déclarés et initialisés, la seule chose à faire est de définir l’état de l’effet dans l’appareil.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Appliquer une technique (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb7cc48c9115dfb81c1688a3a499e24d46cc563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483016"
---
# <a name="apply-a-technique-direct3d-10"></a>Appliquer une technique (Direct3D 10)

Avec les constantes, les textures et l’état du nuanceur déclarés et initialisés, la seule chose à faire est de définir l’état de l’effet dans l’appareil.

## <a name="set-non-shader-state-in-the-device"></a>Définir un état de non-nuanceur dans l’appareil

Un état de pipeline n’est pas défini par un effet. Par exemple, la suppression d’une cible de rendu prépare la cible de rendu pour les données. Avant de définir l’état de l’effet dans l’appareil, voici un exemple d’effacement des tampons de sortie.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Définir l’état de l’effet dans l’appareil

La définition de l’état d’effet s’effectue en appliquant l’état d’effet dans la boucle de rendu. Cette opération s’effectue à partir de l’extérieur de. Autrement dit, sélectionnez une technique, puis définissez l’État pour chacune des passes (selon le résultat souhaité).


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



Un effet n’affiche rien, il définit simplement l’état de l’effet sur l’appareil. Le code de rendu est appelé après que l’état de l’effet a mis à jour l’état de l’appareil. Dans cet exemple, l’appel DrawIndexed effectue le rendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



