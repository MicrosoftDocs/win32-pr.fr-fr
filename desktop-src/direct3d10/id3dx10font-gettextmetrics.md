---
description: Récupérez les caractéristiques de police.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font :: GetTextMetrics, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 97cbddc59dd84d0a5b83610212fe94e87a49757da0430d64cb420280c815d9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047047"
---
# <a name="id3dx10fontgettextmetrics-method"></a>ID3DX10Font :: GetTextMetrics, méthode

Récupérez les caractéristiques de police.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTextMetrics* \[ dans\]
</dt> <dd>

Type : **TEXTMETRIC \***

Pointeur vers une structure [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) , qui contient les propriétés de police. Si Unicode est défini, la fonction retourne une structure TEXTMETRICW. Dans le cas contraire, la fonction retourne une structure TEXTMETRICA.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](../winprog/windows-data-types.md)**

Une valeur différente de zéro si la fonction réussit ; sinon, 0.

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

 

 
