---
title: Comment créer un appareil WARP
description: Cette rubrique montre comment créer un appareil de distorsion qui implémente un rastériseur logiciel à grande vitesse.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990965"
---
# <a name="how-to-create-a-warp-device"></a>Comment : créer un appareil WARP

Cette rubrique montre comment créer un appareil de distorsion qui implémente un rastériseur logiciel à grande vitesse. Pour créer un périphérique WARP, spécifiez simplement que l’appareil que vous créez utilisera un pilote WARP. Cet exemple crée un appareil et une chaîne de permutation en même temps.

**Pour créer un appareil WARP**

1.  Définissez les paramètres initiaux d’une chaîne de permutation.
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  Demandez un niveau de fonctionnalité qui implémente les fonctionnalités dont votre application a besoin. Un appareil de distorsion peut être créé pour les niveaux de fonctionnalités de la **fonctionnalité D3D de \_ \_ niveau \_ 9 \_ 1** à la **\_ fonctionnalité D3D \_ \_ 10 \_ 1** et à partir de Windows 8 pour tous les niveaux de fonctionnalité.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    En savoir plus sur les niveaux de fonctionnalités dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Créez l’appareil en appelant [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



Vous devrez fournir l’appel d’API avec le type de pilote WARP à partir de l’énumération de [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Une fois la méthode réussie, elle retourne une interface de chaîne d’échange, une interface de périphérique, un pointeur vers le niveau de fonctionnalité accordé par le pilote et une interface de contexte immédiate.

Pour plus d’informations sur les limitations de la création d’un périphérique WARP sur certains niveaux de fonctionnalité, consultez [limitations création de périphériques de déformation et de référence](overviews-direct3d-11-devices-limitations.md).

## <a name="new-for-windows-8"></a>Nouveauté de Windows 8

Quand la carte d’affichage principale d’un ordinateur est la « carte d’affichage de base Microsoft » (adaptateur de déviation), cet ordinateur possède également un deuxième adaptateur. Ce deuxième adaptateur est le périphérique de rendu uniquement qui n’a pas de sortie d’affichage. Pour plus d’informations sur l’appareil de rendu uniquement, consultez [nouvelles informations dans Windows 8 sur l’énumération des adaptateurs](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 