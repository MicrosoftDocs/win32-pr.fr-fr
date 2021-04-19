---
description: La méthode obtenir le \_ participant obtient un pointeur vers un tableau d’interfaces ITParticipant représentant les participants impliqués dans l’événement.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'ITParticipantEvent :: get_Participant, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537538"
---
# <a name="itparticipanteventget_participant-method"></a>ITParticipantEvent :: obtient la \_ méthode participante

\[en **savoir \_ plus Le participant** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir le \_ participant** obtient un pointeur vers un tableau d’interfaces [**ITParticipant**](itparticipant.md) représentant les participants impliqués dans l’événement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppParticipant* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’interfaces [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                           | Signification                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | La méthode a réussi.<br/>                                     |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>   | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>  |
| <dl> <dt>**\_NOitems TAPI E \_**</dt> </dl> | Aucun participant n’est associé à l’événement.<br/>  |
| <dl> <dt>**\_pointeur E**</dt> </dl>       | Le paramètre *ppParticipant* n’est pas un pointeur valide.<br/> |



 

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

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




