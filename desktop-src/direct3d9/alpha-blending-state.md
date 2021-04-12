---
description: La valeur alpha d’une couleur contrôle sa transparence. L’activation de la fusion alpha permet de fusionner les couleurs, les matériaux et les textures sur une surface avec une transparence sur une autre surface.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: État de fusion alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393123"
---
# <a name="alpha-blending-state-direct3d-9"></a>État de fusion alpha (Direct3D 9)

La valeur alpha d’une couleur contrôle sa transparence. L’activation de la fusion alpha permet de fusionner les couleurs, les matériaux et les textures sur une surface avec une transparence sur une autre surface.

Pour plus d’informations, consultez [fusion de texture alpha (Direct3D 9)](alpha-texture-blending.md) et [fusion de texture (Direct3D 9)](texture-blending.md).

Les applications écrites en C++ utilisent l’état de rendu [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) pour activer la fusion de la transparence alpha. L’API Direct3D autorise un grand nombre de types de fusions alpha. Toutefois, il est important de noter que le matériel 3D de l’utilisateur peut ne pas prendre en charge tous les États de fusion autorisés par Direct3D.

Le type de fusion alpha effectué dépend des États de rendu [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) et **D3DRS \_ DESTBLEND** . Les États de fusion de source et de destination sont utilisés par paires. L’exemple de code suivant montre comment l’état de fusion source est défini sur D3DBLEND \_ SRCCOLOR et que l’état de fusion de destination est défini sur D3DBLEND \_ INVSRCCOLOR.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



La modification des États de fusion source et de destination peut entraîner l’apparition d’objets émissif dans une atmosphère à la buée ou poussiéreuse. Par exemple, si votre application modélise des flammes, des champs de force, des faisceaux plasma ou des objets rayonnants de la même manière, définissez les États de fusion source et destination sur D3DBLEND \_ .

Une autre application de la fusion alpha consiste à contrôler l’éclairage dans une scène 3D, également appelée « mappage de lumière ». La définition de l’état de fusion source sur D3DBLEND \_ zéro et l’état de fusion de destination sur D3DBLEND \_ SRCALPHA assombrit une scène en fonction des informations alpha de la source. La primitive source est utilisée comme une carte légère qui met à l’échelle le contenu de la mémoire tampon de trame pour l’assombrir quand cela est approprié. Cela produit un mappage de lumière monochrome.

Vous pouvez obtenir le mappage de la lumière en couleur en définissant l’état de fusion alpha source sur D3DBLEND \_ zéro et l’état de fusion de destination sur D3DBLEND \_ SRCCOLOR.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
