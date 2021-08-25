---
description: La méthode SetQOSApplicationID définit l’identificateur de QOS pour l’application.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID :: SetQOSApplicationID, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e7783efaf8ec30ea8f70fec634eefff0acd2f5df99453fc1958258a5a26597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774589"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>ITQOSApplicationID :: SetQOSApplicationID, méthode

\[cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetQOSApplicationID** définit l’identificateur de QoS pour l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pApplicationID* \[ dans\]
</dt> <dd>

Identificateur unique du processus d’application.

</dd> <dt>

*pApplicationGUID* \[ dans\]
</dt> <dd>

GUID de l’application.

</dd> <dt>

*pSubIDs* \[ dans\]
</dt> <dd>

Sub-IDs associé à l’appel en cours.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




