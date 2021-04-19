---
description: Définit le suivi sur l’heure d’animation locale spécifiée.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'ID3DXAnimationController :: SetTrackPosition, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535832"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a>ID3DXAnimationController :: SetTrackPosition, méthode

Définit le suivi sur l’heure d’animation locale spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de suivi.

</dd> <dt>

*Position* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Valeur d’heure d’animation locale à assigner à la piste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
