---
title: Structure CD3DX12_DEPTH_STENCIL_DESC1 (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une \_ structure DESC1 de stencil de profondeur D3D12 \_ \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Structure CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095330"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>\_ \_ Structure DESC1 du stencil de profondeur CD3DX12 \_

Une structure d’assistance pour faciliter l’initialisation d’une structure [**\_ DESC1 de \_ stencil \_ de profondeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ de profondeur du \_ stencil \_ DESC1 ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1.

</dd> <dt>

**\_stencil de profondeur CD3DX12 explicite \_ \_ DESC1 (const D3D12 de \_ profondeur du \_ stencil \_ DESC1& o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs copiées à partir d’une structure DESC1 de [**\_ stencil de profondeur \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

</dd> <dt>

**\_stencil de profondeur CD3DX12 explicite \_ \_ DESC1 (const \_ D3D12 \_ desc du stencil \_& o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs copiées à partir d’une structure DESC du [**\_ stencil de profondeur \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

et le membre **DepthBoundsTestEnable** supplémentaire défini sur **false**.

</dd> <dt>

**CD3DX12 \_ de profondeur du \_ stencil explicite \_ DESC1 (CD3DX12 \_ par défaut)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec l’État par défaut prescrit par D3DX12 :

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

**CD3DX12 de \_ profondeur \_ explicite \_ DESC1 (bool depthEnable, D3D12 \_ masque d’écriture de profondeur \_ \_ depthWriteMask, D3D12 de comparaison DepthFunc, \_ \_ bool STENCILENABLE, UInt8 StencilReadMask, UINT8 stencilWriteMask, D3D12 stencil op frontStencilFailOp, D3D12 stencil op frontStencilDepthFailOp, D3D12 stencil op FRONTSTENCILPASSOP, D3D12 de comparaison Func frontStencilFunc, D3D12 stencil op backStencilFailOp, D3D12 stencil op backStencilDepthFailOp, D3D12 stencil op BACKSTENCILPASSOP, D3D12 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ de comparaison Func backStencilFunc, bool depthBoundsTestEnable)**
</dt> <dd>

Crée une nouvelle instance d’un \_ stencil de profondeur CD3DX12 \_ \_ DESC1, initialisée avec les valeurs passées dans la liste de paramètres.

</dd> <dt>

**~ CD3DX12 \_ de profondeur du \_ stencil \_ DESC1 ()**
</dt> <dd>

Détruit une instance d’un stencil de \_ profondeur \_ D3DX12 \_ DESC1.

</dd> <dt>

**@ const D3D12 \_ de profondeur du \_ STENCIL \_ DESC1& () const**
</dt> <dd>

Conversion implicite en \_ structure DESC1 du stencil de profondeur D3D12 \_ \_ . Étant donné \_ que \_ le stencil de profondeur D3D12 \_ DESC1 est le type sous-jacent du \_ stencil de profondeur CD3DX12 \_ \_ DESC1, l’objet est simplement retourné en tant que référence de stencil de profondeur D3D12 const \_ \_ \_ à lui-même.

</dd> <dt>

**const D3D12- \_ \_ Description du stencil \_ de profondeur () const**
</dt> <dd>

Conversion implicite en \_ valeur de \_ structure DESC du stencil de profondeur D3D12 \_ . Étant donné \_ que \_ \_ la description du stencil de profondeur D3D12 n’est pas le type sous-jacent du \_ stencil de profondeur CD3DX12 \_ \_ DESC1, une nouvelle \_ instance DESC du stencil de profondeur D3D12 \_ \_ est créée et retournée par valeur. Notez que la \_ Description du stencil D3D12 Depth \_ \_ n’inclut pas le membre **DepthBoundsTestEnable** . cette valeur est donc perdue lors de la conversion.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**D3D12 \_ du \_ stencil de profondeur \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**\_Description du \_ stencil de profondeur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





