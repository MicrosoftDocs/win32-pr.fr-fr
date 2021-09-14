---
description: Dessine une bande en courbes dans l’espace à l’écran. L’entrée se présente sous la forme d’un tableau qui définit les points (of D3DXVECTOR2) sur la bande.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine ::D méthode brute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998568"
---
# <a name="id3dxlinedraw-method"></a>ID3DXLine ::D méthode brute

Dessine une bande en courbes dans l’espace à l’écran. L’entrée se présente sous la forme d’un tableau qui définit les points (of [**D3DXVECTOR2**](d3dxvector2.md)) sur la bande.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVertexList* \[ dans\]
</dt> <dd>

Type : **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Tableau des vertex qui composent la ligne. Consultez [**D3DXVECTOR2**](d3dxvector2.md).

</dd> <dt>

*dwVertexListCount* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de vertex dans la liste de vertex.

</dd> <dt>

*Couleur* \[ dans\]
</dt> <dd>

Type : **[ **D3DCOLOR**](d3dcolor.md)**

Couleur de la ligne. Consultez [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
