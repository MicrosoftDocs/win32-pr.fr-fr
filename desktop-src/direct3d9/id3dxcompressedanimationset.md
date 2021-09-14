---
description: Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé stocké dans un format de données compressé.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interface ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118470"
---
# <a name="id3dxcompressedanimationset-interface"></a>Interface ID3DXCompressedAnimationSet

Une application utilise les méthodes de cette interface pour implémenter un ensemble d’animations d’image clé stocké dans un format de données compressé.

## <a name="members"></a>Membres

L’interface **ID3DXCompressedAnimationSet** hérite de [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXCompressedAnimationSet** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXCompressedAnimationSet** possède ces méthodes.



| Méthode                                                                                  | Description                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetCallbackKeys**](id3dxcompressedanimationset--getcallbackkeys.md)                 | Remplit un tableau avec les données de clé de rappel utilisées pour l’animation d’image clé.<br/>   |
| [**GetCompressedData**](id3dxcompressedanimationset--getcompresseddata.md)             | Obtient la mémoire tampon de données qui stocke les données d’animation d’image clé compressées.<br/> |
| [**GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | Obtient le nombre de clés de rappel dans l’ensemble d’animations.<br/>                |
| [**GetPlaybackType**](id3dxcompressedanimationset--getplaybacktype.md)                 | Obtient le type de la boucle de lecture du jeu d’animations.<br/>                     |
| [**GetSourceTicksPerSecond**](id3dxcompressedanimationset--getsourcetickspersecond.md) | Obtient le nombre de graduations d’image clé d’animation qui se produisent par seconde.<br/>   |



 

## <a name="remarks"></a>Notes

Créer une animation d’image clé au format compressé définie avec [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).

Le type LPD3DXCOMPRESSEDANIMATIONSET est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




