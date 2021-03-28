---
title: Comment créer un appareil de référence
description: Cette rubrique montre comment créer un appareil de référence qui implémente une implémentation logicielle très précise du Runtime.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380229"
---
# <a name="how-to-create-a-reference-device"></a>Comment : créer un appareil de référence

Cette rubrique montre comment créer un appareil de référence qui implémente une implémentation logicielle très précise du Runtime. Pour créer un appareil de référence, spécifiez simplement que l’appareil que vous créez utilisera un pilote de référence. Cet exemple crée un appareil et une chaîne de permutation en même temps.

**Pour créer un appareil de référence**

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

    

2.  Demandez un niveau de fonctionnalité qui implémente les fonctionnalités dont votre application a besoin. Un appareil de référence peut être créé avec succès pour le runtime Direct3D 11.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    En savoir plus sur les niveaux de fonctionnalités dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Créez l’appareil en appelant [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



Vous devrez fournir l’appel d’API avec le type de pilote de référence à partir de l’énumération de [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Une fois la méthode réussie, elle retourne une interface de chaîne d’échange, une interface de périphérique, un pointeur vers le niveau de fonctionnalité accordé par le pilote et une interface de contexte immédiate.

Pour plus d’informations sur les limitations de la création d’un appareil de référence sur certains niveaux de fonctionnalité, consultez [limitations création de périphériques de déformation et de référence](overviews-direct3d-11-devices-limitations.md). [Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




