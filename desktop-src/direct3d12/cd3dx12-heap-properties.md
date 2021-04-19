---
title: Structure CD3DX12_HEAP_PROPERTIES (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ Propriétés de tas D3D12 \_ .
ms.assetid: AC759F25-D643-412D-AA83-3A2C040BE64B
keywords:
- Structure CD3DX12_HEAP_PROPERTIES
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_PROPERTIES
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90cc5f5cee6bf70aad064396589aad8a483f2c50
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520311"
---
# <a name="cd3dx12_heap_properties-structure"></a>Structure des propriétés du \_ tas CD3DX12 \_

Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ Propriétés de tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_HEAP_PROPERTIES  : public D3D12_HEAP_PROPERTIES{
       CD3DX12_HEAP_PROPERTIES();
       explicit CD3DX12_HEAP_PROPERTIES(const D3D12_HEAP_PROPERTIES &o);
       CD3DX12_HEAP_PROPERTIES(D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT creationNodeMask = 1, UINT nodeMask = 1);
       explicit CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE type, UINT creationNodeMask = 1, UINT nodeMask = 1);
       operator const D3D12_HEAP_PROPERTIES&() const;
  bool inline operator==( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
  bool inline operator!=( const D3D12_HEAP_PROPERTIES& l, const D3D12_HEAP_PROPERTIES& r );
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Propriétés du tas CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée des propriétés du tas CD3DX12 \_ \_ .

</dd> <dt>

**Propriétés du tas CD3DX12 explicites \_ \_ (propriétés du tas const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une CD3DX12 \_ de \_ Propriétés de tas, initialisée avec le contenu d’une autre structure de [**\_ \_ Propriétés de tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties) .

</dd> <dt>

**CD3DX12 \_ Heap \_ Properties (D3D12 \_ CPU \_ page \_ Property CpuPageProperty, D3D12 \_ Memory \_ pool MEMORYPOOLPREFERENCE, uint creationNodeMask = 1, uint nodeMask = 1)**
</dt> <dd>

Crée une nouvelle instance d’une CD3DX12 \_ de \_ Propriétés de tas, en initialisant les paramètres suivants :

[**D3D12 \_ \_ \_ Propriété de page**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) de l’UC cpuPageProperty

[**D3D12 \_ \_Pool de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

possibilité UINT creationNodeMask = 1

possibilité UINT nodeMask = 1

</dd> <dt>

**Propriétés du tas CD3DX12 explicites \_ \_ (type \_ de tas D3D12 \_ , uint CREATIONNODEMASK = 1, uint nodeMask = 1)**
</dt> <dd>

Crée une nouvelle instance d’une CD3DX12 \_ de \_ Propriétés de tas, en initialisant les paramètres suivants :

[**D3D12 \_ Type \_ de segment de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

possibilité UINT creationNodeMask = 1

possibilité UINT nodeMask = 1

</dd> <dt>

**D3D12 \_ \_ (), const, propriétés de segment de mémoire& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> <dt>

**Inline, opérateur = = (const D3D12 \_ segment \_ Properties& l, const D3D12 \_ segment \_ Properties& r)**
</dt> <dd>

Teste l’égalité entre les \_ \_ instances de propriétés de tas D3D12 spécifiées, en fonction de l’égalité de tous les champs membres.

</dd> <dt>

**Inline, opérateur ! = (const D3D12 \_ segment \_ Properties& l, const D3D12 \_ segment \_ Properties& r)**
</dt> <dd>

Teste l’inégalité entre les instances de propriétés de tas D3D12 spécifiées \_ \_ . Implémenté par l’inverse de la valeur **Operator = =** .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Propriétés du tas D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





