---
title: Structure CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure de \_ plage D3D12 \_ UINT64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Structure CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539923"
---
# <a name="cd3dx12_range_uint64-structure"></a>CD3DX12 \_ plage \_ UINT64 (structure)

Une structure d’assistance pour faciliter l’initialisation d’une structure [**de \_ plage D3D12 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Plage CD3DX12 \_ UINT64 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ plage CD3DX12 \_ UINT64.

</dd> <dt>

**plage CD3DX12 \_ explicite \_ UInt64 (const D3D12 \_ plage \_ UInt64 &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ plage CD3DX12 \_ UInt64, initialisée avec des valeurs copiées à partir d’une structure de [**\_ plage D3D12 \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .

</dd> <dt>

**\_Plage CD3DX12 \_ UINT64 (UInt64 Begin, UInt64 end)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.

</dd> <dt>

**@ const D3D12 \_ plage \_ UINT64& () const**
</dt> <dd>

Conversion implicite en une \_ structure de plage D3D12 \_ UINT64. Étant donné que D3D12 \_ Range \_ UInt64 est le type sous-jacent de la \_ plage CD3DX12 \_ UInt64, l’objet est simplement retourné en tant que référence de plage D3D12 const \_ \_ à lui-même.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Plage D3D12 \_ UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





