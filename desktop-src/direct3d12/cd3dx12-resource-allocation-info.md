---
title: Structure CD3DX12_RESOURCE_ALLOCATION_INFO (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure d’informations d’allocation de ressources D3D12 \_ \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Structure CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535162"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>\_Structure d' \_ informations d’allocation de ressources CD3DX12 \_

Structure d’assistance pour faciliter l’initialisation d’une structure d' [**\_ informations d' \_ allocation \_ de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Informations d' \_ allocation de ressources CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’informations d’allocation de \_ ressources \_ CD3DX12 \_ .

</dd> <dt>

**informations d’allocation de ressources explicites CD3DX12 \_ \_ \_ (const D3D12 \_ resource \_ allocation \_ info& o)**
</dt> <dd>

Crée une nouvelle instance d’informations d' \_ allocation de ressources CD3DX12 \_ \_ , initialisée avec le contenu d’une autre structure d' [**\_ informations d' \_ allocation \_ de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

</dd> <dt>

**\_Informations d' \_ allocation de ressources CD3DX12 \_ (taille UINT64, alignement UInt64)**
</dt> <dd>

Crée une nouvelle instance d’informations d' \_ allocation de ressources CD3DX12 \_ \_ , en initialisant les paramètres suivants :

Taille de UINT64

Alignement de UINT64

</dd> <dt>

**\_const D3D12 Resource \_ ALLOCATION \_ info& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Informations d' \_ allocation de ressources D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





