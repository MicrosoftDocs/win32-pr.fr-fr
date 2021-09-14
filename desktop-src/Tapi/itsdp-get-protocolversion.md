---
description: La \_ méthode obtenir ProtocolVersion obtient la version du protocole 2327 SDP (session descripteur).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'ITSdp :: get_ProtocolVersion, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193484"
---
# <a name="itsdpget_protocolversion-method"></a>ITSdp :: \_ ProtocolVersion, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ ProtocolVersion** obtient la version du protocole 2327 SDP (session descripteur).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProtocolVersion* \[ à\]
</dt> <dd>

Pointeur désignant la version du protocole.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                        |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pProtocolVersion* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>     |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                       |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                      |



 

## <a name="requirements"></a>Spécifications



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

 

 




