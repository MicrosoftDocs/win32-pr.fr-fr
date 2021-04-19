---
description: Normalise tous les pondérations de l’analyse des composants principaux (PCA) afin qu’elles soient comprises entre-1 et 1. Les vecteurs de base sont modifiés pour refléter cette normalisation.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'ID3DXPRTCompBuffer :: NormalizeData, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106528572"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a>ID3DXPRTCompBuffer :: NormalizeData, méthode

Normalise tous les pondérations de l’analyse des composants principaux (PCA) afin qu’elles soient comprises entre-1 et 1. Les vecteurs de base sont modifiés pour refléter cette normalisation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




