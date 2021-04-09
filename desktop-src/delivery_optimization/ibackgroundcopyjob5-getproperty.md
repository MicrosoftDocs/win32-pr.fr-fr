---
title: IBackgroundCopyJob5 GetProperty, méthode (Deliveryoptimization. h)
description: Méthode générique pour obtenir les propriétés du travail d’optimisation de la remise (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, méthode GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942217"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>IBackgroundCopyJob5 :: GetProperty, méthode

Méthode générique pour obtenir les propriétés du travail d’optimisation de la remise (DO).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyId* \[ dans\]
</dt> <dd>

ID de la propriété obtenue spécifiée comme [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valeur enum.

</dd> <dt>

*pPropertyValue* \[ à\]
</dt> <dd>

Valeur de la propriété retournée en tant qu’BITS_JOB_PROPERTY_VALUE Union.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne les valeurs de retour suivantes.



| Code de retour                                                                          | Description        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Succès<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5 :: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





