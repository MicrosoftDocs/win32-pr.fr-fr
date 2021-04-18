---
description: Compile un nuanceur à partir d’un effet qui contient une ou plusieurs fonctions.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler :: CompileShader, méthode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522604"
---
# <a name="id3dxeffectcompilercompileshader-method"></a>ID3DXEffectCompiler :: CompileShader, méthode

Compile un nuanceur à partir d’un effet qui contient une ou plusieurs fonctions.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFunction* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique de la fonction à compiler. Cette valeur ne doit pas être **null**. Consultez [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pTarget* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers un profil de nuanceur qui détermine le jeu d’instructions du nuanceur. Pour obtenir la liste des profils disponibles, consultez [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) ou [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Options de compilation identifiées par différents indicateurs. Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut. Pour plus d’informations, consultez [indicateurs D3DXSHADER](d3dxshader-flags.md) .

</dd> <dt>

*ppShader* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant le nuanceur compilé. Le nuanceur de compilateur est un tableau de DWORDs. Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppErrorMsgs* \[ out, retval\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Mémoire tampon contenant au moins le premier message d’erreur de compilation qui s’est produit. Cela comprend les erreurs d’effet du compilateur et les erreurs de compilation du langage de haut niveau. Pour plus d’informations sur l’accès à la mémoire tampon, consultez [**ID3DXBuffer**](id3dxbuffer.md).

</dd> <dt>

*ppConstantTable* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***

Retourne une interface [**ID3DXConstantTable**](id3dxconstanttable.md) , qui peut être utilisée pour accéder aux constantes du nuanceur. Cette valeur peut être **null**. Si vous compilez votre application en prenant en charge les adresses de grande taille (autrement dit, si vous utilisez l’option de l’éditeur de liens/LARGEADDRESSAWARE pour gérer les adresses supérieures à 2 Go), vous ne pouvez pas utiliser ce paramètre et devez lui affecter la **valeur null**. Au lieu de cela, vous devez utiliser la fonction [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) pour récupérer la table de nuanceur-constante incorporée dans le nuanceur. Dans cet appel **D3DXGetShaderConstantTableEx** , vous devez passer l' **indicateur \_ LARGEADDRESSAWARE D3DXCONSTTABLE** au paramètre *Flags* pour spécifier l’accès à un espace d’adressage virtuel pouvant atteindre 4 Go.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK.

Si les arguments ne sont pas valides, la méthode retourne D3DERR \_ INVALIDCALL.

Si la méthode échoue, la valeur de retour est E \_ Fail.

## <a name="remarks"></a>Notes

Les cibles peuvent être spécifiées pour les nuanceurs de vertex, les nuanceurs de pixels et les fonctions de remplissage de texture.



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| Cibles de nuanceur de sommets | vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0                               |
| Cibles de nuanceur de pixels  | PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0 |
| Cibles de remplissage de texture  | TX \_ 0, TX \_ 1                                                          |



 

Cette méthode Compile un nuanceur à partir d’une fonction écrite dans un langage de type C. Pour plus d’informations, consultez [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
