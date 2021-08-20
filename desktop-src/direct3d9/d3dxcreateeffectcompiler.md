---
description: 'Fonction D3DXCreateEffectCompiler : crée un compilateur d’effet à partir d’une description d’effet ASCII.'
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: D3DXCreateEffectCompiler, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8ad26017bdc3095aaa23bd17f2b90f76b805502781c08ba393047a90714ad50c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096564"
---
# <a name="d3dxcreateeffectcompiler-function"></a>D3DXCreateEffectCompiler fonction)

Crée un effet de compilateur à partir d’une description d’effet ASCII.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSrcData* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon qui contient une description d’effet.

</dd> <dt>

*SrcDataLen* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Longueur, en octets, des données d’effet.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMACRO**](d3dxmacro.md) \***

Tableau de structures [**D3DXMACRO**](d3dxmacro.md) se terminant par un caractère **null** facultatif qui décrivent les définitions de préprocesseur. Cette valeur peut être **null**.

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include. Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Options de compilation identifiées par différents indicateurs (consultez [D3DXSHADER Flags](d3dxshader-flags.md)). Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut. Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .

</dd> <dt>

*ppEffectCompiler* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***

Adresse d’un pointeur vers une interface [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenant le compilateur d’effet.

</dd> <dt>

*ppParseErrors* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) contenant tous les messages d’erreur qui se sont produits pendant la compilation. Ce paramètre peut avoir la valeur **null** pour ignorer les messages d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Effect](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
