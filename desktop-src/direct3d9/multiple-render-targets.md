---
description: Plusieurs cibles de rendu (MRT) se réfèrent à la possibilité d’effectuer un rendu sur plusieurs surfaces (consultez IDirect3D9Surface) avec un seul appel de dessin.
ms.assetid: ae48c5ce-b7f5-4189-8b04-880836be3fe0
title: Plusieurs cibles de rendu (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d617eb5912557620d9c11bc7fc1a6347fa79b5572abad7fdea0d729445205697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092901"
---
# <a name="multiple-render-targets-direct3d-9"></a>Plusieurs cibles de rendu (Direct3D 9)

Plusieurs cibles de rendu (MRT) se réfèrent à la possibilité d’effectuer un rendu sur plusieurs surfaces (consultez [**IDirect3D9Surface**](/windows/desktop/api)) avec un seul appel de dessin. Ces surfaces peuvent être créées indépendamment les unes des autres. Les cibles de rendu peuvent être définies à l’aide de [**IDirect3DDevice9 :: SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget).

Plusieurs cibles de rendu présentent les restrictions suivantes :

-   Toutes les surfaces cibles de rendu utilisées ensemble doivent avoir la même profondeur de bits, mais elles peuvent être de différents formats, sauf si la limite D3DPMISCCAPS \_ MRTINDEPENDENTBITDEPTHS est définie.
-   Toutes les surfaces d’une cible de rendu multiple doivent avoir la même largeur et la même hauteur.
-   Certaines implémentations ne peuvent pas effectuer d’opérations de nuanceur de zéros sur plusieurs cibles de rendu, notamment : aucune trame, aucun test alpha, aucune transparence, aucune fusion ni masquage, à l’exception du test z-test et du stencil. Les appareils qui prennent en charge les opérations de nuanceur après le pixel définissent le bit Cap sur D3DPMISCCAPS \_ MRTPOSTPIXELSHADERBLENDING.

    Lorsque l' \_ embout D3DPMISCCAPS MRTPOSTPIXELSHADERBLENDING est défini, vous devez d’abord consulter le [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec la \_ requête \_ d’utilisation POSTPIXELSHADER le \_ résultat de fusion pour le format de surface spécifique. Si la valeur est false, aucune opération de fusion de nuanceur de pixel postérieure n’est disponible pour ce format de surface spécifique. Si la valeur est true, l’appareil est censé appliquer le même État à toutes les cibles de rendu simultanées comme suit :

    -   Alpha Blend : la valeur de couleur dans oCi est mélangée avec la cible de rendu énième.
    -   Test alpha : la comparaison aura lieu avec oC0. Si la comparaison échoue, le test de pixel s’arrête pour toutes les cibles de rendu.
    -   Brouillard : la cible de rendu 0 va s’afficher. Les autres cibles de rendu ne sont pas définies. Les implémentations peuvent choisir de les survoiler toutes en utilisant le même État.
    -   Tramage : non défini.

-   Aucun anticrénelage n’est pris en charge.
-   Certaines implémentations n’appliquent pas le masque d’écriture de sortie (D3DRS \_ COLORWRITEENABLE). Ceux qui peuvent avoir des masques d’écriture de couleur indépendants. Cela est exprimé à l’aide d’un nouveau bit de fonctionnalité. Le nombre de masques d’écriture de couleur indépendants disponibles sera égal au nombre maximal d’éléments que l’appareil est en capacité de prendre en charge.

Nouvelles extrémités matérielles :


```
D3DCAPS9.NumSimultaneousRTs         
// The value is 1 for all hardware except those that  
//   can support this feature. It is never 0.
D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS - True if the hardware can support it
D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING - True if the hardware can support it
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 
