---
description: L’interface ID3DXConstantTable est utilisée pour accéder à la table constante. Ce tableau contient les variables utilisées par les nuanceurs et les effets de langages de haut niveau.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interface ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ead9e594e79daf8bd43bf4125b857030482028f7128c8063196413d52c9a8b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675479"
---
# <a name="id3dxconstanttable-interface"></a>Interface ID3DXConstantTable

L’interface ID3DXConstantTable est utilisée pour accéder à la table constante. Ce tableau contient les variables utilisées par les nuanceurs et les effets de langages de haut niveau.

## <a name="members"></a>Membres

L’interface **ID3DXConstantTable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXConstantTable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXConstantTable** possède ces méthodes.



| Méthode                                                                                       | Description                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Obtient un pointeur vers la mémoire tampon qui contient la table constante.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Obtient la taille de la mémoire tampon de la table constante.<br/>                                                                             |
| [**GetConstant**](id3dxconstanttable--getconstant.md)                                       | Obtient une constante en recherchant son index.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Obtient une constante en recherchant son nom.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Obtient un pointeur vers un tableau de descriptions constantes dans la table constante.<br/>                                              |
| [**GetConstantElement**](id3dxconstanttable--getconstantelement.md)                         | Obtient une constante d’un tableau de constantes. Un tableau est constitué d’éléments.<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Obtient une description de la table constante.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Retourne l’index de l’échantillonneur.<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | Définit une valeur booléenne.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Définit un tableau de valeurs booléennes.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Affecte aux constantes leurs valeurs par défaut. Les valeurs par défaut sont déclarées dans les déclarations de variable dans le nuanceur.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Définit un nombre à virgule flottante.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Définit un tableau de nombres à virgule flottante.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Définit une valeur entière.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Définit un tableau d’entiers.<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | Définit une matrice nontransposed.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Définit un tableau de matrices nontransposed.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Définit un tableau de pointeurs sur les matrices nontransposed.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Définit une matrice transposée.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Définit un tableau de matrices transposées.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Définit un tableau de pointeurs vers des matrices transposées.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Définit le contenu de la mémoire tampon sur la table constante.<br/>                                                                  |
| [**SetVector**](id3dxconstanttable--setvector.md)                                           | Définit un vecteur 4D.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Définit un tableau de vecteurs 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Remarques

Le type LPD3DXCONSTANTTABLE est défini comme un pointeur vers l’interface **ID3DXConstantTable** .


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
