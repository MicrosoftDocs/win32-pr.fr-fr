---
title: IBackgroundCopyJob5 SetProperty, méthode (Deliveryoptimization. h)
description: Méthode générique pour définir les propriétés de la tâche d’optimisation de la remise.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, méthode SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b006ab3c4e53db1a9e76d35c8812ec32f09dffa
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520499"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5 :: SetProperty, méthode

Méthode générique pour définir les propriétés de la tâche d’optimisation de la remise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyId* \[ dans\]
</dt> <dd>

ID de la propriété définie spécifiée comme [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valeur d’énumération.

</dd> <dt>

*PropertyValue* \[ dans\]
</dt> <dd>

Valeur de la propriété qui est définie. Pour stocker une valeur dont le type est approprié à la propriété, cette valeur est spécifiée via le [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Union qui est composé de tous les types de propriété connus.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne les valeurs de retour suivantes.



| Code de retour                                                                          | Description        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Succès<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5 :: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





