---
title: Structure CD3DX12_TILE_SHAPE (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ forme de vignette D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Structure CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915447"
---
# <a name="cd3dx12_tile_shape-structure"></a>Structure de la \_ forme de vignette CD3DX12 \_

Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ forme de vignette D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_ \_ Forme de vignette CD3DX12 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ forme de vignette CD3DX12 \_ .

</dd> <dt>

**\_forme de vignette CD3DX12 explicite \_ (forme de vignette const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ forme de vignette CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ forme de vignette D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .

</dd> <dt>

**\_ \_ Forme de vignette CD3DX12 (uint WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**
</dt> <dd>

Crée une nouvelle instance d’une \_ forme de vignette CD3DX12 \_ , en initialisant les paramètres suivants :

UINT widthInTexels

UINT heightInTexels

UINT depthInTexels

</dd> <dt>

**\_& de forme de vignette const de l’opérateur D3D12 \_ () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Forme de vignette D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





