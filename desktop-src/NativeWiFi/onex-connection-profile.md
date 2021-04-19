---
description: Contient des informations sur le profil de connexion 802.1 X actuellement utilisé pour l’authentification 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Structure ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543700"
---
# <a name="onex_connection_profile-structure"></a>Structure du profil de \_ connexion Onex \_

La structure du **\_ \_ profil de connexion Onex** contient des informations sur le profil de connexion 802.1 x actuellement utilisé pour l’authentification 802.1 x.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwVersion**
</dt> <dd>

Version de cette structure **de \_ \_ profil de connexion Onex** .

</dd> <dt>

**dwTotalLen**
</dt> <dd>

Longueur, en octets, de cette structure **de \_ \_ profil de connexion Onex** .

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwOneXSupplicantFlags** .

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **supplicantMode** .

</dd> <dt>

**fauthMode**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **authmode** .

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwHeldPeriod** .

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwAuthPeriod** .

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwStartPeriod** .

</dd> <dt>

**fMaxStart**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwMaxStart** .

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwMaxAuthFailures** .

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwNetworkAuthTimeout** .

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **bAllowLogonDialogs** .

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwNetworkAuthWithUITimeout** .

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **bUserBasedVLan** .

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

Ensemble d’indicateurs 802.1 X qui peuvent être présents dans le profil. Ces indicateurs sont réservés à un usage interne par le module d’authentification 802.1 X.

</dd> <dt>

**supplicantMode**
</dt> <dd>

Élément supplicantMode dans le schéma 802.1 X qui spécifie la méthode de transmission utilisée pour EAPOL-Start messages. Pour plus d’informations, consultez l' [**élément supplicantMode (Onex)**](onexschema-supplicantmode-onex-element.md) dans le schéma 802.1 x.



| Valeur                                                                                                                                                                                                                                                                                                                                               | Signification                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | Les messages de EAPOL-Start ne sont pas transmis. Valide pour les profils LAN câblés uniquement.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | Le client détermine quand envoyer des paquets EAPOL-Start en fonction de la capacité du réseau. Les messages de EAPOL-Start sont envoyés uniquement lorsque cela est nécessaire. Valide pour les profils LAN câblés uniquement.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start messages sont transmis comme spécifié par 802.1 X. Valide pour les profils de réseau local câblés et sans fil.<br/>                                                             |



 

</dd> <dt>

**authMode**
</dt> <dd>

Élément authMode dans le schéma 802.1 X qui spécifie le type d’informations d’identification utilisé pour l’authentification 802.1 X. Pour plus d’informations, consultez l' [**élément authmode (Onex)**](onexschema-authmode-onex-element.md) dans le schéma 802.1 x.



| Valeur                                                                                                                                                                                                                                                                                               | Signification                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Utilisez les informations d’identification de l’ordinateur ou de l’utilisateur. Lorsqu’un utilisateur a ouvert une session, les informations d’identification de l’utilisateur sont utilisées pour l’authentification. Quand aucun utilisateur n’est connecté, les informations d’identification de l’ordinateur sont utilisées.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Utiliser uniquement les informations d’identification de l’ordinateur.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Utiliser uniquement les informations d’identification de l’utilisateur.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Utilisez uniquement les informations d’identification invité (vide).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | Les informations d’identification à utiliser ne sont pas spécifiées.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

Élément heldPeriod dans le schéma 802.1 X qui spécifie la durée, en secondes, pendant laquelle un client ne tentera pas une nouvelle tentative d’authentification après l’échec d’une tentative d’authentification. Pour plus d’informations, consultez l' [**élément heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) dans le schéma 802.1 x.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

Élément authPeriod dans le schéma 802.1 X qui spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur. Si aucune réponse n’est reçue pendant la période spécifiée, le client part du principe qu’aucun authentificateur n’est présent sur le réseau. Pour plus d’informations, consultez l' [**élément authPeriod (Onex)**](onexschema-authperiod-onex-element.md) dans le schéma 802.1 x.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

Élément startPeriod dans le schéma 802.1 X qui spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start. Un message de EAPOL-Start est envoyé pour démarrer le processus d’authentification 802.1 X. Pour plus d’informations, consultez l' [**élément startPeriod (Onex)**](onexschema-startperiod-onex-element.md) dans le schéma 802.1 x.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

Élément maxStart dans le schéma 802.1 X qui spécifie le nombre maximal de messages EAPOL-Start envoyés. Une fois que le nombre maximal de messages de EAPOL-Start a été envoyé, le client suppose qu’il n’y a aucun authentificateur présent sur le réseau. Pour plus d’informations, consultez l' [**élément Maxstart (Onex)**](onexschema-maxstart-onex-element.md) dans le schéma 802.1 x.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

Élément maxAuthFailures dans le schéma 802.1 X qui spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification. Pour plus d’informations, consultez l’élément [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) dans le schéma 802.1 x.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

Durée, en secondes, d’attente de l’achèvement de l’authentification 802.1 X avant le démarrage de l’ouverture de session normale. Cette valeur est utilisée dans les scénarios d’authentification unique (SSO). Cette valeur est par défaut de 10 secondes dans un profil 802.1 X. Pour plus d’informations, consultez l' [**élément maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) dans le schéma 802.1 x.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

Durée maximale, en secondes, d’attente d’une connexion au cas où une boîte de dialogue d’interface utilisateur nécessitant une entrée utilisateur s’affiche pendant l’authentification unique par ouverture de session.

Sur Windows Vista avec SP1 et versions ultérieures, cette valeur est codée en dur à 10 minutes et n’est pas configurable. Sur Windows Vista en production, cette valeur est définie par défaut sur 60 secondes dans un profil 802.1 X et est contrôlée par l’élément **maxDelayWithAdditionalDialogs** dans le schéma.

Sur Windows Vista avec SP1 et versions ultérieures, l’élément **maxDelayWithAdditionalDialogs** dans le schéma 802.1 x est ignoré et déconseillé.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Valeur qui spécifie s’il faut autoriser l’affichage de boîtes de dialogue EAP lors de l’utilisation de l’authentification unique préalable à l’ouverture de session. Pour plus d’informations, consultez l’élément **allowAdditionalDialogs** dans le schéma 802.1 x.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

Élément userBasedVirtualLan dans le schéma 802.1 X qui spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur. Certains périphériques NAS (Network Access Server) modifient le réseau local virtuel après l’authentification d’un utilisateur. Quand userBasedVirtualLan a la valeur TRUE, le NAS peut modifier le réseau local virtuel d’un appareil après l’authentification d’un utilisateur. Pour plus d’informations, consultez l' [**élément userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) dans le schéma 802.1 x.

</dd> </dl>

## <a name="remarks"></a>Notes

La structure du **\_ \_ profil de connexion Onex** est utilisée par le module 802.1 x, un nouveau composant de configuration sans fil pris en charge sur Windows Vista et versions ultérieures.

Les [**\_ données de \_ mise \_ à jour du résultat Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contiennent des informations sur un changement d’état de l’authentification 802.1 x. La structure de **\_ \_ \_ données de mise à jour du résultat Onex** est retournée lorsque le membre **NotificationSource** de la structure de [**\_ \_ données de notification WLAN**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) est **\_ source de notification \_ \_ WLAN** et que le membre **NotificationCode** de la structure de **\_ \_ données de notification WLAN** pour la notification reçue est **OneXNotificationTypeResultUpdate**. Pour cette notification, le membre **pData** de la structure de **\_ \_ données de notification WLAN** pointe vers une structure de **\_ \_ \_ données de mise à jour de résultat Onex** qui contient des informations sur le changement d’état d’authentification 802.1 x.

Si le membre **fOneXAuthParams** dans la structure de [**\_ \_ \_ données de mise à jour du résultat Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) est défini, le membre **authParams** de la structure de **\_ \_ \_ données de mise à jour du résultat Onex** contient une structure d' [**\_ \_ objet blob de variable Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) avec une structure de [**\_ \_ paramètres d’authentification Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) incorporée à partir du membre **dwOffset** de l' **\_ \_ objet blob de variable Onex**. Le **membre oneXConnProfile** de la structure de **\_ \_ paramètres d’authentification Onex** contient une structure d' **\_ \_ objet blob de variable Onex** avec une structure de **\_ \_ profil de connexion Onex** incorporée à partir du membre **dwOffset** de l' **\_ \_ objet blob de variable Onex**.

La structure du **\_ \_ profil de connexion Onex** n’est pas définie dans un fichier d’en-tête public.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos de l’architecture ACM](about-the-acm-architecture.md)
</dt> <dt>

[Schéma OneX](onexschema-schema.md)
</dt> <dt>

[**Élément authMode (OneX)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**Élément authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**Élément heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**Élément maxStart (OneX)**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**Élément startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**Élément supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**Élément userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**\_paramètres d’authentification Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**\_type de notification Onex \_**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**\_données de \_ mise à jour du résultat Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**Élément de schéma OneX**](onexschema-onex-element.md)
</dt> <dt>

[**\_blob de variable Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**\_données de notification WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
