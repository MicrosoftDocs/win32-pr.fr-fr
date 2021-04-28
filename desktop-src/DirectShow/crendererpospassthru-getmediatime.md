---
description: 'Méthode CRendererPosPassThru. GetMediaTime : la méthode GetMediaTime récupère les horodatages sur l’échantillon actuel.'
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Méthode CRendererPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085367"
---
# <a name="crendererpospassthrugetmediatime-method"></a>Méthode CRendererPosPassThru. GetMediaTime

La `GetMediaTime` méthode récupère les horodatages sur l’échantillon actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStartTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de début, en unités du format d’heure actuel.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Pointeur vers une variable qui reçoit l’heure de fin, en unités du format d’heure actuel. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                                  | Description                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Réussite.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | La conversion vers ce format n’est pas prise en charge.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>    | Argument de pointeur **null** .<br/>                  |



 

## <a name="remarks"></a>Notes 

Cette méthode remplace la méthode [**CPosPassThru :: GetMediaTime**](cpospassthru-getmediatime.md) . Les valeurs de date et d’heure sont converties au format d’heure actuel en appelant la méthode [**CPosPassThru :: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




