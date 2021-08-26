---
description: Direct3D gère une liste de huit textures actuelles. Elle fusionne ces textures sur l’ensemble de la primitive qu’elle rend. Seules les textures créées en tant que pointeurs d’interface de texture peuvent être utilisées dans l’ensemble des textures actuelles.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Affectation des textures actuelles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b2a9ac0b61f7a7d0a9b3ee27c7a9b7e6b8cd4d48fda33959462e26ad6958ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069419"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Affectation des textures actuelles (Direct3D 9)

Direct3D gère une liste de huit textures actuelles. Elle fusionne ces textures sur l’ensemble de la primitive qu’elle rend. Seules les textures créées en tant que pointeurs d’interface de texture peuvent être utilisées dans l’ensemble des textures actuelles.

Les applications appellent la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) pour assigner des textures à l’ensemble des textures actuelles. Le premier paramètre doit être un nombre compris entre 0-7 inclus. Transmettez le pointeur d’interface de texture comme deuxième paramètre.

L’exemple de code C++ suivant montre comment une texture peut être assignée à l’ensemble des textures actuelles.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> Les périphériques logiciels ne prennent pas en charge l’affectation d’une texture à plusieurs étapes de texture à la fois.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion de texture](texture-blending.md)
</dt> </dl>

 

 
