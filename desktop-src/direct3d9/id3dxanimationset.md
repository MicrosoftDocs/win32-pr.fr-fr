---
description: Cette interface encapsule les fonctionnalités minimales requises d’une animation définie par un contrôleur d’animation.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interface ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211945"
---
# <a name="id3dxanimationset-interface"></a>Interface ID3DXAnimationSet

Cette interface encapsule les fonctionnalités minimales requises d’une animation définie par un contrôleur d’animation. Les utilisateurs expérimentés peuvent souhaiter implémenter cette interface eux-mêmes pour répondre à leurs besoins spécifiques. pour la plupart des utilisateurs, toutefois, les interfaces [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) et [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) dérivées devraient suffire.

## <a name="members"></a>Membres

L’interface **ID3DXAnimationSet** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationSet** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXAnimationSet** possède ces méthodes.



| Méthode                                                                        | Description                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetAnimationIndexByName**](id3dxanimationset--getanimationindexbyname.md) | Obtient l’index d’une animation, en fonction de son nom.<br/>                        |
| [**GetAnimationNameByIndex**](id3dxanimationset--getanimationnamebyindex.md) | Obtient le nom d’une animation, en fonction de son index.<br/>                        |
| [**GetCallback**](id3dxanimationset--getcallback.md)                         | Obtient des informations sur un rappel spécifique dans l’ensemble d’animations.<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | Obtient le nom du jeu d’animations.<br/>                                           |
| [**GetNumAnimations**](id3dxanimationset--getnumanimations.md)               | Obtient le nombre d’animations dans l’ensemble d’animations.<br/>                    |
| [**GetPeriod**](id3dxanimationset--getperiod.md)                             | Obtient la période de l’animation définie.<br/>                                  |
| [**GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)         | Retourne la position de l’heure dans la plage locale d’un ensemble d’animations.<br/>      |
| [**GetSRT**](id3dxanimationset--getsrt.md)                                   | Obtient les valeurs de mise à l’échelle, de rotation et de translation de l’ensemble d’animations.<br/> |



 

## <a name="remarks"></a>Notes

Un jeu d’animations se compose d’animations pour de nombreux nœuds pour la même animation.

Le type LPD3DXANIMATIONSET est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
