---
title: Structure CD3DX12_DEPTH_STENCIL_DESC (D3dx12. h)
description: Une structure d’assistance pour permettre l’initialisation facile d’une \_ structure DESC du stencil de profondeur D3D12 \_ \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Structure CD3DX12_DEPTH_STENCIL_DESC
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fdbd7184ad6fc432beb5ba8e9585c2e9a93486acc604f875ff3a70f72e8ec04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531105"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>\_ \_ Structure DESC du stencil de profondeur CD3DX12 \_

Une structure d’assistance pour permettre l’initialisation facile d’une [**structure \_ \_ \_ desc du stencil de profondeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Description du \_ stencil de profondeur CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ Description du stencil de profondeur D3DX12 \_ \_ .

</dd> <dt>

**DESC du stencil de profondeur CD3DX12 explicite \_ \_ \_ (const D3D12 \_ profondeur du \_ stencil \_& o)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du stencil de profondeur D3DX12 \_ \_ , initialisée avec le contenu d’une autre structure DESC du [**\_ stencil de profondeur \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

</dd> <dt>

**DESC du \_ stencil de profondeur CD3DX12 explicite \_ \_ (CD3DX12 \_ par défaut)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du stencil de profondeur D3DX12 \_ \_ , initialisée avec les paramètres par défaut.

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

**Description du \_ \_ stencil de profondeur de CD3DX12 explicite \_ desc (bool depthEnable, D3D12 de \_ profondeur d' \_ écriture \_ depthWriteMask, D3D12 de \_ comparaison depthFunc \_ , bool STENCILENABLE, UInt8 StencilReadMask, UINT8 stencilWriteMask, D3D12 stencil op frontStencilFailOp, D3D12 stencil op frontStencilDepthFailOp, D3D12 stencil op frontStencilPassOp, D3D12 \_ \_ \_ \_ \_ \_ \_ comparaison \_ Func frontStencilFunc, D3D12 \_ stencil op backStencilFailOp, D3D12 stencil op backStencilDepthFailOp, D3D12 \_ \_ \_ \_ stencil op backStencilPassOp, D3D12 \_ \_ comparaison \_ Func backStencilFunc)**
</dt> <dd>

Crée une nouvelle instance d’une \_ Description du stencil de profondeur D3DX12 \_ \_ , en initialisant les paramètres suivants :

BOOL depthEnable

[**D3D12 \_ \_ \_ Masque d’écriture de profondeur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ Fonction \_ de comparaison**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

BOOL stencilEnable

UINT8 stencilReadMask

UINT8 stencilWriteMask

[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp

[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp

[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp

[**D3D12 \_ Fonction \_ de comparaison**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp

[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp

[**D3D12 \_ STENCIL \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp

[**D3D12 \_ Fonction \_ de comparaison**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~ CD3DX12 \_ du \_ stencil \_ de profondeur ()**
</dt> <dd>

Détruit une instance d’une description du \_ stencil de profondeur CD3DX12 \_ \_ .

</dd> <dt>

**const D3D12- \_ \_ Description du stencil de profondeur \_& () const**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Description du \_ stencil de profondeur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





