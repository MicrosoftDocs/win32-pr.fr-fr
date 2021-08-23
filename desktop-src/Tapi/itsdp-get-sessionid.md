---
description: La \_ méthode obtenir SessionID obtient la valeur du protocole NTP (Network Time Protocol) 32 bits qui sert d’identificateur de session. Elle est générée automatiquement lors de la création de la session.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'ITSdp :: get_SessionId, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67f7e8ea9bef17e5cb34ca23443b1f16f815c964c3cf76b9b122878e8662d051
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621539"
---
# <a name="itsdpget_sessionid-method"></a>ITSdp :: obtient \_ SessionID, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ SessionID** obtient la valeur du protocole NTP (Network Time Protocol) 32 bits qui sert d’identificateur de session. Elle est générée automatiquement lors de la création de la session.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pSessionId* \[ à\]
</dt> <dd>

Pointeur vers l’identificateur de session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pSessionId* n’est pas valide.<br/>             |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pSessionId* n’est pas un pointeur valide.<br/>   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

la valeur de retour de cette méthode peut être **ULONG**, mais Visual Basic ne prend pas en charge le type **ulong** . Un **double** est le plus petit type suivant qui englobe la plage entière de valeurs requises.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




