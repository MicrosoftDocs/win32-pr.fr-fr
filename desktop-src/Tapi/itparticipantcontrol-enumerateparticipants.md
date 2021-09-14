---
description: La méthode EnumerateParticipants énumère les participants associés à la Conférence en cours.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'ITParticipantControl :: EnumerateParticipants, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095694"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>ITParticipantControl :: EnumerateParticipants, méthode

\[**EnumerateParticipants** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **EnumerateParticipants** énumère les participants associés à la Conférence en cours. Cette méthode est fournie pour les applications C et C++. les applications clientes Automation, telles que celles écrites en Visual Basic, doivent utiliser la méthode d' [**extraction des \_ Participants**](itparticipantcontrol-get-participants.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnumParticipants* \[ à\]
</dt> <dd>

Pointeur vers l’interface [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                          |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppEnumParticipants* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>       |



 

## <a name="remarks"></a>Notes

L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumParticipant**](ienumparticipant.md) retournée par **ITParticipantControl :: EnumerateParticipants**. L’application doit appeler **Release** sur l’interface **IEnumParticipant** pour libérer les ressources qui lui sont associées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**accéder aux \_ participants**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




