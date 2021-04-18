---
title: Structure CD3DX12_BLEND_DESC (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation simple d’une \_ structure D3D12 Blend \_ desc.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Structure CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522575"
---
# <a name="cd3dx12_blend_desc-structure"></a>CD3DX12 \_ Blend, \_ structure DESC

Une structure d’assistance pour permettre l’initialisation simple d’une structure [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ Blend \_ desc ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un CD3DX12 \_ Blend \_ desc.

</dd> <dt>

**explicite CD3DX12 \_ Blend \_ desc (const D3D12 \_ Blend \_ desc& o)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ Blend \_ desc, initialisée avec le contenu d’une autre structure [**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

</dd> <dt>

**Explicit CD3DX12 \_ Blend \_ desc (CD3DX12 \_ par défaut)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ Blend \_ desc, initialisé avec les paramètres par défaut.



| State                                   | Valeur par défaut                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ 0 \] . BlendEnable           | **FALSE**                        |
| RenderTarget \[ 0 \] . LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ 0 \] . SrcBlend              | D3D12 \_ Blend \_ One                |
| RenderTarget \[ 0 \] . DestBlend             | D3D12 \_ Blend \_ zéro               |
| RenderTarget \[ 0 \] . BlendOp               | \_Ajouter D3D12 Blend \_ op \_            |
| RenderTarget \[ 0 \] . SrcBlendAlpha         | D3D12 \_ Blend \_ One                |
| RenderTarget \[ 0 \] . DestBlendAlpha        | D3D12 \_ Blend \_ zéro               |
| RenderTarget \[ 0 \] . BlendOpAlpha          | \_Ajouter D3D12 Blend \_ op \_            |
| RenderTarget \[ 0 \] . LogicOp               | D3D12 \_ logique \_ op \_           |
| RenderTarget \[ 0 \] . RenderTargetWriteMask | \_Activer l’écriture en couleur D3D12 \_ \_ \_ tout |



 

</dd> <dt>

**~ CD3DX12 \_ Blend \_ desc ()**
</dt> <dd>

Détruit une instance d’un CD3DX12 \_ Blend \_ desc.

</dd> <dt>

**const, opérateur D3D12 \_ Blend \_ desc& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ Blend \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





