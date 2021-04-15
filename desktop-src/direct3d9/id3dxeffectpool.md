---
description: Les applications utilisent l’interface ID3DXEffectPool pour identifier les paramètres qui vont être partagés entre les effets. Consultez partage de paramètres dans le clonage et le partage (Direct3D 9). Cette interface n’a pas de méthode.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interface ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394071"
---
# <a name="id3dxeffectpool-interface"></a>Interface ID3DXEffectPool

Les applications utilisent l’interface **ID3DXEffectPool** pour identifier les paramètres qui vont être partagés entre les effets. Consultez partage de paramètres dans le [clonage et le partage (Direct3D 9)](cloning-and-sharing.md). Cette interface n’a pas de méthode.

## <a name="members"></a>Membres

L’interface **ID3DXEffectPool** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.

## <a name="remarks"></a>Notes

L’interface ID3DXEffectPool est obtenue en appelant [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

Le type LPD3DXEFFECTPOOL est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces d’effet](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
