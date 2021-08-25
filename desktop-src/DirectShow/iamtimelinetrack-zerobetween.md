---
description: La méthode ZeroBetween supprime tous les éléments de la piste entre les heures spécifiées. Cette méthode fractionne tous les objets qui s’étendent sur la plage de temps spécifiée et supprime les parties qui se trouvent dans la plage.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'IAMTimelineTrack :: ZeroBetween, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b5ec57833ed34a432988c42351a333362168112174cccd7a989e0c2e1bddd694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982899"
---
# <a name="iamtimelinetrackzerobetween-method"></a>IAMTimelineTrack :: ZeroBetween, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `ZeroBetween` méthode supprime tous les éléments de la piste entre les heures spécifiées. Cette méthode fractionne tous les objets qui s’étendent sur la plage de temps spécifiée et supprime les parties qui se trouvent dans la plage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtStart* 
</dt> <dd>

Début de la plage à effacer, en unités de 100 nanosecondes.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Fin de la plage à effacer, en unités de 100 nanosecondes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.



| Code de retour                                                                             | Description                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | L’intervalle de temps dépasse tous les éléments de la piste.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Réussite.<br/>                                             |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




