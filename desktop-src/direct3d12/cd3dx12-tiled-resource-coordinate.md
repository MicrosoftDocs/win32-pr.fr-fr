---
title: Structure CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ coordonnées de ressource en mosaïque D3D12 \_ \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Structure CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537237"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a>Structure de coordonnées de ressource en \_ mosaïque CD3DX12 \_ \_

Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ coordonnées de \_ ressource \_ en mosaïque D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Coordonnée des ressources en mosaïque CD3DX12 \_ \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ \_ coordonnée de ressource en mosaïque CD3DX12 \_ .

</dd> <dt>

**coordonnée de ressource en mosaïque CD3DX12 explicite \_ \_ \_ ( \_ coordonnée de ressource en mosaïque const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ \_ \_ coordonnée de ressource en mosaïque CD3DX12, initialisée avec le contenu d’une autre structure de [**coordonnées de \_ ressource en mosaïque \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .

</dd> <dt>

**\_Coordonnée de la ressource en mosaïque CD3DX12 \_ \_ (UINT x, UINT y, uint z, sous-ressource uint)**
</dt> <dd>

Crée une nouvelle instance d’une \_ \_ \_ coordonnée de ressource en mosaïque CD3DX12, en initialisant les paramètres suivants :

UINT x

UINT y

UINT z

Sous-ressource UINT

</dd> <dt>

**D3D12 \_ \_ \_ () const, opérateur const, co& ordonnée de ressource en mosaïque () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Coordonnée de ressources en mosaïque D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





