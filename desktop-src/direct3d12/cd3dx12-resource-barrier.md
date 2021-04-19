---
title: Structure CD3DX12_RESOURCE_BARRIER (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de barrière de ressources D3D12 \_ .
ms.assetid: 89E0F38C-8802-46E6-9583-95C5D853CD99
keywords:
- Structure CD3DX12_RESOURCE_BARRIER
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_BARRIER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eaa9b19a8bc7dcebba5982313bb362dbcee6157
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528574"
---
# <a name="cd3dx12_resource_barrier-structure"></a>CD3DX12 \_ structure de cloisonnement des ressources \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ barrière de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RESOURCE_BARRIER  : public D3D12_RESOURCE_BARRIER{
                           CD3DX12_RESOURCE_BARRIER();
                           explicit CD3DX12_RESOURCE_BARRIER(const D3D12_RESOURCE_BARRIER &o);
  CD3DX12_RESOURCE_BARRIER static inline Transition(ID3D12Resource* pResource, D3D12_RESOURCE_STATES stateBefore, D3D12_RESOURCE_STATES stateAfter, UINT subresource = D3D12_RESOURCE_BARRIER_ALL_SUBRESOURCES, D3D12_RESOURCE_BARRIER_FLAGS flags = D3D12_RESOURCE_BARRIER_FLAG_NONE);
  CD3DX12_RESOURCE_BARRIER static inline Aliasing(ID3D12Resource* pResourceBefore, ID3D12Resource* pResourceAfter);
  CD3DX12_RESOURCE_BARRIER static inline UAV(ID3D12Resource* pResource);
                           operator const D3D12_RESOURCE_BARRIER&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Barrière des ressources CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ cloisonnement de ressources CD3DX12 \_ .

</dd> <dt>

**\_barrière de ressources CD3DX12 explicite \_ (barrière de ressources const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ barrière de ressources CD3DX12 \_ , initialisée avec le contenu d’un autre [**\_ \_ cloisonnement de ressources D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier).

</dd> <dt>

**Transition statique statique (ID3D12Resource \* présource, D3D12 \_ États des ressources \_ stateBefore, D3D12 des \_ États des ressources \_ stateAfter, uint Resource = D3D12 Resource \_ \_ barrière toutes les sous- \_ \_ ressources, D3D12 \_ indicateurs de barrière des ressources \_ \_ indicateurs = D3D12 \_ indicateur de barrière des ressources \_ \_ \_ aucun)**
</dt> <dd>

Les transitions entre les États des ressources, à l’aide des paramètres suivants :

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Préversion

[**D3D12 \_ \_États des ressources**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateBefore

[**D3D12 \_ \_États des ressources**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) stateAfter

possibilité UINT Resource = D3D12 Resource [ **\_ \_ barrière \_ toutes les \_** sous-ressources](constants.md)

possibilité [**D3D12 \_ Indicateurs \_ de \_ cloisonnement des ressources**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags) indicateurs = \_ indicateur de cloisonnement des ressources D3D12 \_ \_ \_ aucun

</dd> <dt>

**Alias Inline statique (ID3D12Resource \* pResourceBefore, ID3D12Resource \* pResourceAfter)**
</dt> <dd>

Crée des alias pour la ressource avant et après la transition de barrière. Paramètres :

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceBefore

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pResourceAfter

</dd> <dt>

**static Inline UAV ( \* présource ID3D12Resource)**
</dt> <dd>

Crée un mode d’accès non ordonné (UAV) pour la ressource. Paramètres :

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Préversion

</dd> <dt>

**D3D12, const \_ \_ , opérateur de& cloisonnement de ressources () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Barrière des ressources D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_barrier)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





