---
title: Structure CD3DX12_ROOT_DESCRIPTOR_TABLE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de table de \_ descripteurs racine D3D12 \_ .
ms.assetid: 154B4C50-4E94-471C-A44E-F120A84F007C
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR_TABLE
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR_TABLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f675624526a959e6cf92172383b12590c36fc408
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520309"
---
# <a name="cd3dx12_root_descriptor_table-structure"></a>\_Structure de \_ table de descripteurs racine CD3DX12 \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ \_ table de descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR_TABLE  : public D3D12_ROOT_DESCRIPTOR_TABLE{
       CD3DX12_ROOT_DESCRIPTOR_TABLE();
       explicit CD3DX12_ROOT_DESCRIPTOR_TABLE(const D3D12_ROOT_DESCRIPTOR_TABLE &o);
       CD3DX12_ROOT_DESCRIPTOR_TABLE(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void inline Init(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
  void static inline Init(D3D12_ROOT_DESCRIPTOR_TABLE &rootDescriptorTable, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* _pDescriptorRanges);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Tableau de descripteurs racine CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ \_ table de descripteurs racine CD3DX12 \_ .

</dd> <dt>

**\_ \_ table de descripteurs racine CD3DX12 explicite \_ ( \_ table de descripteur racine const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ table de \_ descripteurs racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ \_ table de descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) .

</dd> <dt>

**CD3DX12 \_ \_ table descripteur racine \_ (uint numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* \_ pDescriptorRanges)**
</dt> <dd>

Crée une nouvelle instance d’une \_ table de \_ descripteurs racine CD3DX12 \_ , en initialisant les paramètres suivants :

UINT numDescriptorRanges

[**D3D12 \_ \_Plage de descripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**Inline init (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* \_ pDescriptorRanges)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numDescriptorRanges

[**D3D12 \_ \_Plage de descripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> <dt>

**static Inline init ( \_ \_ table descripteur racine D3D12 \_ &RootDescriptorTable, uint numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* \_ pDescriptorRanges)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_ \_ Tableau du descripteur racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table) &rootDescriptorTable

UINT numDescriptorRanges

[**D3D12 \_ \_Plage de descripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* \_ pDescriptorRanges

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Tableau de \_ descripteurs racine D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





