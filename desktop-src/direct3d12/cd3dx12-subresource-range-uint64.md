---
title: Structure CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure de sous- \_ ressource D3D12 \_ \_ UINT64.
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Structure CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527090"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a>CD3DX12, plage de sous- \_ ressource \_ UINT64, \_ structure

Une structure d’assistance pour faciliter l’initialisation d’une structure de sous- [**\_ ressource D3D12 \_ \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Plage de sous-ressources CD3DX12 \_ UINT64 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une plage de sous- \_ ressources \_ CD3DX12 \_ UINT64.

</dd> <dt>

**\_plage de sous-ressources CD3DX12 explicite \_ \_ UInt64 (const D3D12, plage de sous- \_ ressources \_ \_ UInt64 &o)**
</dt> <dd>

Crée une nouvelle instance d’une plage de sous- \_ ressources CD3DX12 \_ \_ UInt64, initialisée avec des valeurs copiées à partir d’une structure de sous- [**\_ ressource D3D12 \_ \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .

</dd> <dt>

**\_Plage de sous-ressources CD3DX12 \_ \_ UInt64 (uint Resource, const D3D12 \_ plage \_ UInt64& plage)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.

</dd> <dt>

**CD3DX12 \_ sous-ressource de \_ groupe \_ de ressources UINT64 (uint Resource, UInt64 Begin, UInt64 end)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.

</dd> <dt>

**D3D12, opérateur const \_ \_ , plage \_ de sous-ressources UINT64& () const**
</dt> <dd>

Conversion implicite en une \_ structure UINT64 de la plage de sous-ressources D3D12 \_ \_ . Étant donné que \_ \_ la plage \_ de sous-ressources D3D12 UInt64 est le type sous-jacent de la plage de sous- \_ ressources CD3DX12 \_ \_ UInt64, l’objet est simplement retourné en tant que référence de stencil de profondeur D3D12 const \_ \_ \_ à lui-même.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Plage de sous- \_ ressources D3D12 \_ \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





