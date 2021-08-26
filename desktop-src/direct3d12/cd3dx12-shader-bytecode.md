---
title: Structure CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Une structure d’assistance pour faciliter l’initialisation d’une structure de \_ bytecode de nuanceur D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Structure CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd984268a8dcd083b2d42573c6fa0028d2b73e7a3daacecd3fefe41c68150db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988368"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>CD3DX12 \_ structure de bytecode du nuanceur \_

Une structure d’assistance pour faciliter l’initialisation d’une structure [**de \_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

## <a name="syntax"></a>Syntaxe


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Bytecode du nuanceur CD3DX12 \_ ()**
</dt> <dd>

Crée une nouvelle instance non initialisée d’un \_ bytecode de nuanceur CD3DX12 \_ .

</dd> <dt>

**\_bytecode de nuanceur CD3DX12 explicite \_ ( \_ Pseudo-code du nuanceur const D3D12 \_ &o)**
</dt> <dd>

Crée une nouvelle instance d’un \_ bytecode de nuanceur CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ bytecode de nuanceur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**\_Bytecode du nuanceur CD3DX12 \_ (ID3DBlob \* pShaderBlob)**
</dt> <dd>

Crée une nouvelle instance d’un \_ bytecode de nuanceur CD3DX12 \_ , en initialisant les paramètres suivants :

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**\_ \_ Bytecode de nuanceur CD3DX12 (const void \* \_ PShaderBytecode, size \_ T bytecodeLength)**
</dt> <dd>

Crée une nouvelle instance d’un \_ bytecode de nuanceur CD3DX12 \_ , en initialisant les paramètres suivants :

void \* \_ pShaderBytecode

TAILLE \_ T bytecodeLength

</dd> <dt>

**D3D12 \_ \_ () const, opérateur const,& bytecode de nuanceur**
</dt> <dd>

Définit le & opérateur de passage par référence pour le type de structure parent.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Bytecode de nuanceur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Structures d’assistance pour D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

