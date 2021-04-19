---
title: Structure CD3DX12_CLEAR_VALUE (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ valeur Clear D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Structure CD3DX12_CLEAR_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543767"
---
# <a name="cd3dx12_clear_value-structure"></a>CD3DX12 \_ \_ structure de valeur Clear

Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ valeur Clear D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ effacer la \_ valeur ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ valeur Clear CD3DX12 \_ .

</dd> <dt>

**\_valeur Clear CD3DX12 explicite \_ (const D3D12 \_ effacer la \_ valeur &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ valeur Clear CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ valeur Clear D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

</dd> <dt>

**\_Valeur Clear CD3DX12 \_ (format de \_ format dxgi, const float couleur \[ 4 \] )**
</dt> <dd>

Crée une nouvelle instance d’une \_ valeur Clear CD3DX12 \_ , en initialisant les paramètres suivants :

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

Couleur FLOTTante \[ 4 \]

</dd> <dt>

**\_Valeur Clear CD3DX12 \_ ( \_ format de format dxgi, profondeur float, gabarit UINT8)**
</dt> <dd>

Crée une nouvelle instance d’une \_ valeur Clear CD3DX12 \_ , en initialisant les paramètres suivants :

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Format de format

Profondeur FLOAT

Gabarit UINT8

</dd> <dt>

**\_const D3D12 effacer la \_ valeur& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ effacer la \_ valeur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

