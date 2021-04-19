---
description: La \_ méthode put StartTime définit la valeur de l’heure de début du protocole NTP (Network Time Protocol) 32 bits. La session est considérée comme active à partir de cette heure.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: ITTime ::p ut_StartTime, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540404"
---
# <a name="ittimeput_starttime-method"></a>ITTime ::p ut \_ StartTime, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **put \_ StartTime** définit la valeur de l’heure de début du protocole NTP (Network Time Protocol) 32 bits. La session est considérée comme active à partir de cette heure.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Heure* \[ dans\]
</dt> <dd>

Heure de début de la session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *Tim* e n’est pas valide.<br/>                   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données. Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.

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

[**ITTime :: obtient \_ StartTime**](ittime-get-starttime.md)
</dt> </dl>

 

 




