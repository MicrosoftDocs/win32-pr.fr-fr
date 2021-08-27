---
title: Méthode IMsTscAxEvents OnDisconnected
description: Appelé lorsque le contrôle client a été déconnecté du serveur de l’hôte de session Bureau à distance (Bureau à distance).
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnDisconnected
- Méthode OnDisconnected Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnDisconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bc7351d1cc0fafa46aab1f93feed4cafc184dc33090d4d2c7947a285fbb234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125129"
---
# <a name="imstscaxeventsondisconnected-method"></a>IMsTscAxEvents :: OnDisconnected, méthode

Appelé lorsque le contrôle client a été déconnecté du serveur de l’hôte de session Bureau à distance (Bureau à distance).

## <a name="syntax"></a>Syntaxe


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*discReason* \[ dans\]
</dt> <dd>

Spécifie la raison de la déconnexion. La liste suivante répertorie les codes d’erreur. Certains de ces codes d’erreur sont définis dans Wincred. h.

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))


</dt> <dd>

Socket fermé.

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))


</dt> <dd>

Déconnexion distante par le serveur. Il ne s’agit pas d’un code d’erreur.

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))


</dt> <dd>

Erreur de décompression.

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))


</dt> <dd>

Délai de connexion dépassé.

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))


</dt> <dd>

Erreur de déchiffrement.

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))


</dt> <dd>

Échec de la recherche de nom DNS.

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))


</dt> <dd>

Échec de la recherche DNS.

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))


</dt> <dd>

Erreur de chiffrement.

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))


</dt> <dd>

Windows Échec de l’appel [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) des sockets.

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))


</dt> <dd>

Erreur de l’hôte introuvable.

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))


</dt> <dd>

Erreur interne.

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))


</dt> <dd>

Erreur de sécurité interne.

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))


</dt> <dd>

Erreur de sécurité interne.

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))


</dt> <dd>

La méthode de chiffrement spécifiée n’est pas valide.

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))


</dt> <dd>

Adresse IP incorrecte spécifiée.

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))


</dt> <dd>

Les données de sécurité du serveur ne sont pas valides.

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))


</dt> <dd>

Les données de sécurité ne sont pas valides.

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))


</dt> <dd>

L’adresse IP spécifiée n’est pas valide.

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))


</dt> <dd>

Échec de la négociation de la licence.

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))


</dt> <dd>

Délai d’expiration de la licence.

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))


</dt> <dd>

Déconnexion locale. Il ne s’agit pas d’un code d’erreur.

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))


</dt> <dd>

Aucune information n'est disponible.

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))


</dt> <dd>

Mémoire insuffisante.

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))


</dt> <dd>

Mémoire insuffisante.

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))


</dt> <dd>

Mémoire insuffisante.

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0X2))


</dt> <dd>

Déconnexion distante par l’utilisateur. Il ne s’agit pas d’un code d’erreur.

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))


</dt> <dd>

Échec de la décompression du certificat du serveur.

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))


</dt> <dd>

Windows Échec de la [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) des sockets.

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))


</dt> <dd>

Windows Échec de l’appel de [**réception**](/windows/desktop/api/winsock/nf-winsock-recv) des sockets.

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))


</dt> <dd>

Le délai d’attente a expiré.

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))


</dt> <dd>

Erreur de minuteur interne.

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))


</dt> <dd>

Windows Échec de l’appel d' [**envoi**](/windows/desktop/api/winsock2/nf-winsock2-send) de Sockets.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**Protocole SSL \_ \_Compte Err \_ désactivé** (2823 (0xB07))


</dt> <dd>

Le compte est désactivé.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**Protocole SSL \_ Compte d’erreur \_ \_ expiré** (3591 (0xE07))


</dt> <dd>

Le compte a expiré.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**Protocole SSL \_ Compte d’erreur \_ \_ verrouillé \_** (3335 (0xD07))


</dt> <dd>

Le compte est verrouillé.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**Protocole SSL \_ \_ \_ Restriction de compte ERR** (3079 (0xC07))


</dt> <dd>

Le compte est limité.

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**Protocole SSL \_ Le \_ certificat d’erreur \_ a expiré** (6919 (0x1B07))


</dt> <dd>

Le certificat reçu a expiré.

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**Protocole SSL \_ \_ \_ Stratégie de délégation d’erreur** (5639 (0x1607))


</dt> <dd>

La stratégie ne prend pas en charge la délégation des informations d’identification au serveur cible.

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**Protocole SSL \_ ERR \_ actualité \_ cred \_ requise \_ par le \_ serveur** (8455 (0x2107))


</dt> <dd>

La stratégie d’authentification serveur n’autorise pas les demandes de connexion à l’aide des informations d’identification enregistrées. L’utilisateur doit entrer de nouvelles informations d’identification.

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**Protocole SSL \_ \_ \_ Erreur d’ouverture de session** (2055 (0x807))


</dt> <dd>

Échec de la connexion.

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**Protocole SSL \_ ERR \_ aucune \_ \_ autorité d’authentification** (6151 (0x1807))


</dt> <dd>

Aucune autorité n’a pu être contactée pour l’authentification. Le nom de domaine du tiers d’authentification peut être incorrect, le domaine peut être inaccessible ou une relation d’approbation a peut-être échoué.

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**Protocole SSL \_ ERR \_ non de \_ ce type d' \_ utilisateur** (2567 (0xA07))


</dt> <dd>

L’utilisateur spécifié n’a pas de compte.

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**Protocole SSL \_ Le \_ mot de passe Err \_ a expiré** (3847 (0xF07))


</dt> <dd>

Le mot de passe a expiré.

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**Protocole SSL \_ Le \_ mot de passe Err \_ doit \_ changer** (4615 (0x1207))


</dt> <dd>

Le mot de passe de l’utilisateur doit être modifié avant d’ouvrir une session pour la première fois.

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**Protocole SSL \_ Stratégie d’erreur \_ \_ NTLM \_ uniquement** (5895 (0x1707))


</dt> <dd>

La délégation des informations d’identification au serveur cible n’est pas autorisée, sauf si l’authentification mutuelle a été effectuée.

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**Protocole SSL \_ \_Carte à puce Err \_ \_ bloquée** (8711 (0x2207))


</dt> <dd>

La carte à puce est bloquée.

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**Protocole SSL \_ \_ \_ \_ Code pin d’erreur de carte à puce erronée** (7175 (0x1C07))


</dt> <dd>

Un code confidentiel incorrect a été présenté à la carte à puce.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour récupérer une description de l’erreur de déconnexion, appelez la méthode [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) et transmettez-lui le paramètre *discReason* et la propriété [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) de l’interface [**IMsRdpClient**](imsrdpclient-interface.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

