---
description: 'ID3DXTextureShader :: GetConstantByName, méthode-obtient une constante en recherchant son nom.'
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: 'ID3DXTextureShader :: GetConstantByName, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55b3de81179c01171d7ee5ff7b845295709dfb8ead1a9bc1a7cdf615bc37c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729100"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>ID3DXTextureShader :: GetConstantByName, méthode

Obtient une constante en recherchant son nom.

## <a name="syntax"></a>Syntaxe


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hConstant* \[ dans\]
</dt> <dd>

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Handle](handles.md) de la structure de données parent. Si la constante est un paramètre de niveau supérieur (il n’y a aucune structure de données parent), utilisez la **valeur null**.

</dd> <dt>

*pname* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne contenant le nom de la constante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retourne un identificateur unique à la constante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
