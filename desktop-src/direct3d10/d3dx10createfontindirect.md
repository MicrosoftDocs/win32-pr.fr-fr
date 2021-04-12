---
description: Crée un objet de police. Remarque au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser DirectWrite et la bibliothèque DirectXTK, SpriteFont Class.
ms.assetid: 057ee033-37d8-4fc1-9f35-776393fff008
title: D3DX10CreateFontIndirect, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateFontIndirect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ae69b02483a94a80a06ef52ee4857eb081cfcfb2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322770"
---
# <a name="d3dx10createfontindirect-function"></a>D3DX10CreateFontIndirect fonction)

Crée un objet de police.

> [!Note]  
> Au lieu d’utiliser cette fonction, nous vous recommandons d’utiliser [DirectWrite](../directwrite/direct-write-portal.md) et la bibliothèque [DirectXTK](https://github.com/Microsoft/DirectXTK) , la classe **SpriteFont** .

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateFontIndirect(
  _In_        ID3D10Device     *pDevice,
  _In_  const D3DX10_FONT_DESC *pDesc,
  _Out_       LPD3DX10FONT     *ppFont
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Pointeur vers une interface d' [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) .

</dd> <dt>

*pDesc* \[ dans\]
</dt> <dd>

Type : **const [**d3dx10 \_ \_ Description**](d3dx10-font-desc.md) \*** de la police

Pointeur vers une structure de [**\_ police d3dx10 \_**](d3dx10-font-desc.md) décrivant les attributs de l’objet font à créer. Si Unicode est défini, l’appel de fonction est résolu en D3DXCreateFontIndirectW. Dans le cas contraire, l’appel de fonction est résolu en D3DXCreateFontIndirectA, car les chaînes ANSI sont utilisées.

</dd> <dt>

*ppFont* \[ à\]
</dt> <dd>

Type : **[ **LPD3DX10FONT**](id3dx10font.md)\***

Retourne un pointeur vers une [**interface ID3DX10Font**](id3dx10font.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
