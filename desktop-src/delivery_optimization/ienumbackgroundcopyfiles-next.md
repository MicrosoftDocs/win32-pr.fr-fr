---
title: Méthode IEnumBackgroundCopyFiles Next (Deliveryoptimization. h)
description: Récupère un nombre spécifié d’éléments dans la séquence d’énumération. Si le nombre d’éléments restants dans la séquence est inférieur au nombre demandé, il récupère les éléments restants.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Next, méthode
- Next, méthode, IEnumBackgroundCopyFiles, interface
- Interface IEnumBackgroundCopyFiles, méthode Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942605"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>IEnumBackgroundCopyFiles :: Next, méthode

Récupère un nombre spécifié d’éléments dans la séquence d’énumération. Si le nombre d’éléments restants dans la séquence est inférieur au nombre demandé, il récupère les éléments restants.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre d’éléments demandés.

</dd> <dt>

*rgelt* \[ à\]
</dt> <dd>

Tableau d’objets [**IBackgroundCopyFile**](ibackgroundcopyfile.md) . Lorsque vous avez terminé, vous devez libérer chaque objet dans *rgelt* .

</dd> <dt>

*pceltFetched* \[ à\]
</dt> <dd>

Nombre d’éléments retournés dans *rgelt*. Vous pouvez affecter à *pceltFetched* la **valeur null** si *celt* est un. Sinon, initialisez la valeur de *pceltFetched* à 0 avant d’appeler cette méthode.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                              | Description                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl> | Le nombre d’éléments demandés a été retourné.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Retourne une valeur inférieure au nombre d’éléments demandés.<br/>    |



 

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

 

 





