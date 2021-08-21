---
description: La couleur de brouillard pour le brouillard de pixel et de vertex est définie via l' \_ État de rendu D3DRS FOGCOLOR. Les valeurs d’état de rendu peuvent être n’importe quelle couleur RVB, spécifiée comme une couleur RVBA. Le composant alpha est ignoré.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Couleur de brouillard (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 395bb17c9d6495ade54bc7c761b8c8024c53fbd9a51f620a45ee3a807dc6e20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987999"
---
# <a name="fog-color-direct3d-9"></a>Couleur de brouillard (Direct3D 9)

La couleur de brouillard pour le brouillard de pixel et de vertex est définie via l' \_ État de rendu D3DRS FOGCOLOR. Les valeurs d’état de rendu peuvent être n’importe quelle couleur RVB, spécifiée comme une couleur RVBA. Le composant alpha est ignoré.

L’exemple C++ suivant définit la couleur de brouillard sur blanc.


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



Le brouillard est appliqué différemment par le pipeline de fonction fixe et le pipeline programmable.

1.  Si le pilote prend en charge D3DPMISCCAPS \_ FOGANDSPECULARALPHA :
    -   Si le pipeline de fonction fixe est utilisé et que D3DRS \_ FOGCOLOR est défini, v1. w (dans le nuanceur de pixels) est égal à la valeur définie dans le RenderState de brouillard.
    -   Si le pipeline programmable est utilisé, v1. w (dans le nuanceur de pixels) est égal à 0, même si oD1. w est écrit explicitement dans un nuanceur de sommets.
2.  Si le pilote ne prend pas en charge D3DPMISCCAPS \_ FOGANDSPECULARALPHA :
    -   Si le pipeline de fonction fixe est utilisé et que D3DRS \_ FOGCOLOR est défini, v1. w (dans le nuanceur de pixels) est égal à la valeur définie dans le RenderState de brouillard.
    -   Si oFog est écrit explicitement dans un nuanceur de sommets, v1. w (dans le nuanceur de pixels) est égal à oFog, placé entre 0 et 1.
    -   Si aucun des deux cas ci-dessus ne s’applique, v1. w (dans le nuanceur de pixels) est égal à 0, même si oD1. w est écrit explicitement dans un nuanceur de sommets.

Pour plus d’informations, consultez [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de brouillard](fog-types.md)
</dt> </dl>

 

 



