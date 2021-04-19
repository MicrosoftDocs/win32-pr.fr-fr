---
title: Structure CD3DX12_ROOT_DESCRIPTOR_TABLE1 (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation simple d’une \_ \_ structure table1 de descripteur racine D3D12 \_ .
ms.assetid: 82AC1948-92AA-4A4D-B443-717E9BF3046D
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR_TABLE1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3538e5e1e199fdb6f8c7473af4996ccd7b7f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528772"
---
# <a name="cd3dx12_root_descriptor_table1-structure"></a>CD3DX12 \_ \_ structure table1 du descripteur racine \_

Structure d’assistance pour permettre l’initialisation simple d’une structure [**\_ \_ \_ table1 de descripteur racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE1  : public D3D12_ROOT_DESCRIPTOR_TABLE1{
       CD3DX12_ROOT_DESCRIPTOR_TABLE1();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE1(const D3D12_ROOT_DESCRIPTOR_TABLE1 &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE1(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE1 &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* _pDescriptorRanges);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Descripteur racine CD3DX12 \_ \_ table1 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ \_ descripteur racine CD3DX12 \_ table1.

</dd> <dt>

**\_descripteur racine CD3DX12 explicite \_ \_ table1 (const D3D12 \_ racine \_ descripteur \_ table1 &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12 \_ Table1, initialisée avec le contenu d’une autre structure [**\_ \_ \_ table1 de descripteur racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) .

</dd> <dt>

**\_Descripteur racine CD3DX12 \_ \_ table1 (uint numDescriptorRanges, const D3D12 \_ descripteur \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12 \_ Table1, en initialisant les paramètres suivants :

UINT numDescriptorRanges

const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**Inline init (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numDescriptorRanges

const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> <dt>

**static Inline init ( \_ \_ descripteur racine D3D12 \_ table1 &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ description \_ RANGE1 \* \_ pDescriptorRanges)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Descripteur racine \_ table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1) &rootDescriptorTable

UINT numDescriptorRanges

const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Descripteur racine D3D12 \_ \_ table1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





