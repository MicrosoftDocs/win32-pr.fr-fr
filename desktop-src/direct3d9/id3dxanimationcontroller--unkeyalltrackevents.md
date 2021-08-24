---
description: Supprime tous les événements d’une piste d’animation spécifiée.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: 'ID3DXAnimationController :: UnkeyAllTrackEvents, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 196f1041d725f8aed39e54626e00b849f2be09587d5ccd40fbc3d8a091fc1b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791109"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a>ID3DXAnimationController :: UnkeyAllTrackEvents, méthode

Supprime tous les événements d’une piste d’animation spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de la piste sur laquelle tous les événements doivent être supprimés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Remarques

Cette méthode empêche l’exécution de tous les événements précédemment planifiés sur la piste et ignore toutes les données associées à ces événements.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
