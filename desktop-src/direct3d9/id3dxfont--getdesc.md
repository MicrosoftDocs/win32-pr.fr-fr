---
description: Obtient une description de l’objet de police en cours. GetDescW et GetDescA sont identiques à cette méthode, sauf qu’un pointeur est retourné à une \_ structure D3DXFONT DESCW ou D3DXFONT \_ DESCA, respectivement.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont :: GetDesc, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2961c69e47bb46eaf782e8f5d4dbfe0be2d82a49f00f98c36b1ee7b141e962b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675429"
---
# <a name="id3dxfontgetdesc-method"></a>ID3DXFont :: GetDesc, méthode

Obtient une description de l’objet de police en cours. GetDescW et GetDescA sont identiques à cette méthode, sauf qu’un pointeur est retourné à une structure [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ DESCA** , respectivement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* \[ à\]
</dt> <dd>

Type : **[ **D3DXFONT \_ desc**](d3dxfont-desc.md)\***

Pointeur vers une structure [**D3DXFONT \_ desc**](d3dxfont-desc.md) qui décrit l’objet font.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode décrit les objets de police Unicode si UNICODE est défini. Sinon, GetDescA est appelé, ce qui retourne un pointeur vers la structure [**D3DXFONT \_ DESCA**](d3dxfont-desc.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




