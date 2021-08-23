---
description: Définit les coordonnées de texture d’un maillage.
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: MeshTextureCoords
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5854d4a3a7f602d560845874c3af6339ff1d5e9ebbae0f79f35f4298591ee06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628429"
---
# <a name="meshtexturecoords"></a>MeshTextureCoords

Définit les coordonnées de texture d’un maillage.

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

Où :

-   nTextureCoords : nombre de coordonnées de texture.
-   Tableau Coords2d textureCoords \[ nTextureCoords \] -tableau de coordonnées de texture 2D. Consultez [**Coords2d**](coords2d.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



