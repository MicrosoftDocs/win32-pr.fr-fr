---
description: Définit le poids de fusion des priorités pour la piste d’animation spécifiée.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'ID3DXAnimationController :: SetTrackPriority, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: be294710fcd6ec2d8e72c7d7c9437623d29a2729a52144d4edfdc91e5be7eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848969"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>ID3DXAnimationController :: SetTrackPriority, méthode

Définit le poids de fusion des priorités pour la piste d’animation spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Suivre* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Identificateur de suivi.

</dd> <dt>

*Priorité* \[ dans\]
</dt> <dd>

Type : **[ **D3DXPRIORITY \_**](./d3dxpriority-type.md)**

Suivre la priorité. Ce paramètre doit être défini sur l’une des constantes du [**\_ type D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
