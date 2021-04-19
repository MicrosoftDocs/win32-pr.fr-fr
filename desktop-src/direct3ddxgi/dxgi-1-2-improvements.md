---
description: Les fonctionnalités suivantes ont été ajoutées dans Microsoft DirectX Graphics infrastructure (DXGI) 1,2.
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: Améliorations de DXGI 1.2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd274918d179bc7adeb8dd132fe604cf56d80f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515306"
---
# <a name="dxgi-12-improvements"></a>Améliorations de DXGI 1.2

Les fonctionnalités suivantes ont été ajoutées dans Microsoft DirectX Graphics infrastructure (DXGI) 1,2.

## <a name="presentation-enhancements-and-optimizations"></a>Améliorations et optimisations de la présentation

DXGI 1,2 améliore la présentation avec une nouvelle chaîne de permutation-modèle, une protection de contenu, une présentation sans fenêtre et une présentation optimisée dans laquelle vous spécifiez des rectangles incorrects et des zones défilantes. La présentation est également améliorée avec le comportement d’affichage 3D stéréoscopique.

Vous pouvez utiliser l’API DXGI 1,2 suivante pour une présentation améliorée.

-   [**IDXGIDisplayControl::IsStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**IDXGIDisplayControl::SetStereoEnabled**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2::CreateSwapChainForHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2::CreateSwapChainForComposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2::IsWindowedStereoEnabled**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2::RegisterStereoStatusWindow**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2::RegisterStereoStatusEvent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2::UnregisterStereoStatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2::RegisterOcclusionStatusWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2::RegisterOcclusionStatusEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2::UnregisterOcclusionStatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1::CreateSubresourceSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2 :: GetResource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1::GetFullscreenDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1::GetHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1::GetCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1::IsTemporaryMonoSupported**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1::GetRestrictToOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1::SetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1::GetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

Pour plus d’informations sur l’utilisation de l’API DXGI 1,2 pour une présentation améliorée, consultez [amélioration de la présentation avec le modèle de retournement, rectangles modifiés et zones déroulantes](dxgi-1-2-presentation-improvements.md).

Pour plus d’informations sur la façon de déterminer si vous pouvez effectuer un rendu en stéréo, consultez [rendu en stéréo et notification à propos de l’État stéréo](stereo-rendering-stereo-status-notifying.md).

Pour plus d’informations sur la façon de déterminer les modifications de l’état d’occlusion de votre application, consultez [attente d’un événement lorsque le rendu est inutile](waiting-when-occluded.md).

Pour plus d’informations sur la modification des valeurs de données lorsque vous présentez du contenu à l’écran, consultez [conversion de données pour l’espace colorimétrique](converting-data-color-space.md).

## <a name="desktop-duplication"></a>Duplication des postes de travail

Windows 8 désactive les pilotes de mise en miroir Windows 2000 Display Driver Model (XDDM) standard. DXGI 1,2 fournit l’API de duplication de bureau comme alternative. L’API de duplication de bureau fournit un accès à distance à l’image de bureau pour les scénarios de collaboration.

L’API de duplication de bureau est constituée des méthodes suivantes.

-   [**IDXGIOutput1 ::D uplicateOutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**IDXGIOutputDuplication::GetDesc**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**IDXGIOutputDuplication::GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**IDXGIOutputDuplication::MapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**IDXGIOutputDuplication::UnMapDesktopSurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**IDXGIOutputDuplication::ReleaseFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

Pour plus d’informations sur l’utilisation de l’API de duplication de bureau, consultez [API de duplication de bureau](desktop-dup-api.md).

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>Amélioration de l’utilisation des ressources partagées et des événements synchronisés

Dans les versions précédentes de Windows, les applications utilisent l’interrogation continue pour déterminer si l’unité de traitement graphique (GPU) a fini de traiter des commandes arbitraires. DXGI 1,2 permet à une application d’effectuer la mise en file d’attente d’un événement sur un appareil DXGI. L’application peut ensuite attendre que l’appareil DXGI signale l’événement pour déterminer que le GPU a fini d’exécuter toutes les commandes de rendu. DXGI 1,2 permet à plusieurs appareils de partager une ressource par le biais d’un handle NT.

Vous pouvez utiliser l’API DXGI 1,2 et l’API Direct3D 11,1 suivantes pour partager des ressources et synchroniser des événements.

-   [**IDXGIDevice2::EnqueueSetEvent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1::CreateSharedHandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2::GetSharedResourceAdapterLuid**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1::OpenSharedResourceByName**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**D3D11 \_ ressources \_ \_ partagées divers \_ NTHANDLE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>Offrir la mémoire vidéo des ressources

DXGI 1,2 permet à une application d’offrir la mémoire vidéo de ses ressources avec une faible surcharge. En offrant la mémoire vidéo, le système d’exploitation peut libérer de la mémoire vidéo.

Cette fonctionnalité DXGI 1,2 se compose des méthodes suivantes.

-   [**IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2::ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

Vous pouvez utiliser la méthode [**ID3D11Debug :: SetFeatureMask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) pour définir des indicateurs de masque de fonctionnalité qui déboguent le comportement des méthodes [**IDXGIDevice2 :: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) et [**IDXGIDevice2 :: ReclaimResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) dans votre application.

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>Préemption GPU à des niveaux de granularité plus fins pour le modèle de pilote WDDM 1,2

À compter du modèle de pilote WDDM (Windows Display Driver Model) 1,2, le planificateur WDDM peut préempter l’exécution des tâches de l’application par le GPU à des niveaux de granularité plus précis. DXGI 1,2 vous permet de déterminer les niveaux de granularité de préemption du GPU.

Cette fonctionnalité DXGI 1,2 est constituée de la méthode suivante.

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>API de débogage

Le kit de développement logiciel (SDK) Windows 8 fournit des fonctionnalités de débogage supplémentaires. Vous pouvez utiliser les API DXGI suivantes à partir de Dxgidebug.dll pour déboguer votre application :

-   [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Pour accéder à [**DXGIGetDebugInterface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface), appelez la fonction [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) pour accéder Dxgidebug.dll et la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer l’adresse de **DXGIGetDebugInterface**. Vous pouvez ensuite appeler **DXGIGetDebugInterface** pour obtenir l’interface [**IDXGIDebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) ou [**IDXGIInfoQueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) .

Pour plus d’informations sur le débogage des applications DirectX à distance, consultez [débogage des applications DirectX à distance](../direct3dtools/debugging-directx-apps-remotely.md).

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
