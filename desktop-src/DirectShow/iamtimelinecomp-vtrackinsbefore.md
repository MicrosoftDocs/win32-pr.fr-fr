---
description: La méthode VTrackInsBefore insère une piste virtuelle dans la composition à la priorité spécifiée.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'IAMTimelineComp :: VTrackInsBefore, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857787"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>IAMTimelineComp :: VTrackInsBefore, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `VTrackInsBefore` méthode insère une piste virtuelle dans la composition à la priorité spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle.

</dd> <dt>

*Priorité* 
</dt> <dd>

Priorité à laquelle insérer la piste virtuelle, ou – 1 pour insérer la piste virtuelle à la fin de la liste de priorités. La liste priorité détermine les clips visibles. Pour plus d'informations, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                   | Description                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Réussite.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argument non valide.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | L’objet n’est pas une piste virtuelle.<br/> |



 

## <a name="remarks"></a>Notes

Chaque piste virtuelle de la composition a un niveau de priorité unique. Les niveaux de priorité sont compris entre 0 et *n* -1, où *n* est le nombre de pistes virtuelles dans la composition. Pour les groupes vidéo, une piste virtuelle masque toutes les pistes virtuelles avec un niveau de priorité inférieur, sauf dans les endroits où la piste est vide ou contient une transition. Vous pouvez considérer les pistes virtuelles comme des couches dans la composition finale. La piste 1 est superposée au-dessus de la piste 0, la piste 2 est superposée au-dessus de la piste 1, et ainsi de suite.

Si vous spécifiez-1 pour le paramètre *Priority* , la piste virtuelle est insérée à la fin de la liste, avec une valeur de priorité plus élevée que les pistes existantes. Si vous spécifiez une valeur de priorité qui existe déjà dans la composition, chaque piste avec une priorité égale ou supérieure se déplace vers le haut d’un niveau de priorité.

**Exemple**: Track A a la priorité 0 et la piste B a la priorité 1. Si la piste C est insérée à la priorité 0, effectuez le suivi d’un déplacement vers la priorité 1, et la piste B passe à la priorité 2.

Si la priorité spécifiée est supérieure au nombre actuel de suivis dans la composition, la méthode échoue.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




