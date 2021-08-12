---
description: 'ID3DXPRTBuffer :: GetNumChannels, méthode-récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker les échantillons.'
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
ms.openlocfilehash: a86bac0a827839180cf746f762c39c583e64a4f80c4ebeac1d4e5e936ca69c51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294102"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a>ID3DXPRTBuffer :: GetNumChannels, méthode

Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.

## <a name="syntax"></a>Syntaxe


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

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

 

 
