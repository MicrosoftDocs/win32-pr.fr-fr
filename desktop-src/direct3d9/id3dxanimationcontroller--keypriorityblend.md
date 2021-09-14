---
description: Définit les clés d’événement de fusion pour la piste d’animation spécifiée.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController :: KeyPriorityBlend, méthode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916560"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>ID3DXAnimationController :: KeyPriorityBlend, méthode

Définit les clés d’événement de fusion pour la piste d’animation spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NewBlendWeight* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Nombre compris entre 0 et 1 qui est utilisé pour fusionner les pistes.

</dd> <dt>

*StartTime* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Heure globale de démarrage de la fusion.

</dd> <dt>

*Durée* \[ dans\]
</dt> <dd>

Type : **[ **double**](../winprog/windows-data-types.md)**

Durée globale de la fusion.

</dd> <dt>

*Transition* \[ dans\]
</dt> <dd>

Type : **[ **D3DXTRANSITION \_**](./d3dxtransition-type.md)**

Spécifie le type de transition utilisé pour la durée du Blend. Consultez [**\_ type D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Descripteur d’événement pour l’événement Priority Blend. La **valeur null** est retournée si un ou plusieurs des paramètres d’entrée ne sont pas valides ou si aucun événement libre n’est disponible.

## <a name="remarks"></a>Notes

Le contrôleur d’animation se mélange en trois phases : les pistes de faible priorité sont fusionnées en premier, les pistes haute priorité sont fusionnées en second, puis les résultats des deux sont fusionnés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
