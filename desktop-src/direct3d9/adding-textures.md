---
description: Pour ajouter des textures, utilisez la nature hiérarchique du format de fichier et ajoutez un objet de données TextureFilename facultatif aux objets de données de matériau.
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: Ajout de textures (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b60ea80702ffc339fe753dec3ad9b72170b03bc8f23598e545e17bc71209d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045237"
---
# <a name="adding-textures-direct3d-9"></a>Ajout de textures (Direct3D 9)

Pour ajouter des textures, utilisez la nature hiérarchique du format de fichier et ajoutez un objet de données [**TextureFilename**](texturefilename.md) facultatif aux objets de données de [**matériau**](material.md) . Les objets **Material** sont maintenant lus comme suit :


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "tex1.ppm"; }
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "win95.ppm"; }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[X fichiers (hérités)](x-files--legacy-.md)
</dt> </dl>

 

 



