---
description: Le taux d’actualisation des variables indique que le déchirement doit être activé, ce qui est également connu sous le nom de &\# 0034 ; vsync-off&\# 0034 ; support.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Affichage du taux d’actualisation des variables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200716"
---
# <a name="variable-refresh-rate-displays"></a>Affichage du taux d’actualisation des variables

Le taux d’actualisation des variables indique que le *déchirement* doit être activé, ce qui est également appelé prise en charge de la « Vsync ».

-   [Le taux d’actualisation des variables affiche/Vsync désactivé](#variable-refresh-rate-displaysvsync-off)
-   [Rubriques connexes](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Le taux d’actualisation des variables affiche/Vsync désactivé

La prise en charge des taux d’actualisation des variables s’affiche en définissant certains indicateurs lors de la création et de la présentation de la chaîne de permutation.

Pour utiliser cette fonctionnalité, les utilisateurs de l’application doivent se trouver sur des systèmes Windows 10 avec [KB3156421](https://support.microsoft.com/kb/3156421) ou la mise à jour anniversaire installée. La fonctionnalité fonctionne sur toutes les versions de Direct3D 11 et 12 à l’aide de l'*effet d’échange * dxgi \_ \_ \_ bascule \_ \** _ permuter les effets.

Pour ajouter la prise en charge de Vsync à vos applications, vous pouvez vous référer à un exemple complet d’exécution pour Direct3D 12, _ *D3D12Fullscreen** (voir les [exemples de travail](../direct3d12/working-samples.md)). Il y a également quelques points qui ne sont pas explicitement appelés dans l’exemple de code, mais vous devez faire attention à.

-   [**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (ou [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) doit avoir le même indicateur de création de chaîne de permutation (dxgi d’activation de l' \_ indicateur de chaîne de permutation \_ \_ \_ \_ ) passé comme [**présent**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (ou [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).
-   DXGI \_ présente \_ autoriser le \_ déchirement ne peut être utilisé qu’avec l’intervalle de synchronisation 0. Il est recommandé de toujours transmettre cet indicateur de suppression lors de l’utilisation de l’intervalle de synchronisation 0 si [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) signale que le déchirement est pris en charge *et* que l’application est en mode fenêtre, y compris le mode plein écran sans bordure. Pour plus d’informations, reportez-vous aux constantes [**\_ présentes dans dxgi**](dxgi-present.md) .
-   La désactivation de Vsync ne UNCAP pas nécessairement votre fréquence d’images : les développeurs doivent également s’assurer que les appels [**présents**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) ne sont pas limités par d’autres événements de minutage (tels que l' `CompositionTarget::Rendering` événement dans une application XAML).

Le code ci-dessous récapitule quelques éléments clés que vous devez ajouter à vos applications.

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorations de DXGI 1,5](dxgi-1-5-improvements.md)
</dt> <dt>

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
