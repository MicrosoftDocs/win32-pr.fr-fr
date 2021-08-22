---
description: 'ID3DXConstantTable :: GetDesc, méthode-obtient une description de la table constante.'
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'ID3DXConstantTable :: GetDesc, méthode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9e905eceefec4ea2e057776f1045a8fc7f7f213e38328406935c6095efd9c22c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607129"
---
# <a name="id3dxconstanttablegetdesc-method"></a>ID3DXConstantTable :: GetDesc, méthode

Obtient une description de la table constante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* \[ dans\]
</dt> <dd>

Type : **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***

Description de la table constante. Consultez [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




