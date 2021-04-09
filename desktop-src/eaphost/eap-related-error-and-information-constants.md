---
title: Constantes d’informations et d’erreurs liées à EAP (Eaphosterror. h)
description: Groupes individuels de constantes d’informations et d’erreurs liées à EAP communes à toutes les technologies d’API EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032950"
---
# <a name="eap-related-error-and-information-constants"></a>Constantes d’informations et d’erreurs liées à EAP

Groupes individuels de constantes d’informations et d’erreurs liées à EAP communes à toutes les technologies d’API EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST en \_ premier**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur associée à EAPHost se produira entre **EAP \_ e \_ EAPHost en \_ premier** et **EAP \_ e \_ EAPHost en \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST en \_ dernier** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur associée à EAPHost se produira entre **EAP \_ e \_ EAPHost en \_ premier** et **EAP \_ e \_ EAPHost en \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST en \_ premier** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Définit la limite des rapports d’informations ; tout enregistrement d’événement d’information lié à EAPHost aura lieu entre le **\_ \_ \_ premier** et **le \_ \_ \_ dernier EAP i EAPHost**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHOST en \_ dernier**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Définit la limite des rapports d’informations ; tout enregistrement d’événement d’information lié à EAPHost aura lieu entre le **\_ \_ \_ premier** et **le \_ \_ \_ dernier EAP i EAPHost**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_magasin de certificats EAP E \_ \_ \_ inaccessible**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Ni l’authentificateur, ni l’homologue ne peuvent accéder au magasin de certificats.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_ \_ méthode EAPHost E \_ EAPHost \_ non \_ installée**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



La méthode EAP demandée n’est pas installée.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**réinitialisation de l’hôte de la \_ \_ \_ \_ méthode THIRDPARTY \_ EAP E EAPHOST \_**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



L’hôte de la méthode tierce ne répond pas et a été redémarré automatiquement.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ E \_ EAPHOST \_ EAPQEC \_ inaccessible**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost n’est pas en mesure de communiquer avec le [client de contrainte de mise en quarantaine](/windows/desktop/NAP/nap-client-architecture) EAP (QEC) sur un client de protection d' [accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP) compatible.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_identité EAP \_ E \_ EAPHOST \_ inconnue**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost retourne cette erreur si l’authentificateur ne parvient pas à s’authentifier après l’envoi de l’identité d’homologue.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_échec de \_ l’authentification EAP E \_**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost retourne cette erreur en cas d’échec de l’authentification.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_échec de \_ la \_ \_ négociation EAP \_ du protocole EAP I EAPHOST**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost enregistre cet événement d’informations lorsque le client et le serveur ne sont pas configurés avec des types EAP compatibles.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ paquet non valide pour la méthode EAPHost EAP E \_**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Une méthode EAP a reçu un paquet EAP qui ne peut pas être traité. Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide EAP E EAPHOST** est un paquet non valide de la **\_ méthode EAP \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_ \_ \_ \_ paquet non valide distant EAP E EAPHOST \_**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost a reçu un paquet qui ne peut pas être traité. Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide distant EAP E EAPHOST** est le **\_ \_ paquet EAP non valide**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**\_ \_ XML EAPHost non \_ \_ conforme** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Échec de la validation du schéma de configuration EAPHost.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**la \_ configuration de la méthode EAP E \_ \_ \_ ne \_ \_ prend pas en charge l' \_ authentification unique**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 ou version ultérieure : la méthode EAP ne prend pas en charge l’authentification unique (SSO) pour la configuration fournie.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_opération de \_ méthode EAPHOST EAP E \_ \_ \_ non \_ prise en charge**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost retourne cette erreur lorsqu’une méthode EAP configurée ne prend pas en charge une opération demandée (appel de procédure).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_utilisateur EAP \_ E \_ First**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée à l’utilisateur se produira entre l’utilisateur **EAP \_ e \_ User \_ First** et l' **\_ utilisateur EAP e \_ \_ Last**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**\_utilisateur EAP \_ E \_ Last** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée à l’utilisateur se produira entre l’utilisateur **EAP \_ e \_ User \_ First** et l' **\_ utilisateur EAP e \_ \_ Last**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**d' \_ \_ abord l’utilisateur I EAP \_**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Définit la limite des rapports d’informations ; toute journalisation des événements d’information liée à EAP se produira entre le **\_ \_ \_ premier utilisateur EAP i** et l' **\_ utilisateur i EAP en \_ \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_utilisateur I EAP en \_ \_ dernier**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Définit la limite des rapports d’informations ; toute journalisation des événements d’information liée à EAP se produira entre le **\_ \_ \_ premier utilisateur EAP i** et l' **\_ utilisateur i EAP en \_ \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_ \_ certificat utilisateur EAP \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost n’a pas pu trouver de certificat d’utilisateur pour l’authentification.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**\_ \_ certificat utilisateur EAP \_ E \_ non valide**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



Le certificat utilisateur pour lequel l’authentification n’est pas définie n’a pas l’utilisation de clé étendue (EKU) appropriée.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**le \_ \_ certificat utilisateur EAP E \_ \_ a expiré**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost a trouvé un certificat utilisateur arrivé à expiration.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**\_ \_ certificat utilisateur EAP \_ E \_ révoqué**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Le certificat utilisateur utilisé pour l’authentification a été révoqué.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_ \_ \_ \_ autre erreur du certificat utilisateur EAP E \_**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Une erreur inconnue s’est produite lors de l’utilisation de la certification d’utilisateur pour l’authentification.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_ \_ certificat utilisateur EAP \_ E \_ rejeté** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



L’authentificateur a rejeté la certification de l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_ \_ \_ \_ autre erreur du compte d’utilisateur EAP I \_**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Une erreur EAP a été reçue après un échange d’identité, indiquant la probabilité d’un problème avec le compte d’utilisateur d’authentification.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_ \_ informations d’identification de l’utilisateur EAP E \_ \_ rejetées**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



L’authentificateur a rejeté les informations d’identification de l’utilisateur pour l’authentification.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**\_ \_ \_ mot de passe du nom d’utilisateur E EAP \_ \_ rejeté**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 ou version ultérieure : échec de l’authentification. L’authentificateur a rejeté les informations d’identification de l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ pas \_ de \_ lecteur de carte à puce \_**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 ou version ultérieure : aucun lecteur de carte à puce n’a été trouvé.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**\_serveur EAP \_ E \_ First**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée au serveur se produit entre le **\_ serveur EAP e \_ \_** et le serveur **e EAP en \_ \_ \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_dernier E \_ serveur \_ EAP**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée au serveur se produit entre le **\_ serveur EAP e \_ \_** et le serveur **e EAP en \_ \_ \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_certificat de serveur EAP E \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost n’a pas pu trouver le certificat de serveur pour l’authentification.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_certificat du serveur EAP E \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



Le certificat de serveur qui est l’utilisateur pour l’authentification ne dispose pas d’un ensemble d’utilisation de clé étendue (EKU) approprié.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**le \_ certificat du serveur EAP E \_ \_ \_ a expiré**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost a trouvé un certificat de serveur expiré.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_certificat de \_ serveur EAP E \_ \_ révoqué**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Le certificat de serveur utilisé pour l’authentification a été révoqué.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_ \_ \_ \_ autre erreur de certificat de serveur EAP E \_**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Une erreur inconnue s’est produite avec le certificat de serveur.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ certificat racine d’utilisateur EAP E \_ \_ \_ First**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée au certificat racine de l’utilisateur se produit entre le **\_ \_ \_ \_ \_ premier** et le certificat racine de l' **utilisateur EAP e \_ \_ \_ \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ \_ \_ dernier certificat racine d’utilisateur EAP E \_**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée au certificat racine de l’utilisateur se produit entre le **\_ \_ \_ \_ \_ premier** et le certificat racine de l' **utilisateur EAP e \_ \_ \_ \_ \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ certificat racine utilisateur EAP E \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost n’a pas pu trouver de certificat dans un magasin de certificats racines de confiance pour la validation de la certification utilisateur.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_ \_ certificat racine utilisateur EAP E \_ \_ \_ non valide**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



L’authentification a échoué car le certificat racine utilisé pour ce réseau n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**le \_ certificat racine de l’utilisateur EAP E \_ \_ \_ \_ a expiré**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



Le certificat racine approuvé requis pour la validation du certificat de l’utilisateur a expiré.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ certificat racine du serveur EAP E \_ \_ \_ First**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée à un certificat racine du serveur se produit entre le certificat **\_ racine du serveur EAP e \_ \_ \_ \_** et le certificat racine du **\_ \_ serveur \_ \_ \_ EAP** e d’abord.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ \_ dernier certificat racine du serveur EAP E \_**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur liée à un certificat racine du serveur se produit entre le certificat **\_ racine du serveur EAP e \_ \_ \_ \_** et le certificat racine du **\_ \_ serveur \_ \_ \_ EAP** e d’abord.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ certificat racine du serveur EAP E \_ \_ \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost n’a pas pu trouver de certificat racine dans un magasin de certificats racines de confiance pour la validation de la certification du serveur.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificat racine du serveur EAP E \_ \_ \_ non valide** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



L’authentification a échoué car le certificat de serveur requis pour ce réseau sur l’ordinateur serveur n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_nom du \_ certificat racine du serveur EAP E \_ \_ \_ \_ requis**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



L’authentification a échoué car le certificat sur l’ordinateur serveur n’a pas de nom de serveur spécifié.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Il existe d’autres noms pour certaines erreurs :

-   Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide EAP E EAPHOST** est un paquet non valide de la **\_ méthode EAP \_ \_**.
-   Un autre nom pour le **\_ \_ \_ \_ \_ paquet non valide distant EAP E EAPHOST** est le **\_ \_ paquet EAP non valide**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes EAPHost communes](common-eap-host-error-constants.md)
</dt> </dl>

 

