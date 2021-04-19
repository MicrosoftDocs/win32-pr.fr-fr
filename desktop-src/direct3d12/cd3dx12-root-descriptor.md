---
title: Structure CD3DX12_ROOT_DESCRIPTOR (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ \_ structure de descripteurs racine D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531578"
---
# <a name="cd3dx12_root_descriptor-structure"></a>\_Structure du \_ descripteur racine CD3DX12

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ descripteurs racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Descripteur racine CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ \_ descripteur racine CD3DX12.

</dd> <dt>

**\_descripteur racine CD3DX12 explicite \_ ( \_ descripteur racine const D3D12 \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ \_ descripteur racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

</dd> <dt>

**\_Descripteur racine CD3DX12 \_ (uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Crée une nouvelle instance d’un \_ \_ descripteur racine CD3DX12, en initialisant les paramètres suivants :

UINT shaderRegister

possibilité UINT registerSpace = 0

</dd> <dt>

**Inline init (UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

possibilité UINT registerSpace = 0

</dd> <dt>

**static Inline init ( \_ \_ descripteur racine D3D12 &table, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Tableau de &du \_ descripteur racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)

UINT shaderRegister

possibilité UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Descripteur racine D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





