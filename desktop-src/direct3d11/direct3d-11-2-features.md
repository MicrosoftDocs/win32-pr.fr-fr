---
title: Fonctionnalités Direct3D 11,2
description: Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,2, qui est inclus avec Windows 8.1, Windows RT 8,1 et Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971738"
---
# <a name="direct3d-112-features"></a>Fonctionnalités Direct3D 11,2

Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,2, qui est inclus avec Windows 8.1, Windows RT 8,1 et Windows Server 2012 R2.

-   [Ressources en mosaïque](#tiled-resources)
    -   [Vérifier la prise en charge des ressources en mosaïque](#check-tiled-resources-support)
-   [Prise en charge étendue des appareils WARPs](#extended-support-for-warp-devices)
-   [Annoter des commandes graphiques](#annotate-graphics-commands)
-   [Liaison de nuanceur HLSL](#hlsl-shader-linking)
    -   [Graphique de liaison de fonction (FLG)](#function-linking-graph-flg)
-   [Compilateur HLSL de la boîte de réception](#inbox-hlsl-compiler)
-   [Rubriques connexes](#related-topics)

## <a name="tiled-resources"></a>Ressources en mosaïque

Direct3D 11,2 vous permet de créer des ressources en mosaïque qui peuvent être considérées comme des ressources logiques volumineuses qui utilisent de petites quantités de mémoire physique. Les ressources en mosaïque sont utiles (par exemple) avec le terrain dans les jeux et l’interface utilisateur de l’application.

Les ressources en mosaïque sont créées en spécifiant l’indicateur de [**\_ \_ \_ mosaïque diverse des ressources d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Pour utiliser une ressource en mosaïque, utilisez l’API suivante :

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3d11 \_ Fonctionnalité de débogage \_ \_ désactiver le \_ \_ \_ \_ suivi \_ et \_** l’indicateur de validation des ressources en mosaïque avec [ **ID3D11Debug :: SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Pour plus d’informations sur les ressources en mosaïque, consultez [ressources en mosaïque](tiled-resources.md).

### <a name="check-tiled-resources-support"></a>Vérifier la prise en charge des ressources en mosaïque

Avant d’utiliser des ressources en mosaïque, vous devez déterminer si l’appareil prend en charge les ressources en mosaïque. Voici comment vérifier la prise en charge des ressources en mosaïque :


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>Prise en charge étendue des appareils WARPs

Direct3D 11,2 étend la prise en charge des appareils [Warps](overviews-direct3d-11-devices-create-warp.md) , que vous créez en passant la [**\_ \_ \_ distorsion de type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) dans le paramètre *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). Le convertisseur logiciel WARP dans Direct3D 11,2 ajoute une prise en charge complète du [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D 11 \_ 1, y compris les [ressources en mosaïque](#tiled-resources), [**IDXGIDevice3 :: Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), les surfaces BCN partagées, minblend et la valeur par défaut de la carte. La prise en charge [double](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) dans les nuanceurs HLSL a également été activée, ainsi que la prise en charge de 16x MSAA.

## <a name="annotate-graphics-commands"></a>Annoter des commandes graphiques

Direct3D 11,2 vous permet d’annoter des commandes graphiques avec ces API :

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2::EndEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Liaison de nuanceur HLSL

Windows 8.1 ajoute une compilation et une liaison distinctes des nuanceurs HLSL, ce qui permet aux programmeurs graphiques de créer des fonctions HLSL précompilées, de les empaqueter dans des bibliothèques et de les lier à des nuanceurs complets au moment de l’exécution. Il s’agit essentiellement d’un équivalent à la compilation, aux bibliothèques et à la liaison de C/C++ séparés, et permet aux programmeurs de composer du code HLSL précompilé lorsque des informations supplémentaires deviennent disponibles pour finaliser le calcul. Pour plus d’informations sur l’utilisation de la liaison de nuanceur, consultez Utilisation de la [liaison de nuanceur](/windows/desktop/direct3dhlsl/using-shader-linking).

Procédez comme suit pour créer un nuanceur final à l’aide de la liaison dynamique au moment de l’exécution.

**Pour créer et utiliser la liaison de nuanceur**

1.  Créez un objet de l’éditeur de liens [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) , qui représente un contexte de liaison. Un contexte unique ne peut pas être utilisé pour produire plusieurs nuanceurs ; un contexte de liaison est utilisé pour produire un seul nuanceur, puis le contexte de liaison est rejeté.
2.  Utilisez [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) pour charger et définir des bibliothèques à partir de leurs objets BLOB de bibliothèque.
3.  Utilisez [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) pour charger et définir un objet blob d’entrée de nuanceur, ou créez un [nuanceur FLG](#function-linking-graph-flg).
4.  Utilisez [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) pour créer des objets [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) , puis appelez des fonctions sur ces objets pour relier les ressources à leurs emplacements finaux.
5.  Ajoutez les bibliothèques à l’éditeur de liens, puis appelez [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) pour produire le code d’octet du nuanceur final qui peut ensuite être chargé et utilisé dans le runtime, comme un nuanceur lié et précompilé complet.

### <a name="function-linking-graph-flg"></a>Graphique de liaison de fonction (FLG)

Windows 8.1 ajoute également le graphique de liaison de fonction (FLG). Vous pouvez utiliser FLG pour construire des nuanceurs qui se composent d’une séquence d’appels de fonctions précompilées qui passent des valeurs les unes aux autres. Lors de l’utilisation de FLG, il n’est pas nécessaire d’écrire du code HLSL et d’appeler le compilateur HLSL. Au lieu de cela, la structure du nuanceur est spécifiée par programme à l’aide d’appels d’API C++. Les nœuds FLG représentent les signatures d’entrée et de sortie et les appels des fonctions de bibliothèque précompilées. L’ordre d’enregistrement des nœuds d’appel de fonction définit la séquence d’appels. Le nœud de signature d’entrée doit être spécifié en premier, tandis que le nœud de signature de sortie doit être spécifié en dernier. Les bords FLG définissent la façon dont les valeurs sont passées d’un nœud à un autre. Les types de données des valeurs passées doivent être identiques ; Il n’existe pas de conversion de type implicite. Les règles de forme et swizzling suivent le comportement HLSL et les valeurs peuvent uniquement être transmises par progression dans cette séquence. Pour plus d’informations sur l’API FLG, consultez [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>Compilateur HLSL de la boîte de réception

Le compilateur HLSL est désormais la boîte de réception de Windows 8.1 et versions ultérieures. Désormais, la plupart des API de programmation de nuanceur peuvent être utilisées dans les applications du Windows Store conçues pour Windows 8.1 et versions ultérieures. De nombreuses API de programmation de nuanceur n’ont pas pu être utilisées dans les applications du Windows Store conçues pour Windows 8. les pages de référence pour ces API ont été marquées avec une remarque. Toutefois, certaines API de nuanceur (par exemple, [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) peuvent toujours être utilisées uniquement pour développer des applications du Windows Store, et pas dans les applications que vous envoyez au Windows Store. les pages de référence pour ces API sont toujours signalées par une note.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nouveautés de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 