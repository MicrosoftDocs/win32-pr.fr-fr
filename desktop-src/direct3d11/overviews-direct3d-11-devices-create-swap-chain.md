---
title: Comment créer une chaîne de permutation
description: Cette rubrique montre comment créer une chaîne de permutation qui encapsule au moins deux mémoires tampons utilisées pour le rendu et l’affichage.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ef97b261d9831c451c8a81bfc1f4d9d13b1cd423ac28f38de4b90c1d4ae100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530571"
---
# <a name="how-to-create-a-swap-chain"></a>Comment : créer une chaîne de permutation

Cette rubrique montre comment créer une chaîne de permutation qui encapsule au moins deux mémoires tampons utilisées pour le rendu et l’affichage. Ils contiennent généralement un tampon d’avant présenté au périphérique d’affichage et une mémoire tampon d’arrière-plan qui sert de cible de rendu. Une fois le contexte immédiat rendu sur la mémoire tampon d’arrière-plan, la chaîne de permutation présente la mémoire tampon d’arrière-plan en échangeant les deux mémoires tampons.

La chaîne de permutation définit plusieurs caractéristiques de rendu, notamment :

-   Taille de la zone de rendu.
-   Fréquence d’actualisation de l’affichage.
-   Mode d'affichage.
-   Format de surface.

Définissez les caractéristiques de la chaîne de permutation en remplissant une structure [**desc de \_ \_ chaîne \_ de permutation dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) et en initialisant une interface [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) . Initialisez une chaîne de permutation en appelant [**IDXGIFactory :: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="create-a-device-and-a-swap-chain"></a>Créer un appareil et une chaîne de permutation

Pour initialiser un appareil et une chaîne de permutation, utilisez l’une des deux fonctions suivantes :

-   Utilisez la fonction [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) lorsque vous souhaitez initialiser la chaîne de permutation en même temps que l’initialisation de l’appareil. Il s’agit généralement de l’option la plus simple.

-   Utilisez la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) lorsque vous avez déjà créé une chaîne de permutation à l’aide de [**IDXGIFactory :: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 