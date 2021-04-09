---
description: Obtient un pointeur vers un tableau de descriptions constantes dans la table constante.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: 'ID3DXConstantTable :: GetConstantDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953872"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>ID3DXConstantTable :: GetConstantDesc, méthode

Obtient un pointeur vers un tableau de descriptions constantes dans la table constante.

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

Identificateur unique d’une constante. Consultez [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

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

**ID3DXConstantTable :: GetConstantDesc** retourne parfois une [**\_ desc D3DXCONSTANT**](d3dxconstant-desc.md) avec un \_ nombre de registres égal à 0. Cela se produit si une constante apparaît dans plusieurs registres, \_ mais n’a pas d’espace dans ce jeu de registres alloué.

Comme un échantillonneur peut apparaître plusieurs fois dans une table constante, cette méthode peut retourner un tableau de descriptions, chacune avec un index de Registre différent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetDesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
