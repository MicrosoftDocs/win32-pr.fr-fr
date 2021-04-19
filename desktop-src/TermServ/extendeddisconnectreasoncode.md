---
title: Énumération ExtendedDisconnectReasonCode
description: Définit des informations étendues sur la raison de la déconnexion du contrôle.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ExtendedDisconnectReasonCode
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511592"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a>Énumération ExtendedDisconnectReasonCode

Définit des informations étendues sur la raison de la déconnexion du contrôle.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**
</dt> <dd>

Aucune information supplémentaire n'est disponible.

</dd> <dt>

<span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**
</dt> <dd>

Une application a initié la déconnexion.

</dd> <dt>

<span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**
</dt> <dd>

Une application a été déconnectée du client.

</dd> <dt>

<span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**
</dt> <dd>

Le serveur a déconnecté le client car le client a été inactif pendant une période plus longue que le délai d’attente désigné.

</dd> <dt>

<span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**
</dt> <dd>

Le serveur a déconnecté le client car le client a dépassé la période indiquée pour la connexion.

</dd> <dt>

<span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**
</dt> <dd>

La connexion du client a été remplacée par une autre connexion.

</dd> <dt>

<span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**
</dt> <dd>

Aucune mémoire n’est disponible.

</dd> <dt>

<span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**
</dt> <dd>

Le serveur a refusé la connexion.

</dd> <dt>

<span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**
</dt> <dd>

Le serveur a refusé la connexion pour des raisons de sécurité.

</dd> <dt>

<span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**
</dt> <dd>

Le serveur a refusé la connexion pour des raisons de sécurité.

</dd> <dt>

<span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**
</dt> <dd>

Les nouvelles informations d’identification sont requises.

</dd> <dt>

<span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**
</dt> <dd>

L’activité de l’utilisateur a initié la déconnexion.

</dd> <dt>

<span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**
</dt> <dd>

L’utilisateur se déconnecte, déconnecter la session.

</dd> <dt>

<span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**
</dt> <dd>

Erreur de licence interne.

</dd> <dt>

<span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**
</dt> <dd>

Aucun serveur de licences n’était disponible.

</dd> <dt>

<span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**
</dt> <dd>

Aucune licence de logiciel valide n’était disponible.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**
</dt> <dd>

L’ordinateur distant a reçu un message de licence non valide.

</dd> <dt>

<span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**
</dt> <dd>

L’ID de matériel ne correspond pas à celui indiqué sur la licence logicielle.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**
</dt> <dd>

Erreur de licence client.

</dd> <dt>

<span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**
</dt> <dd>

Des problèmes réseau se sont produits pendant le protocole de licence.

</dd> <dt>

<span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**
</dt> <dd>

Le client a terminé le protocole de gestion de licences prématurément.

</dd> <dt>

<span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**
</dt> <dd>

Un message de licence a été chiffré de manière incorrecte.

</dd> <dt>

<span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**
</dt> <dd>

La licence d’accès client de l’ordinateur local n’a pas pu être mise à niveau ou renouvelée.

</dd> <dt>

<span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**
</dt> <dd>

L’ordinateur distant ne dispose pas d’une licence pour accepter les connexions à distance.

</dd> <dt>

<span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**
</dt> <dd>

Une erreur de refus d’accès a été reçue lors de la création d’une clé de Registre pour le magasin de licences.

</dd> <dt>

<span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**
</dt> <dd>

Des informations d’identification non valides ont été rencontrées.

</dd> <dt>

<span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**
</dt> <dd>

Début de la plage d’erreurs de protocole internes. Pour plus d’informations, consultez le journal des événements du serveur.

</dd> <dt>

<span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**
</dt> <dd>

Fin de la plage des erreurs de protocole internes.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





