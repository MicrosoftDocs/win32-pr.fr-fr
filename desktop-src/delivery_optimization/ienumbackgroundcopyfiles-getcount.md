---
title: IEnumBackgroundCopyFiles GetCount, méthode (Deliveryoptimization. h)
description: Récupère le nombre de fichiers dans l’énumération.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount (méthode)
- GetCount, méthode, IEnumBackgroundCopyFiles, interface
- Interface IEnumBackgroundCopyFiles, GetCount, méthode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915640"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>IEnumBackgroundCopyFiles :: GetCount, méthode

Récupère le nombre de fichiers dans l’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCount* \[ à\]
</dt> <dd>

Nombre de fichiers dans l’énumération.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





