---
description: La méthode GetVTrack récupère la piste virtuelle à la priorité spécifiée.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'IAMTimelineComp :: GetVTrack, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 245f19783f7a472f86544d14f27c588e7a5938e899f2f389887d7a7817d6254e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756299"
---
# <a name="iamtimelinecompgetvtrack-method"></a>IAMTimelineComp :: GetVTrack, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetVTrack` méthode récupère la piste virtuelle à la priorité spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppVirtualTrack* \[ à\]
</dt> <dd>

Reçoit l’interface [**IAMTimelineObj**](iamtimelineobj.md) de la piste virtuelle.

</dd> <dt>

*Et* 
</dt> <dd>

Priorité de la piste virtuelle à récupérer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                  | Description                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Aucune piste virtuelle avec la priorité spécifiée.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/>                    |



 

## <a name="remarks"></a>Remarques

Si la méthode est réussie, l’interface **IAMTimelineObj** qu’elle retourne a un nombre de références en suspens. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




