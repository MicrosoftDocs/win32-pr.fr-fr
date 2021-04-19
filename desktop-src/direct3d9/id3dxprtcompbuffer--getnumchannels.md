---
description: Récupère le nombre de canaux de couleurs utilisés en mémoire pour stocker des exemples.
ms.assetid: 8b033cda-feec-4e74-a4c4-ea44b5fb12c7
title: 'ID3DXPRTCompBuffer :: GetNumChannels, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 85712ecc6d9cb4875b93627dfcb15558c33681f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545316"
---
# <a name="id3dxprtcompbuffergetnumchannels-method"></a>ID3DXPRTCompBuffer :: GetNumChannels, méthode

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

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
