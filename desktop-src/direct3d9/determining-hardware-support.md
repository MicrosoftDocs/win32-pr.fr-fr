---
description: Direct3D fournit les fonctions suivantes pour déterminer la prise en charge matérielle.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Détermination de la prise en charge matérielle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42dda0aa1e1d5d75d2c8b6f0364c08daa836e7d2f0996252748bbb49b3d2a4a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730632"
---
# <a name="determining-hardware-support-direct3d-9"></a>Détermination de la prise en charge matérielle (Direct3D 9)

Direct3D fournit les fonctions suivantes pour déterminer la prise en charge matérielle.

-   [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Permet de vérifier si un format de surface peut être utilisé comme texture, si un format de surface peut être utilisé comme texture et une cible de rendu, ou si un format de surface peut être utilisé comme tampon de stencil de profondeur. De plus, cette méthode est utilisée pour vérifier la prise en charge du format de mémoire tampon de profondeur et la prise en charge du format de tampon de stencil de profondeur.

-   [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Permet de vérifier la capacité d’un appareil à effectuer une accélération matérielle, la capacité d’un appareil à créer une chaîne de permutation à des fins de présentation ou la capacité d’un appareil à effectuer un rendu au format d’affichage actuel.

-   [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Permet de vérifier si un format de mémoire tampon de stencil de profondeur est compatible avec un format de cible de rendu. Notez qu’avant d’appeler cette méthode, l’application doit appeler [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sur les formats de stencil de profondeur et de cible de rendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
