---
description: Répertorie les fonctions de prise en charge fournies par le jeu d’outils de configuration de sécurité.
ms.assetid: 5a771014-1706-490f-8540-ec516652cb83
title: Fonctions de gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c17efd55b1dbb806295ac0a83763257ffcc97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867638"
---
# <a name="security-management-functions"></a>Fonctions de gestion de la sécurité

Cette section contient des rubriques sur les groupes de fonctions suivants :

-   [Fonctions de rappel des pièces jointes](#attachment-callback-functions)
-   [Fonctions du moteur d’attachement](#attachment-engine-functions)
-   [Fonctions de stratégie LSA](#lsa-policy-functions)
    -   [Fonctions de stratégie](#lsa-policy-functions)
    -   [Fonctions de compte](#account-functions)
    -   [Fonctions de domaine approuvé](#trusted-domain-functions)
    -   [Fonctions de données privées](#private-data-functions)
    -   [Fonctions diverses](#miscellaneous-functions)
-   [Fonctions du compte de service géré](#managed-service-account-functions)
-   [Fonctions de filtre de mot de passe](#password-filter-functions)
-   [Fonctions plus sécurisées](#safer-functions)

## <a name="attachment-callback-functions"></a>Fonctions de rappel des pièces jointes

Les fonctions de prise en charge suivantes sont fournies par le jeu d’outils de configuration de la sécurité et peuvent être utilisées par les composants logiciels enfichables d’extension et les moteurs d’attachement pour lire et écrire des données de configuration.



| Fonction de rappel                                         | Description                                                                                 |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_informations gratuites \_ sur PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_free_info)<br/>   | Utilisé pour libérer de la mémoire allouée par ces fonctions de prise en charge.<br/>                        |
| [**\_informations sur le journal PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_log_info)<br/>     | Utilisé pour enregistrer le message dans le fichier journal de configuration ou le fichier journal d’analyse.<br/>          |
| [**\_informations sur la requête PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)<br/> | Utilisé pour interroger les informations de configuration et d’analyse d’un service spécifique.<br/> |
| [**PFSCE \_ définir des \_ informations**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)<br/>     | Utilisé pour définir les informations de configuration et d’analyse pour un service spécifique.<br/>       |



 

## <a name="attachment-engine-functions"></a>Fonctions du moteur d’attachement



| Fonction                                                              | Description                                                                                                                                                                                       |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)<br/> | Implémenté par la DLL du moteur de pièce jointe. Le moteur de configuration de sécurité appelle cette fonction lorsque le système est analysé.<br/>                                                           |
| [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)<br/>   | Implémenté par la DLL du moteur de pièce jointe. Le moteur de configuration de sécurité appelle cette fonction lorsque le système est configuré.<br/>                                                         |
| [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)<br/>   | Implémenté par la DLL du moteur de pièce jointe. Le moteur de configuration de sécurité appelle cette fonction lorsqu’il reçoit une demande de mise à jour de configuration à partir de l’extension du composant logiciel enfichable pièce jointe.<br/> |



 

## <a name="lsa-policy-functions"></a>Fonctions de stratégie LSA

Les rubriques suivantes fournissent des informations de référence pour les fonctions de stratégie de l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA).



| Rubrique                               | Description                                                                                                                                                                                   |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fonctions de stratégie<br/>         | Fonctions de détails utilisées pour ouvrir l’objet de [**stratégie**](policy-object.md) locale et pour définir ou récupérer des informations de stratégie globale.<br/>                                                  |
| Fonctions de compte<br/>        | Fonctions de détails utilisées pour gérer les autorisations de compte et pour créer et supprimer des comptes d’utilisateur.<br/>                                                                                       |
| Fonctions de domaine approuvé<br/> | Fonctions de détails utilisées pour créer et supprimer des relations de domaine approuvées et pour définir et récupérer des informations sur ces domaines approuvés.<br/>                                          |
| Fonctions de données privées<br/>   | N’utilisez pas les fonctions de données privées LSA. Utilisez plutôt les fonctions [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .<br/> |
| Fonctions diverses<br/>  | Fonctions de détails non décrites ailleurs.<br/>                                                                                                                                         |



 

### <a name="policy-functions"></a>Fonctions de stratégie

Les fonctions suivantes énumèrent les comptes d’utilisateur et les domaines approuvés, reçoivent les notifications de modification de stratégie et recherchent les noms de compte et les SID.



| Fonction                                                                                          | Description                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright)<br/>         | Énumère tous les comptes qui disposent d’une autorisation utilisateur spécifiée.<br/>                                                                                                                                                                                                                                                                         |
| [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/>                   | Énumère les domaines approuvés.<br/>                                                                                                                                                                                                                                                                                                            |
| [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames)<br/>                                               | Mappe les noms spécifiés à leurs SID. Retourne le SID sous la forme d’une paire RID/SID de domaine.<br/>                                                                                                                                                                                                                                                         |
| [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2)<br/>                                             | Mappe les noms spécifiés à leurs SID. Retourne le SID sous la forme d’un élément unique.<br/>                                                                                                                                                                                                                                                               |
| [**LsaLookupPrivilegeValue**](/windows/desktop/api/ntlsa/nf-ntlsa-lsalookupprivilegevalue)<br/>                             | Récupère l' [*identificateur unique*](/windows/desktop/SecGloss/l-gly) local (LUID) utilisé par l’autorité de [*sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) pour représenter le nom de privilège spécifié.<br/> |
| [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids)<br/>                                                 | Mappe les noms de compte spécifiés à leurs SID.<br/>                                                                                                                                                                                                                                                                                            |
| [**LsaRegisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaregisterpolicychangenotification)<br/>     | Inscrit un objet d’événement pour recevoir des notifications lors de la modification des informations de stratégie locale.<br/>                                                                                                                                                                                                                                              |
| [**LsaUnregisterPolicyChangeNotification**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaunregisterpolicychangenotification)<br/> | Annule l’inscription d’un objet d’événement qui reçoit des notifications de modification de stratégie.<br/>                                                                                                                                                                                                                                                                 |



 

### <a name="account-functions"></a>Fonctions de compte

Les fonctions suivantes permettent d’ajouter, d’énumérer et de supprimer des autorisations pour un compte.



| Fonction                                                                  | Description                                                                                                  |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights)<br/>             | Ajouter des autorisations à un compte. Si le compte n’existe pas encore, il est créé.<br/>              |
| [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights)<br/> | Énumérer les autorisations accordées à un compte.<br/>                                                  |
| [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights)<br/>       | Supprimer les autorisations d’un compte. Lorsque toutes les autorisations sont supprimées, le compte est supprimé.<br/> |



 

### <a name="trusted-domain-functions"></a>Fonctions de domaine approuvé

Les fonctions suivantes permettent de créer, d’énumérer et de supprimer des domaines approuvés, ainsi que de définir et de récupérer des informations de domaine approuvé.



| Fonction                                                                                                                                                    | Description                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex)<br/>                                                                                     | Crée un nouvel objet [**trustedDomain**](trusteddomain-object.md) .<br/>            |
| [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)<br/>                                                                                         | Supprime un objet [**trustedDomain**](trusteddomain-object.md) .<br/>                |
| [**LsaEnumerateTrustedDomains**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains)<br/> [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)<br/> | Énumère les domaines actuellement approuvés par le système local.<br/>                  |
| [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname)<br/>                                                                                 | Ouvre un handle vers un objet [**trustedDomain**](trusteddomain-object.md) .<br/>      |
| [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo)<br/>                                                                                   | Récupère des informations sur un domaine approuvé. Le domaine est spécifié par SID.<br/>  |
| [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname)<br/>                                                                       | Récupère des informations sur un domaine approuvé. Le domaine est spécifié par le nom.<br/> |
| [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname)<br/>                                                                           | Définit des informations pour un domaine approuvé. Le domaine est spécifié par le nom.<br/>        |
| [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation)<br/>                                                                         | Définit des informations pour un domaine approuvé. Le domaine est spécifié par SID.<br/>         |



 

### <a name="private-data-functions"></a>Fonctions de données privées

N’utilisez pas les fonctions de données privées LSA. Utilisez plutôt les fonctions [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) .



| Fonction                                                            | Description                                 |
|---------------------------------------------------------------------|---------------------------------------------|
| [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata)<br/> | Récupère et déchiffre une chaîne.<br/> |
| [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata)<br/>       | Chiffre et stocke une chaîne.<br/>    |



 

### <a name="miscellaneous-functions"></a>Fonctions diverses

L’API de la stratégie LSA contient les trois fonctions suivantes qui ne rentrent dans aucune des autres catégories de fonctions de la stratégie LSA.



| Fonction                                                          | Description                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)<br/>                           | Ferme un handle vers un objet de [**stratégie**](policy-object.md) ou un objet [**trustedDomain**](trusteddomain-object.md) .<br/> |
| [**LsaFreeMemory**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsafreememory)<br/>                 | Libère une mémoire tampon allouée par une fonction LSA.<br/>                                                                           |
| [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror)<br/> | Convertit une valeur **NTSTATUS** en code d’erreur Windows.<br/>                                                                |



 

## <a name="managed-service-account-functions"></a>Fonctions du compte de service géré

Les fonctions suivantes permettent de créer, d’énumérer, de rechercher et de supprimer des comptes de service gérés.



| Fonction                                                                      | Description                                                                                                                 |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**NetAddServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netaddserviceaccount)<br/>               | Crée un compte de service géré.<br/>                                                                               |
| [**NetEnumerateServiceAccounts**](/windows/desktop/api/Lmaccess/nf-lmaccess-netenumerateserviceaccounts)<br/> | Énumère les comptes de serveur sur le serveur spécifié.<br/>                                                          |
| [**NetIsServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netisserviceaccount)<br/>                 | Teste si le compte de service spécifié existe dans le magasin Netlogon sur le serveur spécifié.<br/>                |
| [**NetRemoveServiceAccount**](/windows/desktop/api/Lmaccess/nf-lmaccess-netremoveserviceaccount)<br/>         | Supprime le compte de service spécifié de la base de données [Active Directory](/windows/desktop/AD/active-directory-domain-services) .<br/> |



 

## <a name="password-filter-functions"></a>Fonctions de filtre de mot de passe

Les fonctions de [*filtre de mot de passe*](/windows/desktop/SecGloss/p-gly) suivantes sont implémentées par les dll de filtre de mot de passe personnalisées pour fournir une notification de modification de mot de



| Fonction                                                            | Description                                                     |
|---------------------------------------------------------------------|-----------------------------------------------------------------|
| [**InitializeChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_init_notification_routine)<br/> | Indique qu’une DLL de filtre de mots de passe est initialisée.<br/> |
| [**PasswordChangeNotify**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_notification_routine)<br/>     | Indique qu’un mot de passe a été modifié.<br/>          |
| [**PasswordFilter**](/windows/desktop/api/Ntsecapi/nc-ntsecapi-psam_password_filter_routine)<br/>                 | Valide un nouveau mot de passe en fonction de la stratégie de mot de passe.<br/>   |



 

## <a name="safer-functions"></a>Fonctions plus sécurisées

Les fonctions plus sécurisées suivantes peuvent être utilisées pour vérifier le niveau de sécurité de n’importe quel exécutable et pour consigner les événements.



| Fonction                                                         | Description                                                                                                                                                                          |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SaferCloseLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercloselevel)                       | Ferme un handle de \_ niveau plus sécurisé \_ ouvert à l’aide de la fonction [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) ou de la fonction [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel) .<br/> |
| [**SaferComputeTokenFromLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercomputetokenfromlevel) | Restreint un jeton à l’aide de restrictions spécifiées par un \_ handle de niveau plus sûr \_ .<br/>                                                                                                 |
| [**SaferCreateLevel**](/windows/desktop/api/WinSafer/nf-winsafer-safercreatelevel)                     | Ouvre un handle de \_ niveau plus sûr \_ .<br/>                                                                                                                                             |
| [**SaferGetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)     | Récupère des informations sur un niveau de stratégie.<br/>                                                                                                                               |
| [**SaferGetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetpolicyinformation)   | Récupère des informations sur une stratégie.<br/>                                                                                                                                     |
| [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel)                 | Récupère des informations sur un niveau.<br/>                                                                                                                                      |
| [**SaferiIsExecutableFileType**](/windows/desktop/api/WinSafer/nf-winsafer-saferiisexecutablefiletype) | Détermine si un fichier spécifié est un fichier exécutable.<br/>                                                                                                                |
| [**SaferRecordEventLogEntry**](/windows/desktop/api/WinSafer/nf-winsafer-saferrecordeventlogentry)     | Envoie un message au journal des événements.<br/>                                                                                                                                         |
| [**SaferSetLevelInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safersetlevelinformation)     | Définit les informations relatives à un niveau de stratégie.<br/>                                                                                                                                |
| [**SaferSetPolicyInformation**](/windows/desktop/api/WinSafer/nf-winsafer-safergetlevelinformation)    | Définit les contrôles de stratégie globale.<br/>                                                                                                                                          |



 

 

