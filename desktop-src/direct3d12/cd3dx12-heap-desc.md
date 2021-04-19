---
title: Structure CD3DX12_HEAP_DESC (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une \_ structure DESC du tas D3D12 \_ .
ms.assetid: 38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6
keywords:
- Structure CD3DX12_HEAP_DESC
topic_type:
- apiref
api_name:
- CD3DX12_HEAP_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5b2537d2571355f26c46f03aed3489fb2b6069
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539864"
---
# <a name="cd3dx12_heap_desc-structure"></a>\_Structure DESC du tas CD3DX12 \_

Structure d’assistance pour permettre l’initialisation facile d’une structure [**\_ \_ desc du tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_HEAP_DESC  : public D3D12_HEAP_DESC{
   CD3DX12_HEAP_DESC();
   explicit CD3DX12_HEAP_DESC(const D3D12_HEAP_DESC &o);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_PROPERTIES properties, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_HEAP_TYPE type, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(UINT64 size, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, UINT64 alignment = 0, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_PROPERTIES properties, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_HEAP_TYPE type, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   CD3DX12_HEAP_DESC(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_CPU_PAGE_PROPERTY cpuPageProperty, D3D12_MEMORY_POOL memoryPoolPreference, D3D12_HEAP_FLAGS flags = D3D12_HEAP_FLAG_NONE);
   operator const D3D12_HEAP_DESC&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ \_ , description du tas ()**
</dt> <dd>

Crée une nouvelle instance, non initialisée, d’une \_ Description du tas CD3DX12 \_ .

</dd> <dt>

**DESC du \_ tas CD3DX12 explicite \_ (const D3D12 \_ segment \_ desc &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ desc du tas D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc) .

</dd> <dt>

**\_Description du tas CD3DX12 \_ (taille de UInt64, propriétés des propriétés du \_ tas D3D12 \_ , alignement de UInt64 = 0, indicateurs de \_ tas D3D12 \_ indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :

Taille de UINT64

[**D3D12 \_ Propriétés des \_ Propriétés du tas**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

possibilité -Alignement de UINT64 = 0

possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun

</dd> <dt>

**\_Description du tas CD3DX12 (taille de type de segment de mémoire \_ , type de \_ tas D3D12 \_ , alignement de UInt64 = 0, indicateurs de \_ tas D3D12 \_ indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :

Taille de UINT64

[**D3D12 \_ Type \_ de segment de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

possibilité -Alignement de UINT64 = 0

possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun

</dd> <dt>

**CD3DX12 \_ Heap \_ desc (taille de UINT64, \_ propriété de page D3D12 CPU \_ \_ cpuPageProperty, D3D12 \_ pool de mémoire \_ memoryPoolPreference, UInt64 Alignment = 0, D3D12 \_ segment \_ Flags Flags = D3D12 \_ indicateur de tas \_ \_ None)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :

Taille de UINT64

[**D3D12 \_ \_ \_ Propriété de page**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) de l’UC cpuPageProperty

[**D3D12 \_ \_Pool de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

possibilité -Alignement de UINT64 = 0

possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun

</dd> <dt>

**CD3DX12 \_ segment \_ desc (CONSt D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, propriétés \_ Propriétés du tas D3D12 \_ , D3D12 \_ segments \_ indicateurs indicateurs = D3D12, \_ indicateur de tas \_ \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :

[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Propriétés des \_ Propriétés du tas**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties)

possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun

</dd> <dt>

**CD3DX12 \_ segment \_ desc (CONSt D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 type \_ \_ de tas, D3D12 \_ segment \_ Flags Flags = D3D12 \_ Heap \_ drapeau \_ None)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :

[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ Type \_ de segment de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)

possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun

</dd> <dt>

**CD3DX12 \_ Heap \_ desc (CONSt D3D12 \_ Resource \_ allocation \_ info& resAllocInfo, D3D12 \_ CPU \_ page \_ Property cpuPageProperty, \_ D3D12 \_ pool Memory memoryPoolPreference, D3D12 \_ Heap \_ Flags Flags = D3D12 \_ Heap \_ drapeau \_ None)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du tas CD3DX12 \_ , en initialisant les paramètres suivants :

[**D3D12 \_ \_ \_ Informations d’allocation de ressources**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

[**D3D12 \_ \_ \_ Propriété de page**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cpu_page_property) de l’UC cpuPageProperty

[**D3D12 \_ \_Pool de mémoire**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool) memoryPoolPreference

possibilité [**D3D12 \_ Indicateurs \_ de tas**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags) indicateurs = \_ indicateur de tas D3D12 \_ \_ aucun

</dd> <dt>

**const D3D12 \_ \_ , description du tas& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de \_ structure DESC du tas CD3DX12 \_ .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Description du tas D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





