---
description: La \_ méthode d’événement obtenir obtient un \_ descripteur d’événement participant du type d’événement qui s’est produit.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'ITParticipantEvent :: get_Event, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095678"
---
# <a name="itparticipanteventget_event-method"></a>ITParticipantEvent :: acobtiens, \_ méthode d’événement

\[en **savoir \_ plus l’événement** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode d' **\_ événement obtenir** obtient un descripteur d' [**\_ événement participant**](participant-event.md) du type d’événement qui s’est produit.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pParticipantEvent* \[ à\]
</dt> <dd>

Pointeur vers le descripteur d' [**\_ événement participant**](participant-event.md) de l’événement.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>      |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pParticipantEvent* n’est pas un pointeur valide.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**\_événement participant**](participant-event.md)
</dt> </dl>

 

 




