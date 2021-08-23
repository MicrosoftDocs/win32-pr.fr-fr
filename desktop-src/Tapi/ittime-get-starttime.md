---
description: La \_ méthode obtenir StartTime obtient la valeur d’heure de début du protocole NTP (Network Time Protocol) 32 bits. La session est considérée comme active à partir de cette heure.
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'ITTime :: get_StartTime, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2fcc7aedf94d65f828714a7ebe5e6bbbfd760514654b2b634b479f2fd4802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060757"
---
# <a name="ittimeget_starttime-method"></a>ITTime :: obtient la \_ méthode StartTime

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ StartTime** obtient la valeur d’heure de début du protocole NTP (Network Time Protocol) 32 bits. La session est considérée comme active à partir de cette heure.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pTime* \[ à\]
</dt> <dd>

Pointeur désignant l’heure de début de la session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pTime* n’est pas un pointeur valide.<br/>        |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime ::p ut \_ StartTime**](ittime-put-starttime.md)
</dt> </dl>

 

 




