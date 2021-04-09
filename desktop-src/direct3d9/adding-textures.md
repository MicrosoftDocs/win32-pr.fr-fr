---
description: Pour ajouter des textures, utilisez la nature hiérarchique du format de fichier et ajoutez un objet de données TextureFilename facultatif aux objets de données de matériau.
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: Ajout de textures (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee0090b5990c2093a41efbd15eb998401ce2607
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110275"
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

 

 



