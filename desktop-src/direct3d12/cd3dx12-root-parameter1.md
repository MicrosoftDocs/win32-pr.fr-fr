---
title: Structure CD3DX12_ROOT_PARAMETER1 (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ structure de \_ PARAMÈTRE1 racine D3D12.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- Structure CD3DX12_ROOT_PARAMETER1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517029"
---
# <a name="cd3dx12_root_parameter1-structure"></a>CD3DX12 \_ - \_ structure de paramètre1 racine

Une structure d’assistance pour permettre l’initialisation facile d’une structure de [**\_ \_ paramètre1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ racine \_ paramètre1 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ paramètre1 racine CD3DX12 \_ .

</dd> <dt>

**CD3DX12 \_ racine explicite \_ paramètre1 (const D3D12 \_ racine \_ paramètre1 &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ paramètre1 racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure [**\_ \_ paramètre1 racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) .

</dd> <dt>

**static Inline InitAsDescriptorTable (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint numDescriptorRanges, CONSt D3D12 \_ descripteur \_ RANGE1 \* pDescriptorRanges, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam

UINT numDescriptorRanges

const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsConstants (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsConstantBufferView (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine Flags \_ = D3D12 \_ indicateur de \_ descripteur racine \_ \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsShaderResourceView (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine Flags \_ = D3D12 \_ indicateur de \_ descripteur racine \_ \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsUnorderedAccessView (D3D12 \_ racine \_ paramètre1 &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ \_ descripteurs racine Flags \_ = D3D12 \_ indicateur de \_ descripteur racine \_ \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ &de \_ PARAMÈTRE1 racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) rootParam

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ RANGE1 \* pDescriptorRanges, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numDescriptorRanges

const [**D3D12 \_ descripteur \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT num32BitValues

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12 \_ \_ indicateur de descripteur racine \_ \_ None, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12 \_ \_ indicateur de descripteur racine \_ \_ None, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ \_ descripteur racine Flags \_ = D3D12 \_ \_ indicateur de descripteur racine \_ \_ None, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Indicateur \_ de \_ descripteur racine**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) Flags = \_ indicateur de \_ descripteur racine D3D12 \_ \_ aucun

[**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ racine \_ paramètre1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





