---
description: Récupère les caractéristiques de police qui sont identifiées dans une structure TEXTMETRIC. Cette méthode prend en charge les paramètres du compilateur ANSI et Unicode.
ms.assetid: 37788281-5bb0-45bb-b6d4-bdc4d811e3af
title: 'ID3DXFont :: GetTextMetrics, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetTextMetrics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ce6064804d2aac2846cbea6971f145fc07759f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322882"
---
# <a name="id3dxfontgettextmetrics-method"></a>ID3DXFont :: GetTextMetrics, méthode

Récupère les caractéristiques de police qui sont identifiées dans une structure [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) . Cette méthode prend en charge les paramètres du compilateur ANSI et Unicode.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetTextMetrics(
  [out] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTextMetrics* \[ à\]
</dt> <dd>

Type : **[ **TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)\***

Pointeur vers une structure [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica) , qui contient les propriétés de police.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Une valeur différente de zéro si la fonction réussit ; sinon, 0.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également le type de structure. Si Unicode est défini, la fonction retourne une structure TEXTMETRICW. Dans le cas contraire, l’appel de fonction retourne une structure TEXTMETRICA.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 
