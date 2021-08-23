---
title: Structure CD3DX12_RECT (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ structure D3D12 Rect.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Structure CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff9df3a4c7df2f30e9614b16d5f8b89ea1b6f0279a1566b206cabef7260fb28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729339"
---
# <a name="cd3dx12_rect-structure"></a>CD3DX12 \_ Rect, structure

Une structure d’assistance pour permettre l’initialisation facile d’une structure [**D3D12 \_ Rect**](d3d12-rect.md) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ Rect ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un CD3DX12 \_ Rect.

</dd> <dt>

**CD3DX12 \_ rectangulaire (const D3D12 \_ Rect& o) explicite**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ Rect, initialisée avec le contenu d’une autre structure [**D3D12 \_ Rect**](d3d12-rect.md) .

</dd> <dt>

**CD3DX12 explicite \_ Rect (long gauche, long haut, long Right, long Bottom)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ Rect, en initialisant les paramètres suivants :

LONGUE gauche

LONG haut

LONG droit

LONG bas

</dd> <dt>

**~ CD3DX12 \_ Rect ()**
</dt> <dd>

Détruit une instance d’un CD3DX12 \_ Rect.

</dd> <dt>

**const, opérateur D3D12 \_ RECT& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ Rect**](d3d12-rect.md)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





