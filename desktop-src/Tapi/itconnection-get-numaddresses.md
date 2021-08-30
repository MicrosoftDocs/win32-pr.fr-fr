---
description: La \_ méthode obtenir NumAddresses obtient le nombre d’adresses à utiliser pour la session.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'ITConnection :: get_NumAddresses, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13a2bae08e4d989b0ce9a64b651e777d3c9b1cb0744f63798f06bf182aede58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991889"
---
# <a name="itconnectionget_numaddresses-method"></a>ITConnection :: \_ NumAddresses, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ NumAddresses** obtient le nombre d’adresses à utiliser pour la session.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNumAddresses* \[ à\]
</dt> <dd>

Nombre d’adresses pour la session.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                     |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pNumAddresse* s n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>  |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                    |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 




