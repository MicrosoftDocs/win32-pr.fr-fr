---
description: Obtient une constante de la table constante.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'ID3DXTextureShader :: GetConstantElement, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02d21efb3ef0ed5d4602833571b2b1a32e73df73b76f82a357cda574e93e84ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747388"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>ID3DXTextureShader :: GetConstantElement, méthode

Obtient une constante de la table constante.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Handle](handles.md) vers le tableau de constantes. Cette valeur ne peut pas être **null**.

</dd> <dt>

*Index* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de base zéro de l’élément dans la table constante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne un identificateur unique à la constante.

## <a name="remarks"></a>Remarques

Pour obtenir une constante qui ne fait pas partie d’un tableau, utilisez [**ID3DXTextureShader :: GetConstant**](id3dxtextureshader--getconstant.md) ou [**ID3DXTextureShader :: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
