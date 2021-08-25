---
description: Réinitialise l’heure de l’animation globale à zéro. Tous les événements en attente conservent leurs planifications d’origine, mais dans le nouveau délai.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController :: ResetTime, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3f5f4ba6f10d5119e479a56e9e207e410b2d1e817d6809e7ceac1c98c8d2ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893739"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>ID3DXAnimationController :: ResetTime, méthode

Réinitialise l’heure de l’animation globale à zéro. Tous les événements en attente conservent leurs planifications d’origine, mais dans le nouveau délai.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode est généralement utilisée lorsque la valeur d’heure de l’animation globale est proche de la précision maximale du DOUBLE stockage, ou 2 ⁶ ⁴-1.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




