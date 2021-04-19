---
description: Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.
ms.assetid: dd1e3590-78e1-41a2-9f15-79389d9a210a
title: 'ID3DXPRTBuffer :: GetNumChannels, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99456c6386a822489eca6beef41f639008007778
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539170"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a>ID3DXPRTBuffer :: GetNumChannels, méthode

Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.

## <a name="syntax"></a>Syntaxe


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](../winprog/windows-data-types.md)**

Retourne le nombre de canaux de couleurs utilisés en mémoire pour stocker les échantillons. La valeur est généralement 1 pour représenter les valeurs de luminance, ou 3 pour représenter les valeurs RVB.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
