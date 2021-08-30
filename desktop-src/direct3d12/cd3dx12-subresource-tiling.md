---
title: Structure CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une structure de mosaïque de sous- \_ ressources D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Structure CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36a0625b2389783ea4dafa65930e3095329e5bf5e2cfd4c57813e5251f81b88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987979"
---
# <a name="cd3dx12_subresource_tiling-structure"></a>\_Structure de mosaïques de sous-ressources CD3DX12 \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ mosaïque**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) de sous-ressources D3D12.

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Mosaïque de sous-ressources CD3DX12 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une mosaïque de sous- \_ ressources CD3DX12 \_ .

</dd> <dt>

**mosaïque explicite des \_ sous-ressources CD3DX12 \_ (const D3D12 Resource \_ \_ juxtaposition &o)**
</dt> <dd>

Crée une nouvelle instance d’une mosaïque de sous- \_ ressources CD3DX12 \_ , initialisée avec le contenu d’une autre structure de mosaïque de sous- [**\_ ressources \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .

</dd> <dt>

**\_ \_ Mosaïque de sous-ressources CD3DX12 (uint WIDTHINTILES, UInt16 HEIGHTINTILES, UInt16 DEPTHINTILES, uint startTileIndexInOverallResource)**
</dt> <dd>

Crée une nouvelle instance d’une mosaïque de sous- \_ ressources CD3DX12 \_ , en initialisant les paramètres suivants :

UINT widthInTiles

UINT16 heightInTiles

UINT16 depthInTiles

UINT startTileIndexInOverallResource

</dd> <dt>

**\_const D3D12 Resource \_ juxtaposition& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Mosaïque de sous- \_ ressources D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





