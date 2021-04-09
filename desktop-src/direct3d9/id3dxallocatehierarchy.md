---
description: Cette interface est implémentée par l’application pour allouer ou libérer des objets conteneurs de frame et de maillage. Les méthodes de ce sont appelées lors du chargement et de la destruction des hiérarchies de frame.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interface ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043174"
---
# <a name="id3dxallocatehierarchy-interface"></a>Interface ID3DXAllocateHierarchy

Cette interface est implémentée par l’application pour allouer ou libérer des objets conteneurs de frame et de maillage. Les méthodes de ce sont appelées lors du chargement et de la destruction des hiérarchies de frame.

## <a name="members"></a>Membres

L’interface **ID3DXAllocateHierarchy** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAllocateHierarchy** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXAllocateHierarchy** possède ces méthodes.



| Méthode                                                                       | Description                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CreateFrame**](id3dxallocatehierarchy--createframe.md)                   | Demande l’allocation d’un objet Frame.<br/>            |
| [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md)   | Demande l’allocation d’un objet conteneur de maillage.<br/>   |
| [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)                 | Demande la désallocation d’un objet Frame.<br/>          |
| [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) | Demande la désallocation d’un objet conteneur de maillage.<br/> |



 

## <a name="remarks"></a>Notes

Le type LPD3DXALLOCATEHIERARCHY est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
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

 

 
