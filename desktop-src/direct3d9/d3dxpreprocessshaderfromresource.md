---
description: Prétraite une ressource de nuanceur sans effectuer la compilation. Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: D3DXPreprocessShaderFromResource, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322838"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a>D3DXPreprocessShaderFromResource fonction)

Prétraite une ressource de nuanceur sans effectuer la compilation. Cela résout tous les \# définitions et les \# inclusions, en fournissant un nuanceur autonome pour la compilation suivante.

> [!Note]  
> Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcModule* \[ dans\]
</dt> <dd>

Type : **[ **HMODULE**](../winprog/windows-data-types.md)**

Handle du module qui contient la ressource de nuanceur. Si cette valeur est **null**, le module en cours sera utilisé.

</dd> <dt>

*pSrcResource* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne qui représente le nom de la ressource dans le module.

</dd> <dt>

*pDefines* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMACRO**](d3dxmacro.md) \***

Tableau de structures [**D3DXMACRO**](d3dxmacro.md) terminé par un caractère **null** facultatif. Cette valeur peut être **null**.

</dd> <dt>

*pInclude* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Pointeur d’interface facultatif, [**ID3DXInclude**](id3dxinclude.md), à utiliser pour gérer les \# directives include. Si cette valeur est **null**, \# include est respecté lors de la compilation à partir d’un fichier ou provoque une erreur lorsqu’elle est compilée à partir d’une ressource ou d’une mémoire.

</dd> <dt>

*ppShaderText* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne une mémoire tampon contenant une seule grande chaîne qui représente le flux de jetons mis en forme résultant.

</dd> <dt>

*ppErrorMsgs* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Retourne une mémoire tampon qui contient une liste d’erreurs et d’avertissements qui ont été rencontrés pendant la compilation. Ce sont les mêmes messages que le débogueur affiche lorsqu’il s’exécute en mode débogage. Cette valeur peut être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de nuanceur](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[**D3DXPreprocessShaderFromFile**](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[**D3DXPreprocessShader**](d3dxpreprocessshader.md)
</dt> </dl>

 

 
