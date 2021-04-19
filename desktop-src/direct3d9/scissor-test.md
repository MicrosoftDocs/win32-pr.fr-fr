---
description: Le test de ciseaux élimine les pixels qui se trouvent en dehors du rectangle symétrique, une sous-section rectangulaire définie par l’utilisateur de la cible de rendu.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Test de ciseaux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516760"
---
# <a name="scissor-test-direct3d-9"></a>Test de ciseaux (Direct3D 9)

Le test de ciseaux élimine les pixels qui se trouvent en dehors du rectangle symétrique, une sous-section rectangulaire définie par l’utilisateur de la cible de rendu.

Le rectangle à ciseaux peut être utilisé pour indiquer la zone de la cible de rendu où le monde du jeu est dessiné. La zone en dehors du rectangle est Culling et peut être dédiée à l’interface utilisateur graphique d’un jeu. Le test de ciseaux ne peut pas les zones non rectangulaires.

Les rectangles de ciseaux ne peuvent pas être plus grands que la cible de rendu, mais ils peuvent être plus grands que la fenêtre d’affichage.

Le rectangle de la ciseaux est géré par un état de rendu de l’appareil. Un test de ciseaux est activé ou désactivé en affectant à RenderState la **valeur true** ou **false**. Ce test est effectué après le calcul de la couleur du fragment, mais avant le test alpha. [**IDirect3DDevice9 :: SetRenderTarget**](/windows/desktop/api) réinitialise le rectangle de la ciseaux sur la cible de rendu complète, similaire à la fenêtre d’affichage réinitialisée. [**IDirect3DDevice9 :: SetScissorRect**](/windows/desktop/api) est enregistré par Stateblocks et [**IDirect3DDevice9 :: CreateStateBlock**](/windows/desktop/api) avec le paramètre d’État All (D3DSBT \_ toute la valeur dans [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)). Le test de ciseaux affecte également l’opération [**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) de l’appareil.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



Le rectangle à ciseaux par défaut est la fenêtre d’affichage complète.

Le test de ciseaux est effectué juste après la fin du traitement des pixels par un nuanceur de pixels ou le pipeline de fonction fixe, comme indiqué dans le diagramme suivant.

![diagramme de l’exécution du test de ciseaux par rapport à d’autres étapes](images/scissor-test.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 
