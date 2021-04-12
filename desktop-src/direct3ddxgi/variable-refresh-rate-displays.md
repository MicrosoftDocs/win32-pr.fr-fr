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
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="872f5-103">Affichage du taux d’actualisation des variables</span><span class="sxs-lookup"><span data-stu-id="872f5-103">Variable refresh rate displays</span></span>

<span data-ttu-id="872f5-104">Le taux d’actualisation des variables indique que le *déchirement* doit être activé, ce qui est également appelé prise en charge de la « Vsync ».</span><span class="sxs-lookup"><span data-stu-id="872f5-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="872f5-105">Le taux d’actualisation des variables affiche/Vsync désactivé</span><span class="sxs-lookup"><span data-stu-id="872f5-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="872f5-106">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="872f5-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="872f5-107">Le taux d’actualisation des variables affiche/Vsync désactivé</span><span class="sxs-lookup"><span data-stu-id="872f5-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="872f5-108">La prise en charge des taux d’actualisation des variables s’affiche en définissant certains indicateurs lors de la création et de la présentation de la chaîne de permutation.</span><span class="sxs-lookup"><span data-stu-id="872f5-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="872f5-109">Pour utiliser cette fonctionnalité, les utilisateurs de l’application doivent se trouver sur des systèmes Windows 10 avec [KB3156421](https://support.microsoft.com/kb/3156421) ou la mise à jour anniversaire installée.</span><span class="sxs-lookup"><span data-stu-id="872f5-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="872f5-110">La fonctionnalité fonctionne sur toutes les versions de Direct3D 11 et 12 à l’aide de l'*effet d’échange \* dxgi \_ \_ \_ bascule \_ \** _ permuter les effets.</span><span class="sxs-lookup"><span data-stu-id="872f5-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="872f5-111">Pour ajouter la prise en charge de Vsync à vos applications, vous pouvez vous référer à un exemple complet d’exécution pour Direct3D 12, _ *D3D12Fullscreen*\* (voir les [exemples de travail](../direct3d12/working-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="872f5-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="872f5-112">Il y a également quelques points qui ne sont pas explicitement appelés dans l’exemple de code, mais vous devez faire attention à.</span><span class="sxs-lookup"><span data-stu-id="872f5-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="872f5-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (ou [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) doit avoir le même indicateur de création de chaîne de permutation (dxgi d’activation de l' \_ indicateur de chaîne de permutation \_ \_ \_ \_ ) passé comme [**présent**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (ou [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span><span class="sxs-lookup"><span data-stu-id="872f5-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="872f5-114">DXGI \_ présente \_ autoriser le \_ déchirement ne peut être utilisé qu’avec l’intervalle de synchronisation 0.</span><span class="sxs-lookup"><span data-stu-id="872f5-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="872f5-115">Il est recommandé de toujours transmettre cet indicateur de suppression lors de l’utilisation de l’intervalle de synchronisation 0 si [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) signale que le déchirement est pris en charge *et* que l’application est en mode fenêtre, y compris le mode plein écran sans bordure.</span><span class="sxs-lookup"><span data-stu-id="872f5-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="872f5-116">Pour plus d’informations, reportez-vous aux constantes [**\_ présentes dans dxgi**](dxgi-present.md) .</span><span class="sxs-lookup"><span data-stu-id="872f5-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="872f5-117">La désactivation de Vsync ne UNCAP pas nécessairement votre fréquence d’images : les développeurs doivent également s’assurer que les appels [**présents**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) ne sont pas limités par d’autres événements de minutage (tels que l' `CompositionTarget::Rendering` événement dans une application XAML).</span><span class="sxs-lookup"><span data-stu-id="872f5-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="872f5-118">Le code ci-dessous récapitule quelques éléments clés que vous devez ajouter à vos applications.</span><span class="sxs-lookup"><span data-stu-id="872f5-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="872f5-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="872f5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="872f5-120">Améliorations de DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="872f5-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="872f5-121">Guide de programmation pour DXGI</span><span class="sxs-lookup"><span data-stu-id="872f5-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
