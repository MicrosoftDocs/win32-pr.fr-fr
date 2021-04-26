---
description: Indicateurs de capacité du stencil du pilote.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6716748d77fe4c3620413f43ae4a4ae48076c09f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997376"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Indicateurs de capacité du stencil du pilote.



| \#définition                 | Value       | Description                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ conserver     | 0x00000001L | Ne mettez pas à jour l’entrée dans la mémoire tampon du stencil. Il s’agit de la valeur par défaut.                             |
| D3DSTENCILCAPS \_ zéro     | 0x00000002L | Affectez à l’entrée de tampon stencil la valeur 0.                                                                    |
| D3DSTENCILCAPS \_ remplacer  | 0x00000004L | Remplacez l’entrée stencil-tampon par la valeur de référence.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Incrémentez l’entrée de mémoire tampon du stencil, en la conservant à la valeur maximale.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Décrémenter l’entrée de mémoire tampon du stencil, en la mettant à zéro.                                                 |
| D3DSTENCILCAPS \_ inversé   | 0x00000020L | Inversez les bits dans l’entrée de mémoire tampon du stencil.                                                          |
| \_Incr D3DSTENCILCAPS     | 0x00000040L | Incrémente l’entrée de mémoire tampon du stencil, en renvoyant à zéro si la nouvelle valeur dépasse la valeur maximale.      |
| D3DSTENCILCAPS \_ DECR (     | 0x00000080L | Décrémente l’entrée de mémoire tampon du stencil, en renvoyant à la valeur maximale si la nouvelle valeur est inférieure à zéro. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | L’appareil prend en charge le stencil à deux côtés.                                                                |



 

Les entrées de mémoire tampon de stencil sont des valeurs entières comprises entre 0 et 2 ⁿ-1, où n est la profondeur en bits de la mémoire tampon du stencil.

Ces constantes sont utilisées par le membre StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



|                          |            |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



