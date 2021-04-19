---
title: Structure CD3DX12_ROOT_PARAMETER (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de paramètres racine D3D12 \_ .
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- Structure CD3DX12_ROOT_PARAMETER
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529594"
---
# <a name="cd3dx12_root_parameter-structure"></a>\_Structure de \_ paramètre racine CD3DX12

Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ paramètres racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Paramètre racine CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ paramètre racine CD3DX12 \_ .

</dd> <dt>

**paramètre racine CD3DX12 explicite \_ \_ (paramètre racine const D3D12 \_ \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ paramètre racine CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ paramètres racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) .

</dd> <dt>

**static Inline InitAsDescriptorTable (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint numDescriptorRanges, CONSt D3D12 \_ descripteur \_ Range \* pDescriptorRanges, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT numDescriptorRanges

[**D3D12 \_ \_Plage de DEscripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsConstants (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT num32BitValues

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsConstantBufferView (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsShaderResourceView (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**static Inline InitAsUnorderedAccessView (D3D12 \_ \_ paramètre racine &ROOTPARAM, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Paramètre racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsDescriptorTable (UINT numDescriptorRanges, const D3D12 \_ descripteur \_ Range \* pDescriptorRanges, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT numDescriptorRanges

[**D3D12 \_ \_Plage de DEscripteurs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsConstants (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT num32BitValues

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsConstantBufferView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsShaderResourceView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> <dt>

**Inline InitAsUnorderedAccessView (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ Shader \_ Visibility Visibility = D3D12 \_ Shader \_ Visibility \_ All)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT shaderRegister

possibilité UINT registerSpace = 0

possibilité [**D3D12 \_ Visibilité de la \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) = \_ visibilité du nuanceur D3D12 \_ \_ tout

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Paramètre racine \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





