---
description: La distorsion visible dans les texels d’un objet 3D dont la surface est orientée à un angle par rapport au plan de l’écran est appelée anisotrope.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Filtrage de texture anisotrope (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363aeef463f137a240602e52410260108ee4a40a1a23da7b2e7c245ed6e74a65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676939"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Filtrage de texture anisotrope (Direct3D 9)

La distorsion visible dans les texels d’un objet 3D dont la surface est orientée à un angle par rapport au plan de l’écran est appelée anisotrope. Lorsqu’un pixel d’une primitive anisotrope est mappé à des texels, sa forme est déformée. Direct3D mesure l’anisotropie d’un pixel comme un allongement, c’est-à-dire une longueur divisée par la largeur d’un pixel d’écran qui est mappé inversement à l’espace de texture.

Vous pouvez utiliser le filtrage de texture anisotrope conjointement avec le filtrage de texture linéaire ou le filtrage de texture mipmap pour améliorer les résultats de rendu. Votre application active le filtrage de texture anisotrope en appelant la méthode [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Définissez la valeur du premier paramètre sur le numéro d’index entier (0-7) de la texture pour laquelle vous sélectionnez une méthode de filtrage de texture. Transmettez D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER pour le deuxième paramètre afin de définir le filtre d’agrandissement, de minimisation ou de mappage MIP. Définissez le troisième paramètre sur D3DTEXF \_ anisotrope.

Votre application doit également définir le degré de l’anisotropie sur une valeur supérieure à un. Pour ce faire, appelez la méthode [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Définissez la valeur du premier paramètre sur le numéro d’index entier (0-7) de la texture pour laquelle vous définissez le degré de isotropy. Transmettez D3DSAMP \_ MAXANISOTROPY comme valeur du deuxième paramètre. Le dernier paramètre doit être le degré de isotropy.

Vous pouvez désactiver le filtrage isotrope en définissant le degré de isotropy à un ; toute valeur supérieure à 1 l’active. Vérifiez l’indicateur MaxAnisotropy dans la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour déterminer la plage de valeurs possible pour le degré d’anisotropie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage de texture](texture-filtering.md)
</dt> </dl>

 

 
