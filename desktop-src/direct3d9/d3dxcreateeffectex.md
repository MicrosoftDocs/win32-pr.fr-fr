---
description: Crée un effet à partir d’une description d’effet ASCII ou binaire. Cette fonction est une version étendue de D3DXCreateEffect qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: D3DXCreateEffectEx, fonction (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 19321dde9f44a2262ee3875d40bd5822e65eff9b84d1fc01656993ea584a8dc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988649"
---
# <a name="d3dxcreateeffectex-function"></a>D3DXCreateEffectEx fonction)

Crée un effet à partir d’une description d’effet ASCII ou binaire. Cette fonction est une version étendue de [**D3DXCreateEffect**](d3dxcreateeffect.md) qui permet à une application de contrôler les paramètres qui sont ignorés par le système d’effets.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers l’appareil qui va créer l’effet. Consultez [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*pSrcData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon qui contient une description d’effet.

</dd> <dt>

*SrcDataLen* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Longueur des données d’effet, en octets.

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

*pSkipConstants* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne de paramètres d’effet qui sera ignorée par le système d’effet. La chaîne doit se terminer par une **valeur null** et doit contenir le nom de chaque constante gérée par l’application, séparées par un point-virgule.

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Si *pSrcData* contient un effet de texte, Flags peut être une combinaison d' [indicateurs D3DXSHADER](d3dxshader-flags.md) et d’indicateurs [D3DXFX](d3dxfx.md) ; Sinon, *pSrcData* contient un effet binaire et les seuls indicateurs honorés sont des indicateurs D3DXFX. Le compilateur HLSL Direct3D 10 est désormais la valeur par défaut. Pour plus d’informations [, consultez outil de compilateur Effect](../direct3dtools/fxc.md) .

</dd> <dt>

*pPool* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Pointeur vers un objet [**ID3DXEffectPool**](id3dxeffectpool.md) à utiliser pour les paramètres partagés. Si cette valeur est **null**, aucun paramètre n’est partagé.

</dd> <dt>

*ppEffect* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Retourne un pointeur vers une interface [**ID3DXEffect**](id3dxeffect.md) .

</dd> <dt>

*ppCompilationErrors* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne une mémoire tampon qui contient une liste d’erreurs de compilation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Cette fonction est une version étendue de [**D3DXCreateEffect**](d3dxcreateeffect.md) qui permet à une application de spécifier les constantes d’effet qui seront gérées par l’application. Une constante gérée par l’application est ignorée par le système d’effets. Autrement dit, l’application est responsable de l’initialisation de la constante, ainsi que de l’enregistrement et de la restauration de son état chaque fois que nécessaire.

Cette fonction vérifie chaque constante dans pSkipConstants pour voir ce qui suit :

-   Elle est liée à un registre de constantes.
-   Il est utilisé uniquement dans le code de nuanceur HLSL.

Si une constante est nommée dans la chaîne qui n’est pas présente dans l’effet, elle est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Effect](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectFromFileEx**](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
