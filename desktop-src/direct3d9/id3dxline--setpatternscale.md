---
description: Étire le modèle stipple le long de la direction de la ligne.
ms.assetid: 411464db-d721-4252-bff3-bec57252273e
title: 'ID3DXLine :: SetPatternScale, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df460f8040b1f73d4837b51533586a19630eed1ddcf435291857b05dc4bae1a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951359"
---
# <a name="id3dxlinesetpatternscale-method"></a>ID3DXLine :: SetPatternScale, méthode

Étire le modèle stipple le long de la direction de la ligne.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPatternScale(
  [in] FLOAT fPatternScale
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fPatternScale* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Valeur de mise à l’échelle du modèle stipple. 1.0 f est la valeur par défaut et ne représente aucune mise à l’échelle. Une valeur inférieure à 1,0 f réduit le modèle, et une valeur supérieure à 1,0 étire le modèle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
