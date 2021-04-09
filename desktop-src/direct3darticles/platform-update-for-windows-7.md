---
title: Mise à jour de plateforme pour Windows 7
description: Cette rubrique décrit les améliorations apportées aux composants de la pile graphique Windows 7 qui deviennent disponibles via la mise à jour de plateforme pour Windows 7.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842630"
---
# <a name="platform-update-for-windows-7"></a>Mise à jour de plateforme pour Windows 7

Cette rubrique décrit les améliorations apportées aux composants de la pile graphique Windows 7 qui deviennent disponibles via la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838).

Lorsqu’elle est installée sur Windows 7, la mise à jour de la plateforme pour Windows 7 met à jour Windows 7 avec les fonctionnalités disponibles dans Windows 8. Par exemple, ces composants Windows 8 deviennent disponibles avec toutes les fonctionnalités :

-   Direct2D 1,1 (y compris les effets Direct2D)
-   DirectWrite
-   Composant Imagerie Windows (WIC)

Celles-ci fournissent des fonctionnalités partielles :

-   Direct3D 11,1
-   DXGI 1,2

Et, par exemple, ce composant n’est pas disponible :

-   DirectComposition (DComp)

Pour plus d’informations sur Direct2D, DirectWrite et WIC avec la mise à jour de la plateforme, consultez les rubriques suivantes :

-   [Nouveautés de Direct2D pour Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Nouveautés de DirectWrite pour Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Nouveautés de WIC dans Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Pour plus d’informations sur Direct3D et DXGI avec la mise à jour de la plateforme, consultez les rubriques suivantes :

-   [Fonctionnalités D3D 11.1](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [Améliorations de DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Une fois la mise à jour de la plateforme installée, les interfaces introduites dans Direct3D 11.1 et DXGI 1,2 sont disponibles avec des fonctionnalités partielles. Les fonctionnalités de ces composants graphiques sont directement liées aux composants du noyau Graphics, aux pilotes graphiques et au matériel graphique. Avant d’utiliser Direct3D 11.1 sur Windows 7, familiarisez-vous avec ces caractéristiques :

-   Windows 8 a introduit le modèle de pilote WDDM 1,2, qui a apporté des améliorations à l’ensemble de la surface d’API associée pour tous les [niveaux de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro). Lors de la lecture de la documentation de Direct3D 11.1, sachez que les *nouveaux pilotes* sont les pilotes WDDM 1,2. Ces versions de pilote mises à jour, ainsi que la plupart des fonctionnalités facultatives exposées via [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport), ne sont pas disponibles sur Windows 7. Étant donné qu’il n’y a aucune garantie que ces fonctionnalités facultatives sont disponibles, assurez-vous que vos applications ont des comportements de secours appropriés dans le cas où la fonctionnalité souhaitée n’est pas disponible.

    Il y a une exception importante. Plusieurs fonctionnalités, telles que [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) avec des décalages de mémoire tampon constants, nécessitent de nouveaux pilotes pour le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 et versions ultérieures, mais elles sont en réalité émulées pour le niveau de fonctionnalité 9. Cette émulation est disponible sur Windows 7 avec la mise à jour de la plateforme. Pour plus d’informations sur les fonctionnalités émulées, consultez [**\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .

-   Le modèle de pilote WDDM 1,2 de Windows 8 prend en charge une nouvelle génération de matériel, exposée via le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) D3D 11,1. Windows 7 avec la mise à jour de plateforme ne prend en charge que le modèle de pilote WDDM 1,1 et, par conséquent, la prise en charge matérielle de niveau de fonctionnalité 11,1 n’est pas disponible (via la mise à jour de la plateforme). Sur Windows 7 avec la mise à jour de la plateforme, [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) retourne toujours un niveau de fonctionnalité de 11,0 ou une valeur antérieure, à l’exception de avec un appareil de référence qui peut être utilisé pour tester un chemin de code 11,1 sur Windows 7. Utilisez uniquement les fonctionnalités disponibles à vos niveaux de fonctionnalités cibles, comme décrit dans la référence de niveau de fonctionnalité.
-   Certaines nouvelles méthodes introduites dans DGXI 1,2 ne sont pas entièrement prises en charge avec la mise à jour de plateforme pour Windows 7. vous pouvez tester la disponibilité de ces fonctions en les appelant directement et en vérifiant l’existence d’un code d’erreur. Assurez-vous que vos applications ciblant Windows 7 avec la mise à jour de la plateforme ont une solution de secours en place lorsque la fonctionnalité souhaitée n’est pas disponible. Ces classes de fonctionnalités ne sont pas disponibles sur la mise à jour de plateforme pour Windows 7 :

    -   Stéréo
    -   Chaînes d’échange ne cible pas les HWND
    -   Notifications d’état d’occlusion
    -   Duplication des postes de travail
    -   Ressources de handle NT

    Plus précisément, les API suivantes renvoient une \_ erreur dxgi \_ non prise en charge, DXGI \_ Error \_ invalid \_ Call, e \_ NOTIMPL ou e \_ INVALIDARG :

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Ces API présentent des différences de comportement, comme indiqué ci-dessous :
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) prend une [**structure \_ \_ \_ DESC1 de chaîne d’échange dxgi**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) , qui a un champ pour la mise à **l’échelle**. [**Dxgi \_ La mise \_ à l’échelle**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) n’est pas prise en charge sur Windows 7 avec la mise à jour de la plateforme et provoque le renvoi par **CreateSwapChainForHwnd** d’un \_ \_ appel non valide dxgi \_ .
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) est utile uniquement lorsqu’il est défini sur un utilise permutation à l’aide de la \_ mise à l’échelle dxgi \_ None. Sa valeur est toujours stockée et peut être récupérée, mais elle n’a aucun effet.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)et [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) retournent tous la **valeur false**.
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) et **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) ont été ajoutés pour faciliter les modes d’affichage stéréo. Le stéréo n’est pas pris en charge sur la mise à jour de plateforme pour Windows 7. cette méthode est donc équivalente à [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) en [**\_ mode dxgi \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). La valeur stéréo est toujours FALSe.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) et **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) ne sont pas pris en charge sur la mise à jour de plateforme pour Windows 7. Toutefois, le runtime les autorise toujours à être appelé et effectue une validation qu’ils sont utilisés correctement sur des ressources non partagées.
    -   Les appareils [Warps](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) prennent uniquement en charge le [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0. Autrement dit, les appareils distorsions créés en passant le paramètre de [ \_ \_ type \_ Warp du pilote D3D](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) dans le paramètre *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) ne prennent pas en charge 11,1 et ne prennent pas en charge les surfaces partagées.
-   Pour les développeurs qui travaillent actuellement sur des applications dans Microsoft Visual Studio 2010 ou version antérieure à l’aide de l’indicateur de [**\_ \_ \_ débogage d3d11 créer un appareil**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) , sachez que les appels à [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) échoueront. Cela est dû au fait que le runtime D3D 11.1 requiert désormais D3D11 \_1SDKLayers.dll au lieu de D3D11SDKLayers.dll. Pour accéder à cette nouvelle DLL (D3D11 \_1SDKLayers.dll), installez le [Kit de développement logiciel (SDK) Windows 8](https://dev.windows.com/downloads/windows-8-sdk)ou [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)ou les outils de débogage à distance de Visual Studio 2012. Pour plus d’informations, consultez la documentation de la [couche de débogage](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) .

 

 