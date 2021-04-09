---
title: IEnumBackgroundCopyFiles Skip, méthode (Deliveryoptimization. h)
description: Ignore le nombre spécifié d’éléments suivant dans la séquence d’énumération. S’il y a moins d’éléments restants dans la séquence que le nombre demandé d’éléments à ignorer, il ignore le dernier élément de la séquence.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip (méthode)
- Skip, méthode, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, Skip (méthode)
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032504"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a>IEnumBackgroundCopyFiles :: Skip, méthode

Ignore le nombre spécifié d’éléments suivant dans la séquence d’énumération. S’il y a moins d’éléments restants dans la séquence que le nombre demandé d’éléments à ignorer, il ignore le dernier élément de la séquence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d'éléments à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le nombre d’éléments demandés a été ignoré.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Valeur inférieure au nombre d’éléments demandés ignorée.<br/>    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





