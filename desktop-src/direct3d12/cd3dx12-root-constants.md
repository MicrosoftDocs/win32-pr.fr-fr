---
title: Structure CD3DX12_ROOT_CONSTANTS (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation facile d’une structure de \_ \_ constantes racine D3D12.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Structure CD3DX12_ROOT_CONSTANTS
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918504"
---
# <a name="cd3dx12_root_constants-structure"></a>CD3DX12 \_ , \_ structure de constantes racine

Structure d’assistance pour permettre l’initialisation facile d’une structure [**de \_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Membres

<dl> <dt>

**CD3DX12 \_ \_ , constantes racine ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’une \_ constante racine CD3DX12 \_ .

</dd> <dt>

**\_constantes racine CD3DX12 explicites \_ ( \_ constantes racine const D3D12 \_ &o)**
</dt> <dd>

Crée une nouvelle instance de \_ \_ constantes racine CD3DX12, initialisée avec le contenu d’une autre structure de [**\_ \_ constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

</dd> <dt>

**CD3DX12 \_ , \_ constantes racine (uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Crée une nouvelle instance de \_ \_ constantes racine CD3DX12, en initialisant les paramètres suivants :

UINT num32BitValues

UINT shaderRegister

possibilité UINT registerSpace = 0

</dd> <dt>

**Inline init (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

UINT num32BitValues

UINT shaderRegister

possibilité UINT registerSpace = 0

</dd> <dt>

**static Inline init ( \_ \_ constantes racine D3D12 &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Spécifie une fonction qui initialise les paramètres suivants :

[**D3D12 \_ \_Constantes racine**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants

UINT num32BitValues

UINT shaderRegister

possibilité UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ Constantes racine D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





