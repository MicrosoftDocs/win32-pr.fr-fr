---
description: Obtient le nombre maximal d’influences pour un vertex de la maille.
ms.assetid: 012168e8-30e5-4571-b793-647ab23df068
title: 'ID3DXSkinInfo :: GetMaxVertexInfluences, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxVertexInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cd33155ba5b306fc24e345f535a083c78031da243b291f2c36c5894561e270d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095709"
---
# <a name="id3dxskininfogetmaxvertexinfluences-method"></a>ID3DXSkinInfo :: GetMaxVertexInfluences, méthode

Obtient le nombre maximal d’influences pour un vertex de la maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMaxVertexInfluences(
  [in] DWORD *maxVertexInfluences
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*maxVertexInfluences* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)\***

Pointeur vers l’influence de vertex maximale.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
