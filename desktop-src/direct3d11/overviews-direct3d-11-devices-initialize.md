---
title: Comment créer un appareil et un contexte immédiat
description: Cette rubrique montre comment initialiser un appareil.
ms.assetid: 02a20ada-b3aa-435e-8d66-117a19222f9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 546bee6631816beb699f282a3b4f46bbbc142afc
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786765"
---
# <a name="how-to-create-a-device-and-immediate-context"></a>Comment : créer un appareil et un contexte immédiat

Cette rubrique montre comment initialiser un [appareil](overviews-direct3d-11-devices-intro.md). L’initialisation d’un [appareil](overviews-direct3d-11-devices-intro.md) est l’une des premières tâches que votre application doit effectuer avant de pouvoir afficher votre scène.

**Pour créer un appareil et un contexte immédiat**

Remplissez la structure [**\_ desc de \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) avec des informations sur les formats de mémoire tampon et les dimensions. Pour plus d’informations, consultez Création d’une chaîne de permutation.

L’exemple de code suivant montre comment remplir la structure [**desc de la \_ \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .


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



À l’aide de la structure DESC de la [**\_ \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) de l’étape 1, appelez [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) pour initialiser l’appareil et la chaîne de permutation en même temps.


```
D3D_FEATURE_LEVEL  FeatureLevelsRequested = D3D_FEATURE_LEVEL_11_0;
UINT               numLevelsRequested = 1;
D3D_FEATURE_LEVEL  FeatureLevelsSupported;

if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                D3D_DRIVER_TYPE_HARDWARE, 
                NULL, 
                0,
                &FeatureLevelsRequested, 
                numFeatureLevelsRequested, 
                D3D11_SDK_VERSION, 
                &sd, 
                &g_pSwapChain, 
                &g_pd3dDevice, 
                &FeatureLevelsSupported,
                &g_pImmediateContext )))
{
    return hr;
}
```



> [!Note]  
> Si vous demandez un appareil de [**\_ niveau de fonctionnalité D3D \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) sur un ordinateur uniquement avec le runtime Direct3D 11,0, [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) se ferme immédiatement avec **E \_ INVALIDARG**. Pour demander en toute sécurité tous les niveaux de fonctionnalités possibles sur un ordinateur avec le runtime DirectX 11,0 ou DirectX 11,1, utilisez ce code :
>
> 
>
> <table>
> <colgroup>
> <col  />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>const D3D_FEATURE_LEVEL lvl[] = { D3D_FEATURE_LEVEL_11_1, D3D_FEATURE_LEVEL_11_0,
> D3D_FEATURE_LEVEL_10_1, D3D_FEATURE_LEVEL_10_0,
> D3D_FEATURE_LEVEL_9_3, D3D_FEATURE_LEVEL_9_2, D3D_FEATURE_LEVEL_9_1 };
>
> UINT createDeviceFlags = 0;
> #ifdef _DEBUG
> createDeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
> #endif
>
> ID3D11Device* device = nullptr;
> HRESULT hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, lvl, _countof(lvl), D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> if ( hr == E_INVALIDARG )
> {
>     hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, &lvl[1], _countof(lvl) - 1, D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> }
>
> if (FAILED(hr))
>     return hr;</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> Créez une vue de cible de rendu en appelant [**ID3D11Device :: CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview) et liez la mémoire tampon d’arrière-plan en tant que cible de rendu en appelant [**ID3D11DeviceContext :: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets).
>
> 
>
> <table>
> <colgroup>
> <col  />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>ID3D11Texture2D* pBackBuffer;
>
> // Get a pointer to the back buffer
> hr = g_pSwapChain->GetBuffer( 0, __uuidof( ID3D11Texture2D ), 
>                              ( LPVOID* )&pBackBuffer );
>
> // Create a render-target view
> g_pd3dDevice->CreateRenderTargetView( pBackBuffer, NULL,
>                                       &g_pRenderTargetView );
>
> // Bind the view
> g_pImmediateContext->OMSetRenderTargets( 1, &g_pRenderTargetView, NULL );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> Créez une fenêtre d’affichage pour définir les parties de la cible de rendu qui seront visibles. Définissez la fenêtre d’affichage à l’aide de la structure de la [**\_ fenêtre d’affichage d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) et définissez la fenêtre d’affichage à l’aide de la méthode [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) .
>
> 
>
> <table>
> <colgroup>
> <col  />
> </colgroup>
> <thead>
> <tr class="header">
> <th>C++</th>
> </tr>
> </thead>
> <tbody>
> <tr class="odd">
> <td><pre><code>    // Setup the viewport
>     D3D11_VIEWPORT vp;
>     vp.Width = 640;
>     vp.Height = 480;
>     vp.MinDepth = 0.0f;
>     vp.MaxDepth = 1.0f;
>     vp.TopLeftX = 0;
>     vp.TopLeftY = 0;
>     g_pImmediateContext->RSSetViewports( 1, &vp );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="related-topics"></a>Rubriques connexes
>
> <dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>
>
>  
>
>  
>
