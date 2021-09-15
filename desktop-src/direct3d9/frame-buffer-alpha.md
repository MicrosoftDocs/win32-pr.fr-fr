---
description: La fusion alpha de la mémoire tampon de frame est un peu différente du vertex alpha, du matériau alpha et de la texture alpha.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Mémoire tampon de trame alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516841"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Mémoire tampon de trame alpha (Direct3D 9)

La fusion alpha de la mémoire tampon de frame est un peu différente du vertex alpha, du matériau alpha et de la texture alpha. Les valeurs de transparence de jeu alpha de vertex, de matériau et de texture, qui sont utilisées uniquement pour la primitive actuelle, et qui n’ont pas d’effet sur d’autres Primitives. La fonction de fusion alpha de la mémoire tampon de trame contrôle la manière dont la primitive actuelle est combinée avec les pixels existants dans la mémoire tampon de trame pour produire une couleur de pixel finale.

Lors de l’exécution de la fusion alpha, deux couleurs sont combinées : une couleur source et une couleur de destination. La couleur source provient de l’objet transparent, la couleur de destination est la couleur qui figure déjà à l’emplacement du pixel. La couleur de destination est le résultat du rendu d’un autre objet qui se trouve derrière l’objet transparent, autrement dit, l’objet qui sera visible via l’objet transparent. La fusion alpha utilise une formule pour contrôler le rapport entre les objets source et de destination.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor est la contribution de la primitive rendue à l’emplacement de pixel actuel. PixelColor est la contribution de la mémoire tampon de trame à l’emplacement actuel du pixel.

L’ensemble des facteurs alpha Blend qui peuvent être utilisés sont répertoriés ci-dessous.



| Facteur de mode de fusion         | Description                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ zéro            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ un             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (RS, GS, BS, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1-RS, 1-GS, 1-BS, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (As, As, As, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-As, 1-As, 1-As, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (AD, ad, ad, AD)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1-AD, 1-AD, 1-AD, 1-AD)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (Rd, GD, BD, AD)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-gd, 1-BD, 1-AD)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min (As, 1-AD)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Obsolète pour DirectX 6 et versions ultérieures. Vous pouvez obtenir le même effet en définissant les facteurs de fusion source et destination sur D3DBLEND \_ SRCALPHA et D3DBLEND \_ INVSRCALPHA dans des appels distincts. |
| D3DBLEND \_ BOTHINVSRCALPHA | Obsolète pour DirectX 6. Vous pouvez obtenir le même effet en définissant les facteurs de fusion source et destination sur D3DBLEND \_ INVSRCALPHA et D3DBLEND \_ SRCALPHA dans des appels distincts.           |
| D3DBLEND \_ BLENDFACTOR     | Utilisez Color. r, Color. g, Color. b et Color. a obtenu à partir du \_ paramètre D3DRS BLENDFACTOR.                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Utilisez 1-Color. r, 1-Color. g, 1-Color. b et 1-Color. a obtenu à partir du \_ paramètre D3DRS BLENDFACTOR.                                                                                         |



 

Direct3D utilise l' \_ État de rendu D3DRS ALPHABLENDENABLE pour activer la fusion de la transparence alpha. Le type de fusion alpha effectué dépend des \_ États de rendu D3DRS SRCBLEND et D3DRS \_ DESTBLEND. Les États de fusion de source et de destination sont utilisés par paires. Le fragment de code suivant définit l’état de fusion source sur D3DBLEND \_ SRCCOLOR et l’état de fusion de destination sur D3DBLEND \_ INVSRCCOLOR.


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



Ce code effectue un mélange linéaire entre la couleur source (la couleur de la primitive rendue à l’emplacement actuel) et la couleur de destination (la couleur à l’emplacement actuel dans la mémoire tampon de trame). L’apparence qui en résulte est semblable au verre teinté, car une partie de la couleur de l’objet de destination semble être transmise via l’objet source. le reste de celui-ci semble être absorbé.

La plupart de ces facteurs de mélange nécessitent des valeurs alpha dans la texture pour fonctionner correctement. Ainsi, lorsque vous utilisez un vertex ou un matériau alpha, l’application est limitée quant aux modes qui produiront des résultats intéressants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion alpha](alpha-blending.md)
</dt> </dl>

 

 



