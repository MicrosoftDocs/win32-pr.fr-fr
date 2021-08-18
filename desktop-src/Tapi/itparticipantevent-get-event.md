---
description: La \_ méthode d’événement obtenir obtient un \_ descripteur d’événement participant du type d’événement qui s’est produit.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'ITParticipantEvent :: get_Event, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d45e8f6aab556eb1b6f5c6dc1b4b0cbadf9653e06fd77f4fb806b7ef89d7813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864700"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                         |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>      |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pParticipantEvent* n’est pas un pointeur valide.<br/> |



 

## <a name="requirements"></a>Configuration requise



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

 

 




