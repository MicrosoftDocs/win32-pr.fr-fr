---
description: Obtient un pointeur vers le tableau de constantes dans la table constante.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: 'ID3DXTextureShader :: GetConstantDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22898880e5cef5669defae89cda4f7d9818f9f1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529628"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>ID3DXTextureShader :: GetConstantDesc, méthode

Obtient un pointeur vers le tableau de constantes dans la table constante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificateur unique d’une constante. Consultez [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXCONSTANT \_ desc**](d3dxconstant-desc.md)\***

Retourne un pointeur vers un tableau de descriptions. Consultez [**D3DXCONSTANT \_ desc**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)\***

L’entrée fournie doit correspondre à la taille maximale du tableau. La sortie est le nombre d’éléments qui sont remplis dans le tableau lorsque la fonction retourne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="remarks"></a>Notes

Les échantillonneurs peuvent apparaître plusieurs fois dans une table constante. par conséquent, cette méthode peut retourner un tableau de descriptions, chacune avec un index de Registre différent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader::GetDesc**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
