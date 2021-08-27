---
title: Comment se procurer le niveau de fonctionnalité de l’appareil
description: Cette rubrique montre comment obtenir le niveau de fonctionnalité le plus élevé pris en charge par un appareil.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac21d00aeef8ae6c82ffd9f55a40415b6af1d0a780cc6878d8c30bf453457eb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119599"
---
# <a name="how-to-get-the-device-feature-level"></a>Procédure : obtention du niveau de fonctionnalité de l’appareil

Cette rubrique montre comment obtenir le niveau de [fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) le plus élevé pris en charge par un [appareil](overviews-direct3d-11-devices-intro.md). Les périphériques Direct3D 11 prennent en charge un ensemble fixe de niveaux de fonctionnalités qui sont définis dans l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Lorsque vous connaissez le [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) le plus élevé pris en charge par un appareil, vous pouvez exécuter des chemins de code appropriés pour cet appareil.

**Pour accéder au niveau de fonctionnalité de l’appareil**

1.  Appelez la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou les fonctions [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) tout en spécifiant une **valeur null** pour le paramètre *ppDevice* . Vous pouvez effectuer cette opération avant la création de l’appareil.

    \- ou -

    Appelez [**ID3D11Device :: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) après la création de l’appareil.

2.  Examinez la valeur de l’énumération de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) retournée à partir de la dernière étape pour déterminer le niveau de fonctionnalité pris en charge.

L’exemple de code suivant montre comment déterminer le niveau de fonctionnalité le plus élevé pris en charge en appelant la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) . **D3D11CreateDevice** stocke le niveau de fonctionnalité le plus élevé pris en charge dans la variable FeatureLevel. Vous pouvez utiliser ce code pour examiner la valeur du type énuméré de [**\_ \_ niveau de fonctionnalité D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) retourné par **D3D11CreateDevice** . Notez que ce code répertorie tous les niveaux de fonctionnalité explicitement (pour Direct3D 11,1 et Direct3D 11,2).

> [!Note]  
> Si le runtime Direct3D 11,1 est présent sur l’ordinateur et que *pFeatureLevels* a la valeur **null**, cette fonction ne crée pas un appareil de [**niveau de fonctionnalité D3D \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Pour créer un appareil de **\_ niveau de fonctionnalité D3D \_ \_ 11 \_ 1** , vous devez fournir explicitement un tableau de **\_ \_ niveau de fonctionnalité D3D** qui comprend le **niveau de \_ fonctionnalité D3D \_ \_ 11 \_ 1**. Si vous fournissez un tableau de **\_ \_ niveau de fonctionnalité D3D** qui contient le **niveau de \_ fonctionnalité D3D \_ \_ 11 \_ 1** sur un ordinateur sur lequel le runtime Direct3D 11,1 n’est pas installé, cette fonction échoue immédiatement avec E \_ INVALIDARG.

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



La section de [référence 10Level9](d3d11-graphics-reference-10level9.md) répertorie les différences entre la façon dont les différentes méthodes [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) se comportent à différents niveaux de fonctionnalités 10Level9.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Direct3D 11 sur du matériel de niveau inférieur](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




