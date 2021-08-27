---
description: 'La méthode ZeroBetween2 supprime tous les éléments de la piste entre les heures spécifiées. Cette méthode est équivalente à IAMTimelineTrack :: ZeroBetween, mais prend des valeurs REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'IAMTimelineTrack :: ZeroBetween2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72ea9d96be976f1b09e1cdc9721eb5eebe7adce2905d7a028d70a9ff50ff58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952778"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>IAMTimelineTrack :: ZeroBetween2, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `ZeroBetween2` méthode supprime tous les éléments de la piste entre les heures spécifiées. Cette méthode est équivalente à [**IAMTimelineTrack :: ZeroBetween**](iamtimelinetrack-zerobetween.md), mais prend des valeurs [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rtStart* 
</dt> <dd>

Début de la plage à effacer, en secondes.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Fin de la plage à effacer, en secondes.

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

 

 




