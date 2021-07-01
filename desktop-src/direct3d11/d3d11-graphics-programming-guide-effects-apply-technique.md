---
title: Appliquer une technique (Direct3D 11)
description: Découvrez comment définir l’état de l’effet dans l’appareil pour Direct3D 11 après que les constantes, les textures et l’état du nuanceur sont déclarés et initialisés.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d03f92957eaf1b3d501c0acd54aafde7e16d8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118944"
---
# <a name="apply-a-technique-direct3d-11"></a>Appliquer une technique (Direct3D 11)

Avec les constantes, les textures et l’état du nuanceur déclarés et initialisés, la seule chose à faire est de définir l’état de l’effet dans l’appareil.

## <a name="set-non-shader-state-in-the-device"></a>Définir un état de non-nuanceur dans l’appareil

Un état de pipeline n’est pas défini par un effet. Par exemple, la suppression d’une cible de rendu prépare la cible de rendu pour les données. Avant de définir l’état de l’effet dans l’appareil, voici un exemple d’effacement des tampons de sortie.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Définir l’état de l’effet dans l’appareil

La définition de l’état d’effet s’effectue en appliquant l’état d’effet dans la boucle de rendu. Cette opération s’effectue à partir de l’extérieur de. Autrement dit, sélectionnez une technique, puis définissez l’État pour chacune des passes (selon le résultat souhaité).


```
    D3D11_TECHNIQUE_DESC techDesc;
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

[Rendu d’un effet (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




