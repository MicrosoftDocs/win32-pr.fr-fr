---
description: Récupère les valeurs Albedo des vertex de maillage.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'ID3DXPRTEngine :: GetVertexAlbedo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bdaf264e887c12b6dd711be978c5fc233bacc14d41d0899ddda43473001fe6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985559"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a>ID3DXPRTEngine :: GetVertexAlbedo, méthode

Récupère les valeurs Albedo des vertex de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVertColors* \[ in, out\]
</dt> <dd>

Type : **[ **D3DXCOLOR**](d3dxcolor.md)\***

Pointeur vers un tableau de destination de valeurs Albedo des vertex de maillage. Consultez [**D3DXCOLOR**](d3dxcolor.md).

</dd> <dt>

*NumVerts* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex dans la maille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
