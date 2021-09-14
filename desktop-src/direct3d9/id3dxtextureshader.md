---
description: Interface ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interface ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854967"
---
# <a name="id3dxtextureshader-interface"></a>Interface ID3DXTextureShader

Interface ID3DXTextureShader.

## <a name="members"></a>Membres

L’interface **ID3DXTextureShader** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureShader** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXTextureShader** possède ces méthodes.



| Méthode                                                                                       | Description                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**GetConstant**](id3dxtextureshader--getconstant.md)                                       | Obtient une constante en recherchant son index.<br/>                         |
| [**GetConstantBuffer**](id3dxtextureshader--getconstantbuffer.md)                           | Obtient un pointeur vers la table constante.<br/>                             |
| [**GetConstantByName**](id3dxtextureshader--getconstantbyname.md)                           | Obtient une constante en recherchant son nom.<br/>                          |
| [**GetConstantDesc**](id3dxtextureshader--getconstantdesc.md)                               | Obtient un pointeur vers le tableau de constantes dans la table constante.<br/>  |
| [**GetConstantElement**](id3dxtextureshader--getconstantelement.md)                         | Obtient une constante de la table constante.<br/>                          |
| [**GetDesc**](id3dxtextureshader--getdesc.md)                                               | Obtient une description de la table constante.<br/>                        |
| [**GetFunction**](id3dxtextureshader--getfunction.md)                                       | Obtient un pointeur vers le flux de fonction DWORD.<br/>                     |
| [**SetBool**](id3dxtextureshader--setbool.md)                                               | Définit une valeur BOOL.<br/>                                               |
| [**SetBoolArray**](id3dxtextureshader--setboolarray.md)                                     | Définit un tableau de valeurs BOOL.<br/>                                    |
| [**SetDefaults**](id3dxtextureshader--setdefaults.md)                                       | Affecte aux constantes les valeurs par défaut déclarées dans le nuanceur.<br/> |
| [**SetFloat**](id3dxtextureshader--setfloat.md)                                             | Définit un nombre à virgule flottante.<br/>                                    |
| [**SetFloatArray**](id3dxtextureshader--setfloatarray.md)                                   | Définit un tableau de nombres à virgule flottante.<br/>                         |
| [**SetInt**](id3dxtextureshader--setint.md)                                                 | Définit une valeur entière.<br/>                                           |
| [**SetIntArray**](id3dxtextureshader--setintarray.md)                                       | Définit un tableau d’entiers.<br/>                                       |
| [**SetMatrix**](id3dxtextureshader--setmatrix.md)                                           | Définit une matrice non transposée.<br/>                                    |
| [**SetMatrixArray**](id3dxtextureshader--setmatrixarray.md)                                 | Définit un tableau de matrices non transposées.<br/>                        |
| [**SetMatrixPointerArray**](id3dxtextureshader--setmatrixpointerarray.md)                   | Définit un tableau de pointeurs vers des matrices non transposées.<br/>            |
| [**SetMatrixTranspose**](id3dxtextureshader--setmatrixtranspose.md)                         | Définit une matrice transposée.<br/>                                        |
| [**SetMatrixTransposeArray**](id3dxtextureshader--setmatrixtransposearray.md)               | Définit un tableau de matrices transposées.<br/>                            |
| [**SetMatrixTransposePointerArray**](id3dxtextureshader--setmatrixtransposepointerarray.md) | Définit un tableau de pointeurs vers des matrices transposées.<br/>                |
| [**SetValue**](id3dxtextureshader--setvalue.md)                                             | Définit la table de constantes avec les données dans la mémoire tampon.<br/>             |
| [**SetVector**](id3dxtextureshader--setvector.md)                                           | Définit un vecteur 4D.<br/>                                                |
| [**SetVectorArray**](id3dxtextureshader--setvectorarray.md)                                 | Définit un tableau de vecteurs 4D.<br/>                                     |



 

## <a name="remarks"></a>Notes

L’interface **ID3DXTextureShader** est obtenue en appelant la fonction [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .

L’interface **ID3DXTextureShader** , comme toutes les interfaces com, hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

Le type LPD3DXTEXTURESHADER est défini comme un pointeur vers l’interface **ID3DXTextureShader** .


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
