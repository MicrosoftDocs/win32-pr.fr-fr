---
description: Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'ID3DX10Font :: GetGlyphData, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eaabcd6de2acf5ec86ab8c9a47d4224ed230104fe189816abd9d02fd3ac09596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302889"
---
# <a name="id3dx10fontgetglyphdata-method"></a>ID3DX10Font :: GetGlyphData, méthode

Retourne des informations sur le positionnement et l’orientation d’un glyphe dans une cellule de caractère.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Glyphe* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de glyphe.

</dd> <dt>

*ppTexture* \[ à\]
</dt> <dd>

Type : **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***

Adresse d’un pointeur vers un objet ID3D10Texture qui contient le glyphe.

</dd> <dt>

*pBlackBox* \[ dans\]
</dt> <dd>

Type : **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***

Pointeur vers le plus petit objet rectangle qui englobe complètement le glyphe. Consultez [Rect](/previous-versions//ms536136(v=vs.85)).

</dd> <dt>

*pCellInc* \[ dans\]
</dt> <dd>

Type : **point \***

Pointeur vers le vecteur à deux dimensions qui connecte l’origine de la cellule de caractère en cours à l’origine de la cellule de caractère suivante. Consultez [point](/previous-versions//ms536119(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.

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

 

 
