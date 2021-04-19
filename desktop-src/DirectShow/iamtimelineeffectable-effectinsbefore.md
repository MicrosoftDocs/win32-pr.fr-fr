---
description: La méthode EffectInsBefore insère un effet dans l’objet au niveau de priorité spécifié.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'IAMTimelineEffectable :: EffectInsBefore, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537916"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>IAMTimelineEffectable :: EffectInsBefore, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `EffectInsBefore` méthode insère un effet dans l’objet au niveau de priorité spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFX* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’effet.

</dd> <dt>

*Priorité* 
</dt> <dd>

Niveau de priorité auquel insérer l’effet. Utilisez la valeur-1 pour insérer l’effet à la fin de la liste de priorités.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK en cas de réussite ou E \_ NOTIMPL si l’objet n’est pas un effet. Sinon, retourne une autre valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes

Les heures de début et de fin de l’effet sont découpées dans les limites de la plage horaire de l’objet, si nécessaire. S’il existe déjà un effet au niveau de priorité spécifié, tous les effets de ce point sur descendent dans la liste des priorités pour faire de la place pour le nouvel effet.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




