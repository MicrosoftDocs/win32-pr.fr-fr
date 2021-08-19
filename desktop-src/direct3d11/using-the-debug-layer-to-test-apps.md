---
title: Utilisation de la couche de débogage pour déboguer des applications
description: Ici, nous parlerons de la façon d’activer la couche de débogage et certains des problèmes que vous pouvez empêcher à l’aide de la couche de débogage.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ac5492b96c40b4395b2c501b764c646a8edbb06d3a6386a15cbb2534778d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912733"
---
# <a name="using-the-debug-layer-to-debug-apps"></a>Utilisation de la couche de débogage pour déboguer des applications

Nous vous recommandons d’utiliser la [couche de débogage](overviews-direct3d-11-devices-layers.md) pour déboguer vos applications et vous assurer qu’il ne s’agit pas d’erreurs et d’avertissements. La couche de débogage vous aide à écrire du code Direct3D. En outre, votre productivité peut augmenter lorsque vous utilisez la couche de débogage, car vous pouvez voir immédiatement les causes d’erreurs de rendu obscures ou même d’écrans noirs à leur source. La couche de débogage fournit des avertissements pour de nombreux problèmes. Par exemple, la couche de débogage fournit des avertissements pour les problèmes suivants :

-   Vous avez oublié de définir une texture, mais de la lire dans votre nuanceur de pixels
-   Profondeur de sortie, mais aucune limite d’État du gabarit de profondeur
-   Échec de la création de la texture avec INVALIDARG

Ici, nous parlerons de la façon d’activer la [couche de débogage](overviews-direct3d-11-devices-layers.md) et certains des problèmes que vous pouvez empêcher à l’aide de la couche de débogage.

-   [Activation de la couche de débogage](#enabling-the-debug-layer)
-   [Prévention des erreurs dans votre application avec la couche de débogage](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [Ne pas passer de pointeurs NULL au mappage](#dont-pass-null-pointers-to-map)
    -   [Limiter la zone source dans les ressources source et de destination](#confine-source-box-within-source-and-destination-resources)
    -   [Ne supprimez pas DiscardResource ou DiscardView](#dont-drop-discardresource-or-discardview)
-   [Rubriques connexes](#related-topics)

## <a name="enabling-the-debug-layer"></a>Activation de la couche de débogage

Pour activer la [couche de débogage](overviews-direct3d-11-devices-layers.md), spécifiez l’indicateur de [**\_ \_ \_ débogage d3d11 créer un appareil**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) dans le paramètre *Flags* lorsque vous appelez la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) pour créer le périphérique de rendu. cet exemple de code montre comment activer la couche de débogage lorsque votre projet Microsoft Visual Studio se trouve dans une version debug :


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a>Prévention des erreurs dans votre application avec la couche de débogage

Si vous abusez de l’API Direct3D 11 ou si vous transmettez des paramètres incorrects, la sortie de débogage de la [couche de débogage](overviews-direct3d-11-devices-layers.md) signale une erreur ou un avertissement. Vous pouvez ensuite corriger votre erreur. Ensuite, nous examinons certains problèmes de codage qui peuvent provoquer un comportement indéfini ou même le système d’exploitation. Vous pouvez intercepter et éviter ces problèmes à l’aide de la couche de débogage.

### <a name="dont-pass-null-pointers-to-map"></a>Ne pas passer de pointeurs NULL au mappage

Si vous transmettez la **valeur null** au paramètre *PreSource* ou *pMappedResource* de la méthode [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , le comportement de **Map** n’est pas défini. Si vous avez créé un appareil qui prend uniquement en charge la [couche principale](overviews-direct3d-11-devices-layers.md), les paramètres non valides à **mapper** peuvent bloquer le système d’exploitation. Si vous avez créé un appareil qui prend en charge la [couche de débogage](overviews-direct3d-11-devices-layers.md), la sortie de débogage signale une erreur sur cet appel de **mappage** non valide.

### <a name="confine-source-box-within-source-and-destination-resources"></a>Limiter la zone source dans les ressources source et de destination

Dans un appel à la méthode [**ID3D11DeviceContext :: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) , la zone source doit se trouver dans la ressource source. Les décalages de destination, (x, y et z) permettent de compenser la zone source lors de l’écriture dans la ressource de destination, mais les dimensions de la zone source et des décalages doivent être comprises dans la taille de la ressource. Si vous essayez de copier en dehors de la ressource de destination ou si vous spécifiez une zone source supérieure à la ressource source, le comportement de **CopySubresourceRegion** n’est pas défini. Si vous avez créé un appareil qui prend en charge la [couche de débogage](overviews-direct3d-11-devices-layers.md), la sortie de débogage signale une erreur sur cet appel **CopySubresourceRegion** non valide. Des paramètres non valides pour **CopySubresourceRegion** provoquent un comportement indéfini et peuvent entraîner un rendu incorrect, un découpage, aucune copie ou même la suppression du périphérique de rendu.

### <a name="dont-drop-discardresource-or-discardview"></a>Ne supprimez pas DiscardResource ou DiscardView

Le runtime supprime un appel à [**ID3D11DeviceContext1 ::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) ou [**ID3D11DeviceContext1 ::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) , sauf si vous créez correctement la ressource.

La ressource que vous transmettez à [**ID3D11DeviceContext1 ::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) doit avoir été créée à l’aide de la [**\_ \_ valeur par défaut**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) de l’utilisation de d3d11 ou de l' [**\_ utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), sinon le runtime supprime l’appel à **DiscardResource**.

La ressource sous-jacente de la vue que vous transmettez à [**ID3D11DeviceContext1 ::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) doit avoir été créée à l’aide de la [**\_ \_ valeur par défaut**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) de l’utilisation de d3d11 ou de l' [**\_ utilisation \_ dynamique de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), sinon le runtime supprime l’appel à **DiscardView**.

Si vous avez créé un appareil qui prend en charge la [couche de débogage](overviews-direct3d-11-devices-layers.md), la sortie de débogage signale une erreur concernant l’appel supprimé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Couches logicielles](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




