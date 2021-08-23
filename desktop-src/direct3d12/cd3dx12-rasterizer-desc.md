---
title: Structure CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure D3D12 \_ rastériseur \_ desc.
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Structure CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa95dde87aea8e3c61d0d1fb6de6845f33717f6a46db4df7996a23afd7590b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729429"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>\_Structure CD3DX12 rastériseur \_ desc

Structure d’assistance pour permettre l’initialisation facile d’une structure [**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ rastériseur \_ desc ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un CD3DX12 \_ rastériseur \_ desc.

</dd> <dt>

**CD3DX12 \_ de rastérisation explicite \_ desc (const D3D12 \_ rastériseur \_ desc& o)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ rastériseur \_ desc, initialisée avec le contenu d’une autre structure [**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

</dd> <dt>

**CD3DX12 \_ rastériseur DESC explicite \_ (CD3DX12 \_ par défaut)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ rastériseur \_ desc, initialisé avec les paramètres par défaut.

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**CD3DX12 \_ rastériseur DESC explicite \_ (D3D12 \_ mode de remplissage \_ fillMode, D3D12 \_ mode d’élimination \_ CullMode, bool FrontCounterClockwise, int DepthBias, float DepthBiasClamp, float SlopeScaledDepthBias, BOOL DepthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 \_ mode de pixellisation conservatrice \_ \_ conservativeRaster)**
</dt> <dd>

Crée une nouvelle instance d’un CD3DX12 \_ rastériseur \_ desc, en initialisant les paramètres suivants :

[**D3D12 \_ \_Mode de remplissage**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_ \_Mode d’élimination**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode

BOOL frontCounterClockwise

INT depthBias

DepthBiasClamp FLOAT

SlopeScaledDepthBias FLOAT

BOOL depthClipEnable

BOOL multisampleEnable

BOOL antialiasedLineEnable

UINT forcedSampleCount

[**D3D12 \_ \_ \_ Mode de pixellisation conservateur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~ CD3DX12 \_ rastériseur \_ desc ()**
</dt> <dd>

Détruit une instance d’un CD3DX12 \_ rastériseur \_ desc.

</dd> <dt>

**const D3D12, opérateur const \_ \_ descr DESC& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D3D12 \_ rastériseur \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





