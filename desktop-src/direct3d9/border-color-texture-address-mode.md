---
description: Le mode d’adresse de texture de couleur de la bordure, identifié par le \_ membre de bordure D3DTADDRESS du type énuméré D3DTEXTUREADDRESS, fait en sorte que Direct3D utilise une couleur arbitraire, appelée couleur de bordure, pour toutes les coordonnées de texture situées en dehors de la plage comprise entre 0,0 et 1,0 inclus.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Mode d’adresse de la texture de couleur de la bordure (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e0685359227f80a847174157117e90116cffe8e61a48e172451a83aa8ec5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496313"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Mode d’adresse de la texture de couleur de la bordure (Direct3D 9)

Le mode d’adresse de texture de couleur de la bordure, identifié par le \_ membre de bordure D3DTADDRESS du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fait en sorte que Direct3D utilise une couleur arbitraire, appelée couleur de bordure, pour toutes les coordonnées de texture situées en dehors de la plage comprise entre 0,0 et 1,0 inclus.

Dans l’illustration suivante, l’application spécifie que la texture doit être appliquée à la primitive à l’aide d’une bordure rouge.

![illustration d’une texture et d’une texture avec bordure rouge](images/border.png)

Les applications définissent la couleur de la bordure en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate). Définissez le premier paramètre pour l’appel à l’identificateur de l’étape de texture souhaitée, le deuxième paramètre à la valeur d’état de l' \_ étape D3DSAMP BORDERCOLOR et le troisième paramètre à la nouvelle couleur de bordure RVBA.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes d’adressage de la texture](texture-addressing-modes.md)
</dt> </dl>

 

 
