---
title: Structure CD3DX12_DESCRIPTOR_RANGE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de plage de descripteur D3D12 \_ .
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- Structure CD3DX12_DESCRIPTOR_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 641afe973c89d66257a8fc7b46defe2e77d8a8667094448ef58ab4beb2839b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989939"
---
# <a name="cd3dx12_descriptor_range-structure"></a>Structure de la \_ plage du descripteur CD3DX12 \_

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ plage de descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Plage du descripteur CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ plage de descripteurs D3DX12 \_ .

</dd> <dt>

**plage du \_ descripteur CD3DX12 explicite \_ ( \_ plage du descripteur const D3D12 \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ plage de descripteurs D3DX12 \_ , initialisée avec le contenu d’une autre structure de la [**\_ \_ plage du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) .

</dd> <dt>

**\_Plage du descripteur CD3DX12 \_ ( \_ type de plage de descripteur D3D12 \_ \_ RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 \_ \_ Append décalage de la plage du descripteur \_ \_ )**
</dt> <dd>

Crée une nouvelle instance d’une \_ plage de descripteurs D3DX12 \_ , en initialisant les paramètres suivants :

[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_

</dd> <dt>

**Inline init ( \_ type de plage de descripteur D3D12 \_ \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 de décalage de la \_ plage du descripteur \_ \_ \_ append)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_

</dd> <dt>

**static Inline init ( \_ plage du descripteur D3D12 \_ &Range, D3D12 \_ descripteur \_ \_ type RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, UINT RegisterSpace = 0, uint offsetInDescriptorsFromTableStart = D3D12 décalage de la \_ plage du descripteur \_ \_ \_ append)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Plage \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) de &de la plage de descripteurs

[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Plage du descripteur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





