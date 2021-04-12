---
title: Indicateurs de méthode EAP (Eaptypes. h)
description: Les indicateurs de méthode EAP sont utilisés dans les fonctions du demandeur, de l’authentificateur et de l’homologue pour spécifier les comportements d’une session d’authentification EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464178"
---
# <a name="eap-method-flags"></a>Indicateurs de méthode EAP

Les indicateurs de méthode EAP sont utilisés dans les fonctions du demandeur, de l’authentificateur et de l’homologue pour spécifier les comportements d’une session d’authentification EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Indicateur EAP \_ Reserved1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_indicateur EAP \_ non \_ interactif**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



N’affiche pas d’interface utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**connexion de l' \_ indicateur EAP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Les données utilisateur ont été obtenues à partir de l’ouverture de session Windows.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**Aperçu de l' \_ indicateur EAP \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Affiche l’interface utilisateur des informations d’identification avant l’authentification, même si des informations d’identification mises en cache sont présentes.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**Protocole EAP \_ INDICATEUR \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**authentification de machine de l' \_ indicateur EAP \_ \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Utiliser l’authentification au niveau de l’ordinateur ; Si vous ne définissez pas cet indicateur, l’authentification au niveau de l’utilisateur est utilisée.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_indicateur EAP \_ \_ accès invité**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Indique une demande de fourniture d’un accès invité.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Indicateur EAP \_ Reserved3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**Protocole EAP \_ INDICATEUR \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_ \_ reprise de la \_ \_ mise en veille de l’indicateur EAP**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Indique qu’il s’agit du premier appel après la reprise de l’activité de l’ordinateur à partir d’une période de mise en veille prolongée.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**Protocole EAP \_ INDICATEUR \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Indicateur EAP \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ authentification complète de l’indicateur EAP \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Indique que les méthodes de tunnel doivent effectuer une authentification complète au lieu d’une version abrégée, telle que la [reconnexion rapide PEAP (Protected EAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**l' \_ indicateur EAP \_ préfère les \_ \_ informations d’identification Alt**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indique que les informations d’identification passées dans [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) sont préférées à toutes les autres formes de récupération des informations d’identification, même si les données de configuration transmises à la fonction actuelle demandent un mode de récupération des informations d’identification différent.

> [!Note]  
> Cet indicateur est utilisé uniquement par [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Indicateur EAP \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**changement d’état d’intégrité de l' \_ indicateur d’homologue EAP \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Indique que la nouvelle authentification est un rappel de [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP); La protection d’accès réseau a initié la session d’authentification car l’état d’intégrité a changé. Cet indicateur doit être envoyé uniquement lorsque cette fonction est appelée par un rappel [*NotificationHandler*](/previous-versions/windows/desktop/api) spécifique à la protection d’accès réseau fourni par un appel précédent à cette fonction.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_ \_ \_ interface utilisateur supprimer l’indicateur EAP**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Continuer l’authentification avec les informations disponibles. Si l’authentification ne peut pas se poursuivre, échoue.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_pré- \_ ouverture de \_ session de l’indicateur EAP**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indique qu’EAPHost doit fournir une authentification unique (SSO). Pour plus d’informations, consultez [SSO et PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**authentification de l’utilisateur de l' \_ indicateur EAP \_ \_**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indique l’authentification au niveau de l’utilisateur pour les méthodes héritées qui ne peuvent pas définir l’authentification de l' **\_ \_ ordinateur \_ indicateur EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_indicateur EAP \_ CONFG \_ ReadOnly**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Indique que la configuration peut être affichée mais pas mise à jour.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Indicateur EAP \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Ne pas utiliser. Réservé pour un usage futur.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes EAPHost communes](common-eap-host-error-constants.md)
</dt> </dl>

