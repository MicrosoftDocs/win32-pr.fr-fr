---
title: Structure CD3DX12_ROOT_DESCRIPTOR1 (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ \_ structure DESCRIPTOR1 racine D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Structure CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532482"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>CD3DX12 \_ racine \_ DESCRIPTOR1, structure

Une structure d’assistance pour permettre l’initialisation facile d’une [**structure \_ \_ DESCRIPTOR1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ racine \_ DESCRIPTOR1 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ DESCRIPTOR1 racine CD3DX12 \_ .

</dd> <dt>

**CD3DX12 \_ racine \_ DESCRIPTOR1 explicite (const D3D12 \_ racine \_ DESCRIPTOR1 &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ DESCRIPTOR1 racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ DESCRIPTOR1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

</dd> <dt>

**CD3DX12 \_ root \_ DESCRIPTOR1 (uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12, \_ indicateur de \_ descripteur racine \_ \_ aucun)**
</dt> <dd>

Crée une nouvelle instance d’un \_ DESCRIPTOR1 racine CD3DX12 \_ , en initialisant les paramètres suivants :

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

</dd> <dt>

**Inline init (UINT shaderRegister, UINT registerSpace = 0, D3D12 la \_ racine du \_ descripteur Flags \_ = D3D12 \_ \_ , indicateur de descripteur racine \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

</dd> <dt>

**static Inline init (D3D12 \_ racine \_ DESCRIPTOR1 &table, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine \_ indicateurs Flags = D3D12 \_ \_ indicateur de descripteur racine \_ \_ aucun)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Table &racine \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ racine \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





