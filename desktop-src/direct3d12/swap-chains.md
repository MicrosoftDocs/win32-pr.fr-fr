---
title: Chaînes de permutation
description: Les chaînes d’échange contrôlent la rotation de la mémoire tampon d’arrière-plan, formant ainsi la base de l’animation graphique.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012867"
---
# <a name="swap-chains"></a>Chaînes de permutation

Les chaînes d’échange contrôlent la rotation de la mémoire tampon d’arrière-plan, formant ainsi la base de l’animation graphique.

## <a name="overview"></a>Vue d’ensemble

Le modèle de programmation pour les chaînes de permutation dans Direct3D 12 n’est pas identique à celui des versions antérieures de D3D. La commodité de programmation, par exemple, de prise en charge de la rotation automatique des ressources qui était présente dans D3D10 et D3D11 n’est pas prise en charge à l’heure actuelle. Les applications activées pour la rotation automatique des ressources permettent de restituer le même objet d’API, tandis que la surface réelle rendue change chaque cadre. Le comportement des chaînes de permutation est modifié avec Direct3D 12 pour permettre à d’autres fonctionnalités de Direct3D 12 d’avoir une surcharge de l’UC faible. La clé de couleur automatique et l’échantillonnage multiple ne sont pas pris en charge, bien que l’étirement et la rotation soient, en particulier, toujours.

### <a name="buffer-lifetime"></a>Durée de vie de la mémoire tampon

Les applications sont autorisées à stocker des descripteurs précréés qui font référence à des tampons d’arrière-plan. cette option est activée en garantissant que l’ensemble de mémoires tampons détenu par une chaîne de permutation ne change jamais pendant la durée de vie de la chaîne de permutation. L’ensemble de mémoires tampons retourné par [**IDXGISwapChain :: GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) ne change pas tant que certaines API ne sont pas appelées :

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

L’ordre des mémoires tampons retournées par [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) ne change jamais.

[**IDXGISwapChain3 :: GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) retourne l’index de la mémoire tampon d’arrière-plan actuelle à l’application.

### <a name="swap-effects"></a>Permuter les effets

Les seuls effets d’échange pris en charge sont [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) et [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), ce qui nécessite que le nombre de tampons soit supérieur à un.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Transition entre les modes fenêtre et plein écran

Direct3D 12 ne prend pas en charge le mode exclusif plein écran (FSE). Au lieu de cela, lorsqu’un jeu est la seule application visible à l’écran, le système d’exploitation utilise une stratégie appelée « optimisation de l’écran complet » (FSO) pour obtenir un effet similaire à FSE sans les inconvénients en matière de performances. Pour plus d’informations sur le FSO, consultez [démystification des optimisations en plein écran](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

Direct3D 12 maintient la restriction que les applications doivent appeler [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) après la transition entre les modes plein écran et avec fenêtres (les chaînes de permutation de modèle d3d11 présentent les mêmes restrictions).

Les transitions [**IDXGISwapChain :: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) ne modifient pas l’ensemble des mémoires tampons visibles par l’application dans la chaîne de permutation. Seuls les appels [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) et [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) créent ou détruisent des mémoires tampons visibles par l’application. Toutefois, dans Direct3D 12 [**IDXGISwapChain :: SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) ne passe pas en mode plein écran et modifie simplement les résolutions et les fréquences d’actualisation pour autoriser les optimisations en plein écran. Ces modifications peuvent être apportées par une application sans l’utilisation de cette méthode

Quand ou [**IDXGISwapChain ::P renvoyer**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) ou [**IDXGISwapChain1 ::P renvoyé**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) est appelé, la mémoire tampon d’arrière-plan à présenter doit être dans l’état d' [**État de \_ ressource D3D12 \_ \_ présent**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) . La présence échouera avec l' **erreur dxgi d' \_ \_ \_ appel non valide** si ce n’est pas le cas.

Les chaînes d’échange plein écran continuent d’avoir la restriction indiquant que [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(false, null) doit être appelé avant la version finale de la chaîne de permutation. **SetFullscreenState**(false) parvient sur les chaînes de permutation s’exécutant sur les périphériques Direct3D 12.

Les opérations présentes se produisent sur la file d’attente 3D fournie lors de la création de utilise permutation, et les applications sont libres de présenter simultanément plusieurs chaînes de permutation, ainsi que d’enregistrer et d’exécuter des listes de commandes.

Lorsque la dernière partie du travail (par exemple, le post-traitement des frames) est effectuée sur une file d’attente de calcul, ou n’implique pas la file d’attente graphique de l’appareil, la création d’une deuxième file d’attente 3D à présenter peut être bénéfique et empêcher la latence de la présentation qui retarde le début de la trame suivante. 

### <a name="example"></a>Exemple

L’exemple de code suivant est présent dans la boucle de rendu principale :

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Création de chaînes de permutation

Lors de l’utilisation des appels [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)ou [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) , Notez que le paramètre *pDevice* nécessite en fait un pointeur vers une file d’attente de commandes directe dans Direct3D 12, et non un appareil.

### <a name="presenting-on-windows-7"></a>présentation de Windows 7

quand vous ciblez direct3d 12 sur Windows 7, les types DXGI nécessaires pour direct3d 12 ne sont pas présents. vous devez donc utiliser le **ID3D12CommandQueueDownLevel** fourni par D3D12On7 (interrogé à partir de la file d’attente de commandes directe) à présenter.

vous fournissez une liste de commandes ouverte à la méthode Windows 7 présente, qui sera ensuite utilisée, fermée et automatiquement envoyée à l’appareil. Vous devez fournir une mémoire tampon d’arrière-plan qui doit être créée par l’application, doit être une ressource validée, doit avoir un échantillon unique et doit être de l’un des formats suivants.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Rubriques connexes

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Didacticiels vidéo sur DirectX Advanced Learning : fréquence d’images délimitée](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Rendu](rendering.md)
