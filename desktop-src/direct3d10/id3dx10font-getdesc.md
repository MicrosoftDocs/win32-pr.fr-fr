---
description: Obtient une description de l’objet de police en cours.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font :: GetDesc, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523210"
---
# <a name="id3dx10fontgetdesc-method"></a>ID3DX10Font :: GetDesc, méthode

Obtient une description de l’objet de police en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDesc* \[ dans\]
</dt> <dd>

Type : description de la **[ **\_ police \_ d3dx10**](d3dx10-font-desc.md)\***

Pointeur vers une [**structure \_ \_ desc de police d3dx10**](d3dx10-font-desc.md) qui décrit l’objet font. Si UNICODE est défini, un pointeur vers un D3DX10FONT \_ DESCW est retourné ; sinon, un pointeur vers un D3DX10FONT \_ DESCA est retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Cette méthode décrit les objets de police Unicode si UNICODE est défini. Sinon, GetDescA est appelé, ce qui retourne un pointeur vers la \_ structure D3DX10FONT DESCA.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




