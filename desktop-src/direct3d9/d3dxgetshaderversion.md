---
description: Retourne la version du nuanceur du nuanceur compilé.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: D3DXGetShaderVersion, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116222"
---
# <a name="d3dxgetshaderversion-function"></a>D3DXGetShaderVersion fonction)

Retourne la version du nuanceur du nuanceur compilé.

## <a name="syntax"></a>Syntaxe


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFunction* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers le flux de fonction DWORD.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Retourne la version du nuanceur du nuanceur donné, ou zéro si la fonction de nuanceur est **null**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
