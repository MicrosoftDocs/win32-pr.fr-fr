---
title: Structure CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de taille de zone de vignette D3D12 \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Structure CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cc1b96ae4d7d33101068a1ba08f0314b99950146e91a352ab49fea714376471
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119609"
---
# <a name="cd3dx12_tile_region_size-structure"></a>Structure de taille de la \_ zone de vignette CD3DX12 \_ \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ taille de \_ zone \_ de vignette D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Taille de la zone de vignette CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ taille de zone de vignette CD3DX12 \_ \_ .

</dd> <dt>

**\_ \_ taille de la zone de mosaïque CD3DX12 explicite \_ (taille de la zone de vignette const D3D12 \_ \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ taille de zone de vignette CD3DX12 \_ \_ , initialisée avec le contenu d’une autre structure de taille de [**\_ zone de vignette \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .

</dd> <dt>

**\_ \_ Taille de la zone de vignette CD3DX12 \_ (uint NumTiles, bool useBox, uint Width, UINT16 hauteur, UInt16 depth)**
</dt> <dd>

Crée une nouvelle instance d’une \_ taille de zone de vignette CD3DX12 \_ \_ , en initialisant les paramètres suivants :

UINT numTiles

BOOL useBox

Largeur UINT

Hauteur de UINT16

Profondeur UINT16

</dd> <dt>

**\_ \_ \_& taille de la zone de vignette D3D12 () const de l’opérateur const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Taille de la \_ zone de vignette D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





