---
description: Les fonctionnalités suivantes ont été ajoutées ou modifiées dans Microsoft DirectX Graphics infrastructure (DXGI) 1,4, principalement pour prendre en charge Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: Améliorations de DXGI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e9a8a48dd026248afac7c1a7df23a99176adef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033415"
---
# <a name="dxgi-14-improvements"></a>Améliorations de DXGI 1,4

Les fonctionnalités suivantes ont été ajoutées ou modifiées dans Microsoft DirectX Graphics infrastructure (DXGI) 1,4, principalement pour prendre en charge Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Énumération des adaptateurs les plus économiques

Pour Direct3D 12, il n’est plus possible de revenir d’un appareil au [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) utilisé pour le créer. Il n’est pas non plus possible de fournir \_ la \_ distorsion de type de pilote D3D \_ dans [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice). Pour faciliter le développement, vous pouvez utiliser [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) pour gérer les deux. [**IDXGIFactory4 :: EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (conçu pour être associé à [**ID3D12Device :: GetAdapterLuid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)) permet à une application de récupérer des informations sur l’adaptateur sur lequel un appareil Direct3D 12 a été créé. [**IDXGIFactory4 :: EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) fournit un adaptateur qui peut être fourni à **D3D12CreateDevice** pour utiliser le convertisseur de distorsion.

## <a name="video-memory-budget-tracking"></a>Suivi des budgets de mémoire vidéo

Les développeurs d’applications sont encouragés à utiliser un système de réservation de mémoire vidéo pour informer le système d’exploitation de la quantité de mémoire vidéo physique que l’application ne peut pas déconnecter sans.

La quantité de mémoire physique disponible pour un processus est connue sous le nom de « budget de la mémoire vidéo ». Le budget peut fluctuer de façon notable au fur et à mesure de l’éveil et du sommeil des processus d’arrière-plan ; et fluctuent considérablement lorsque l’utilisateur passe à une autre application. L’application peut être avertie lorsque le budget change et interroger à la fois le budget actuel et la quantité de mémoire actuellement consommée. Si une application ne reste pas dans son budget, le processus sera gelé par intermittence pour permettre à d’autres applications de s’exécuter et/ou les API de création renverront un échec. L’interface [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fournit les méthodes relatives à cette fonctionnalité, en particulier [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) et [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Pour plus d’informations, reportez-vous à la rubrique Direct3D 12 consacrée à la [résidence](../direct3d12/residency.md).

## <a name="direct3d-12-swapchain-changes"></a>Modifications de Direct3D 12 utilise permutation

Une partie de la fonctionnalité de utilise permutation Direct3D 11 existante a été dépréciée pour atteindre les réductions de la surcharge dans Direct3D 12. Bien que d’autres modifications aient été apportées pour s’aligner sur les concepts Direct3D 12 ou offrir une meilleure prise en charge des fonctionnalités Direct3D 12.

**Identité de la mémoire tampon d’invariant**

Dans Direct3D 11, les applications pouvaient appeler [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)(0,... ) une seule fois. Chaque appel à [**présent**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) a modifié implicitement l’identité de ressource de l’interface retournée. Direct3D 12 ne prend plus en charge cette modification de l’identité de ressource implicite, en raison de la surcharge du processeur requise et de la conception du descripteur de ressource flexible. Par conséquent, l’application doit appeler manuellement **GetBuffer** pour chaque mémoire tampon créée avec utilise permutation. L’application doit effectuer un rendu manuel à la mémoire tampon suivante dans la séquence après l’appel de la **présente**. Les applications sont encouragées à créer un cache de descripteurs pour chaque mémoire tampon, plutôt que de recréer un grand nombre d' **objets.**

**Prise en charge de plusieurs adaptateurs**

Lorsqu’un utilise permutation est créé sur un adaptateur à plusieurs GPU, les mémoires tampons sont toutes créées sur le nœud 1 et une seule file d’attente de commandes est prise en charge. [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) permet aux applications de créer des mémoires tampons en attente sur des nœuds différents, ce qui permet d’utiliser une file d’attente de commandes différente avec chacune. Ces fonctionnalités permettent l’utilisation de techniques de rendu de frames (AFR) supplémentaires avec utilise permutation. Reportez-vous à [systèmes à plusieurs adaptateurs](../direct3d12/multi-engine.md).

**Divers**

-   Un objet de file d’attente de commandes doit être passé aux méthodes [**CreateSwapChain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) à la place de l’objet appareil Direct3D 12.
-   Seuls les deux effets de basculement de modèle suivants sont pris en charge : <dl> DXGI \_ swap \_ Effect \_ Flip \_ ignore doit être préféré quand les applications effectuent un rendu complet sur la mémoire tampon d’application avant de la présenter ou s’intéressent facilement à la prise en charge de scénarios à plusieurs adaptateurs.  
    \_L’effet d’échange dxgi \_ \_ retourne \_ séquentiel doit être utilisé par les applications qui reposent sur des optimisations de présentation partielles ou lues régulièrement à partir de mémoires tampons de cache présentées précédemment.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Rubriques connexes

[Niveaux de fonctionnalité matérielle Direct3D 12](../direct3d12/hardware-feature-levels.md)

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
