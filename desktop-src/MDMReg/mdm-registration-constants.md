---
title: Valeurs d’erreur d’inscription MDM (MDMRegistration. h)
description: Les valeurs d’erreur suivantes sont fournies avec l’inscription MDM.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb62977a48400866e9fa8829696c884e58e54325
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548984"
---
# <a name="mdm-registration-error-values"></a>Valeurs d’erreur d’inscription MDM

Les valeurs d’erreur suivantes sont fournies avec l’inscription MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**incompatibilité de \_ type de données E \_**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



Le type de données ne correspond pas au type de données attendu.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**\_erreur de \_ \_ format de \_ message \_ de l’appareil MREGISTER E**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Schéma non valide, erreur de format de message du serveur.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**\_erreur de \_ \_ format de \_ message \_ de l’appareil MENROLL E**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Schéma non valide, erreur de format de message du serveur.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**\_ \_ \_ erreur d’authentification de l’appareil MREGISTER E \_**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Le serveur n’a pas pu authentifier l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**\_ \_ \_ erreur d’authentification de l’appareil MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Le serveur n’a pas pu authentifier l’utilisateur.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**\_ \_ \_ erreur d’autorisation d’appareil MREGISTER E \_**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



L’utilisateur n’est pas autorisé à s’inscrire.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**\_ \_ \_ erreur d’autorisation d’appareil MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



L’utilisateur n’est pas autorisé à s’inscrire.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**\_erreur de \_ CERTIFCATEREQUEST d’appareil MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



L’utilisateur n’a pas d’autorisation pour le modèle de certificat ou l’autorité de certification est inaccessible.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**\_erreur de \_ CERTIFCATEREQUEST d’appareil MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



L’utilisateur n’a pas d’autorisation pour le modèle de certificat ou l’autorité de certification est inaccessible.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**\_erreur de \_ CONFIGMGRSERVER d’appareil MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Une défaillance s’est produite au niveau du serveur d’administration, par exemple une erreur d’accès à la base de données.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_erreur de \_ CONFIGMGRSERVER d’appareil MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Une défaillance s’est produite au niveau du serveur d’administration, par exemple une erreur d’accès à la base de données.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**\_erreur de \_ INTERNALSERVICE d’appareil MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Une exception non gérée s’est produite sur le serveur.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**\_erreur de \_ INTERNALSERVICE d’appareil MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Une exception non gérée s’est produite sur le serveur.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**\_erreur de \_ INVALIDSECURITY d’appareil MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Une exception non gérée s’est produite sur le serveur.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**\_erreur de \_ INVALIDSECURITY d’appareil MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Une exception non gérée s’est produite sur le serveur.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ \_ erreur inconnue de l’appareil MREGISTER E \_**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Erreur de serveur inconnue.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ \_ erreur inconnue de l’appareil MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Erreur de serveur inconnue.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**\_inscription MREGISTER \_ E \_ en \_ cours**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



Une autre opération d’inscription est en cours d’exécution.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**\_inscription MENROLL E \_ \_ en \_ cours**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



Une autre opération d’inscription est en cours d’exécution.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**\_appareil MREGISTER \_ E \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



N'est plus utilisé.

**Windows 8.1 :** L’appareil est déjà inscrit.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**\_appareil MENROLL \_ E \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



L’appareil est déjà inscrit.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**\_appareil MREGISTER \_ E \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



N'est plus utilisé.

**Windows 8.1 :** L’appareil n’est pas inscrit.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**\_appareil MENROLL \_ E \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



L’appareil n’est pas inscrit.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER \_ E \_ \_ redirection de la détection**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



N'est plus utilisé.

**Windows 8.1 :** La redirection est nécessaire.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**erreur d’inscription de l' \_ appareil MREGISTER E \_ \_ non \_ Active Directory \_ \_**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



N'est plus utilisé.

**Windows 8.1 :** L’appareil n’est pas inscrit auprès de Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**MENROLL \_ E \_ détection \_ s \_ Date de certificat \_ \_ non valide**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Pendant la découverte, la date de certificat sec n’est pas valide.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**échec de la \_ découverte MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



N'est plus utilisé.

**Windows 8.1 :** Échec de la découverte. la redirection est nécessaire.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**\_ \_ mot de passe MENROLL E \_ requis**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



Un mot de passe est nécessaire, mais n’a pas été fourni.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**\_erreur MENROLL E \_ wab \_**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Une erreur s’est produite lors de l’inscription WAB.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**\_connectivité MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Une erreur réseau s’est produite, telle que DNS ou un délai d’attente réseau.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**l' \_ inscription de MENROLL S est \_ \_ suspendue**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



L’inscription a été suspendue. N'est plus pris en charge.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL \_ E \_ INVALIDSSLCERT**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



Le certificat SSL n’est pas valide.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



L’utilisateur a déjà inscrit un trop grand nombre d’appareils. Supprimez ou annulez l’inscription des anciens pour résoudre cette erreur. Notez que l’utilisateur peut résoudre cette erreur sans assistance administrative.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180014
</dt> <dt>



Une plateforme spécifique (par exemple, Windows) ou une version n’est pas prise en charge. Le correctif général de cette erreur est la mise à niveau de l’appareil.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



La gestion des périphériques mobiles n’est généralement pas prise en charge pour cet appareil : l’utilisateur peut appeler l’administrateur, mais il sera peu probable de résoudre ce problème.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



L’appareil essaie de renouveler, mais le serveur a rejeté la demande. Vérifiez l’heure sur l’appareil. L’utilisateur peut être en mesure de résoudre cette erreur en réinscrivant.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ inmaintenance**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



Le compte est en cours de maintenance ; réessayez plus tard. L’utilisateur peut réessayer ultérieurement. Toutefois, l’utilisateur peut choisir d’appeler l’administrateur pour déterminer la planification de la maintenance.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



La licence de l’utilisateur est dans une inscription de blocage d’État incorrecte ; l’utilisateur doit appeler l’administrateur.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



Le serveur a rejeté les données d’inscription ; le serveur n’est peut-être pas configuré correctement.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



Le serveur a demandé le protocole HTTP au lieu de HTTPs, mais il n’a pas été accepté.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**\_ \_ \_ état incorrect de la plateforme MENROLL E \_**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Une opération non valide a été tentée, par exemple en tentant d’inscrire le même appareil deux fois ou d’annuler l’inscription d’un périphérique inconnu.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**erreur de licence de la \_ plateforme MENROLL E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



La version de Windows installée sur le client ne prend pas en charge ce type d’inscription.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**\_ \_ \_ erreur inconnue de la plateforme MENROLL E \_**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Une erreur inconnue s’est produite sur le client.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ \_ CERTSTORE CSP Proven \_**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Échec de l’approvisionnement dans le CSP du magasin de certificats.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ \_ CSP \_**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Échec de l’approvisionnement dans un RPC W7/DMAcc.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ \_ DMCLIENT CSP Proven \_**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Échec de l’approvisionnement dans un CSP client DM.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ \_ PFW CSP Proven \_**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Échec de l’approvisionnement dans un CSP Passport for Work.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ provation Proven \_ \_ misc**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Échec de l’approvisionnement dans un CSP non listé ci-dessus.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ prove \_ inconnu**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Échec de l’approvisionnement, mais aucun CSP spécifique n’est indiqué.

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ Prov \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Lors de la tentative de liaison du certificat public/de la clé privée, le certificat public n’a pas été trouvé : lors de la tentative de liaison du certificat public/de la clé privée, ou lors de la recherche de la charge utile d’approvisionnement (peut-être en ciblant le mauvais magasin).

**Windows 8.1 :** Cette constante n’est pas disponible avant Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ \_ APPMGMT CSP Proven \_**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Échec de l’approvisionnement dans le CSP EnterpriseAppManagement.

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**\_gestion des appareils MENROLL E \_ \_ \_ bloquée**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



La gestion des appareils mobiles (MDM) a été bloquée, peut-être par stratégie de groupe ou la fonction [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**échec de MENROLL \_ \_ CERTPOLICY \_ PRIVATEKEYCREATION \_**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Échec de la création de la clé privée.

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH \_ n’a pas pu \_ \_ trouver le \_ certificat**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



L’authentification par certificat a été demandée, mais a échoué lors de la recherche d’un certificat à utiliser.

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ \_ message vide**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



Le serveur a répondu avec HTTP 200, mais le message était vide.

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**annulation de l' \_ utilisateur MENROLL E \_ \_** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



L’utilisateur a annulé l’opération.

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL \_ E \_ MDM \_ non \_ configuré**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



La gestion des appareils mobiles (MDM) n’est pas configurée.

> [!Note]  
> Cette constante n’est pas disponible avant Windows 10, version 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                    |
| En-tête<br/>                   | <dl> <dt>MDMRegistration. h</dt> </dl> |



 

 





