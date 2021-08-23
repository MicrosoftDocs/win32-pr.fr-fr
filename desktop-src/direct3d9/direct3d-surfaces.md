---
description: Une surface représente une zone linéaire de la mémoire d’affichage et se trouve généralement dans la mémoire d’affichage de la carte d’affichage, bien que les surfaces puissent exister dans la mémoire système. Les surfaces sont gérées par l’interface IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Surfaces Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 529320673eca39cf4b9afdb96377295d595191fd79cd81c316b258841d82ae6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988199"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Surfaces Direct3D (Direct3D 9)

Une surface représente une zone linéaire de la mémoire d’affichage et se trouve généralement dans la mémoire d’affichage de la carte d’affichage, bien que les surfaces puissent exister dans la mémoire système. Les surfaces sont gérées par l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .

-   Mémoire tampon d’avant. Rectangle de mémoire qui est traduit par la carte graphique et affiché sur le moniteur. Dans Direct3D, une application n’écrit jamais directement dans le tampon d’avant.
-   Mémoire tampon d’arrière-plan. Rectangle de mémoire dans lequel une application peut écrire directement. La mémoire tampon d’arrière-plan n’est jamais directement affichée sur le moniteur.
-   Retournement des surfaces. Processus de déplacement de la mémoire tampon d’arrière-plan vers la mémoire tampon d’arrière-plan.
-   Chaîne de permutation. Collection d’une ou plusieurs mémoires tampons d’arrière-plan qui peuvent être présentées en série au tampon d’avant.

## <a name="getting-a-surface"></a>Obtention d’une surface

Créez une surface en appelant l’une des méthodes suivantes :

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Les formats de surface déterminent la façon dont les données pour chaque pixel de la mémoire de surface sont interprétées. Direct3D utilise le membre [D3DFORMAT](d3dformat.md) de la structure [**D3DSURFACE \_ desc**](d3dsurface-desc.md) pour décrire le format de surface. Vous pouvez récupérer le format d’une surface existante en appelant la méthode [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .

Une fois qu’une surface est créée, vous pouvez obtenir un pointeur vers celle-ci en appelant l’une des méthodes suivantes :

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

L’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) vous permet d’accéder indirectement à la mémoire par le biais de la méthode [**UpdateSurface**](/windows/desktop/api) . Cette méthode vous permet de copier une zone rectangulaire de pixels d’une interface **IDirect3DSurface9** vers une autre interface **IDirect3DSurface9** . L’interface surface possède également des méthodes pour accéder directement à la mémoire d’affichage. Par exemple, vous pouvez utiliser la méthode [**LockRect**](/windows/desktop/api) pour verrouiller une zone rectangulaire de mémoire d’affichage. Il est important d’appeler [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) une fois que vous avez fini d’utiliser la zone rectangulaire verrouillée sur l’aire.

## <a name="additional-surface-topics"></a>Rubriques supplémentaires sur la surface

Apprenez-en davantage sur l’utilisation des surfaces avec l’une des rubriques suivantes :

-   [Formats de surface (Direct3D 9)](surface-formats.md)
-   [Qu’est-ce qu’une chaîne de permutation ? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Largeur et inclinaison (Direct3D 9)](width-vs--pitch.md)
-   [Retournement des surfaces (Direct3D 9)](flipping-surfaces.md)
-   [Mise en mémoire tampon de basculement et de page (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Copier dans des surfaces (Direct3D 9)](copying-to-surfaces.md)
-   [Copie de surfaces (Direct3D 9)](copying-surfaces.md)
-   [Accès direct à la mémoire de surface (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Données de surface privée (Direct3D 9)](private-surface-data.md)
-   [Contrôles gamma (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 
