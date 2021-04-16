---
title: Méthode IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Demande des informations sur l’ordinateur cible sur lequel la connexion doit être redirigée.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetTargetInfo
- Méthode GetTargetInfo Services Bureau à distance, interface IConnectionBrokerClient
- Services Bureau à distance de l’interface IConnectionBrokerClient, méthode GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508302"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>IConnectionBrokerClient :: GetTargetInfo, méthode

Demande des informations sur l’ordinateur cible sur lequel la connexion doit être redirigée. Cette méthode est utilisée par le redirecteur pour obtenir des informations de redirection pour la demande de connexion entrante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pConnectionInfo* \[ dans\]
</dt> <dd>

Adresse d’une structure [**d' \_ \_ informations de connexion CB**](cb-connection-info.md) qui contient des informations sur la demande de connexion entrante.

</dd> <dt>

*Réservé* \[ dans\]
</dt> <dd>

Ce paramètre est réservé pour une utilisation ultérieure et doit être égal à zéro.

</dd> <dt>

*hStatusEvent* \[ dans\]
</dt> <dd>

Handle d’un événement qui est défini à chaque mise à jour de la progression de la requête. Vous êtes responsable de la création et de la fermeture de cet événement.

</dd> <dt>

*pTargetInfo* \[ à\]
</dt> <dd>

Adresse d’une structure [**d' \_ \_ informations de la cible CB**](cb-target-info.md) qui reçoit des informations sur l’ordinateur cible sur lequel la connexion entrante doit être redirigée. Étant donné qu’il s’agit d’une méthode asynchrone, cette mémoire doit rester disponible jusqu’à ce que la demande soit terminée. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

*pResult* \[ à\]
</dt> <dd>

Adresse d’une variable **DWORD** qui reçoit un code de résultat. Étant donné qu’il s’agit d’une méthode asynchrone, cette mémoire doit rester disponible jusqu’à ce que la demande soit terminée. Pour plus d'informations, consultez la section Notes.

Ce code de résultat sera l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Réussite.

</dd> <dt>

0x0000400
</dt> <dd>

L’ordinateur de destination est introuvable.

</dd> <dt>

0x0000401
</dt> <dd>

L’ordinateur de destination n’est pas disponible.

</dd> <dt>

0x0000402
</dt> <dd>

Erreur lors du chargement de l’ordinateur de destination.

</dd> <dt>

0x0000403
</dt> <dd>

Erreur lors de l’importation de l’ordinateur de destination en ligne.

</dd> <dt>

0x0000404
</dt> <dd>

Erreur lors de la redirection vers l’ordinateur de destination.

</dd> <dt>

0x0000405
</dt> <dd>

Erreur lors de la réactivation de la machine virtuelle.

</dd> <dt>

0x0000406
</dt> <dd>

Erreur lors du démarrage de la machine virtuelle.

</dd> <dt>

0x0000407
</dt> <dd>

Erreur lors de la recherche de l’adresse IP de la machine virtuelle.

</dd> <dt>

0x0000408
</dt> <dd>

Le service session Broker n’a trouvé aucun ordinateur disponible dans le pool.

</dd> <dt>

0x0000409
</dt> <dd>

Le courtier de session a annulé la connexion.

</dd> <dt>

0x0000410
</dt> <dd>

Le service session Broker n’a pas pu valider les paramètres de connexion.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ à\]
</dt> <dd>

Adresse d’un pointeur d’interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que vous utilisez pour obtenir des mises à jour d’État pour une opération asynchrone. Cette interface est utilisée conjointement avec le paramètre *hStatusEvent* pour attendre et obtenir les résultats de cette opération asynchrone.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **E \_ en attente** si la requête asynchrone est créée. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est asynchrone. Les paramètres *pTargetInfo* et *pResult* doivent rester valides jusqu’à ce que la méthode [**IConnectionBrokerRequest :: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtienne la **demande d’État CB \_ \_ \_ terminée**.

Pour plus d’informations sur l’utilisation de cette méthode, voir [How to use the connexion Bureau à distance Broker client API](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





