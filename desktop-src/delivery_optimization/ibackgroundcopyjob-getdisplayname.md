---
title: Méthode ibackgroundcopyjob GetDisplayName, méthode (Deliveryoptimization. h)
description: Récupère le nom complet du travail. En général, vous utilisez le nom complet pour identifier la tâche dans une interface utilisateur.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName (méthode)
- GetDisplayName, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, GetDisplayName, méthode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a50d2bdc1c492725b79368774f07755c7b629d73209a7d53f865cc738eb7025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755539"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>Méthode ibackgroundcopyjob :: GetDisplayName, méthode

Récupère le nom complet du travail. En général, vous utilisez le nom complet pour identifier la tâche dans une interface utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppDisplayName* \[ à\]
</dt> <dd>

Chaîne terminée par le caractère null qui contient le nom complet qui identifie le travail. Plusieurs travaux peuvent avoir le même nom complet. Appelez la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer *ppDisplayName* quand vous avez terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes, ainsi que d’autres.



| Code de retour                                                                                  | Description                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>     | Le nom d’affichage a été récupéré avec succès.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Le paramètre *ppDisplayName* ne peut pas avoir la **valeur null**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

