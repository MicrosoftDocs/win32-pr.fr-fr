---
title: Structure CD3DX12_DESCRIPTOR_RANGE1 (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure RANGE1 de descripteur D3D12 \_ .
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- Structure CD3DX12_DESCRIPTOR_RANGE1
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6386d8094d573fba9cd3af44b0148215ee621e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095325"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>\_Structure RANGE1 du descripteur CD3DX12 \_

Structure d’assistance pour faciliter l’initialisation d’une structure [**\_ \_ RANGE1 de descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Descripteur CD3DX12 \_ RANGE1 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ descripteur CD3DX12 \_ RANGE1.

</dd> <dt>

**descripteur CD3DX12 explicite \_ \_ range1 (const D3D12 \_ Descriptor \_ range1 &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ descripteur CD3DX12 \_ range1, initialisée avec le contenu d’une autre structure [**\_ \_ range1 du descripteur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) .

</dd> <dt>

**CD3DX12 descripteur \_ \_ RANGE1 (D3D12 \_ descripteur de \_ \_ type RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ plage du descripteur indicateurs \_ \_ = D3D12 \_ plage de descripteurs \_ \_ \_ aucun, uint offsetInDescriptorsFromTableStart = D3D12 décalage de la \_ plage du descripteur \_ \_ \_**
</dt> <dd>

Crée une nouvelle instance d’un \_ descripteur CD3DX12 \_ RANGE1, en initialisant les paramètres suivants :

[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ Identificateurs de \_ plage \_ de descripteurs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ indicateur de plage de descripteurs D3D12 \_ \_ \_ aucun

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_

</dd> <dt>

**Inline init ( \_ type de plage de descripteur D3D12 \_ \_ RangeType, UINT NumDescriptors, UINT BaseShaderRegister, uint registerSpace = 0, D3D12 \_ plage de descripteur indicateurs \_ \_ = D3D12 \_ plage de descripteurs \_ \_ \_ aucun, uint offsetInDescriptorsFromTableStart = D3D12 ajout de décalage de la \_ plage du descripteur \_ \_ \_ )**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ Identificateurs de \_ plage \_ de descripteurs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ indicateur de plage de descripteurs D3D12 \_ \_ \_ aucun

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_

</dd> <dt>

**static Inline init (D3D12 \_ descripteur \_ RANGE1 &plage, D3D12 \_ descripteur \_ \_ type RANGETYPE, uint NUMDESCRIPTORS, uint baseShaderRegister, uint registerSpace = 0, D3D12 \_ plage du descripteur indicateurs = D3D12 plage du descripteur \_ \_ \_ \_ \_ \_ None, uint offsetInDescriptorsFromTableStart = D3D12 de décalage de la \_ plage du descripteur \_ \_ \_**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ Plage de &\_ RANGE1 du DEscripteur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)

[**D3D12 \_ \_ \_ Type de plage de descripteur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_ Identificateurs de \_ plage \_ de descripteurs**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) = \_ indicateur de plage de descripteurs D3D12 \_ \_ \_ aucun

UINT offsetInDescriptorsFromTableStart = D3D12 \_ descripteur de décalage de la plage de descripteurs \_ \_ \_

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Descripteur D3D12 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





