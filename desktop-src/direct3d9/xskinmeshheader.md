---
description: Ce modèle est instancié par maillage uniquement dans les maillages qui contiennent des informations d’enveloppement exportées. L’objectif de ce modèle est de fournir des informations sur la nature des informations d’habillage qui ont été exportées.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c86127e46809cd1415b191a769b25e09535405e6500e511df6248e6174888d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796853"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Ce modèle est instancié par maillage uniquement dans les maillages qui contiennent des informations d’enveloppement exportées. L’objectif de ce modèle est de fournir des informations sur la nature des informations d’habillage qui ont été exportées.

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

Où :

-   nMaxSkinWeightsPerVertex : nombre maximal de transformations qui affectent un vertex dans la maille.
-   nMaxSkinWeightsPerFace : nombre maximal de transformations uniques qui affectent les trois sommets de n’importe quelle face.
-   nBones : nombre d’os qui affectent des vertex dans ce maillage.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



