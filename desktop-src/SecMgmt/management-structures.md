---
description: Répertorie les structures utilisées avec les API de gestion de la sécurité.
ms.assetid: 8df25095-a215-464a-abac-39a6ea05f6a3
title: Structures de gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2212332b65d89a8d2c1f5a24601a59cca041ff42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013617"
---
# <a name="security-management-structures"></a>Structures de gestion de la sécurité

Cette section contient des pages de référence pour les groupes de structures suivants :

-   [Structures de gestion des stratégies LSA](#lsa-policy-management-structures)
-   [Structures de pièces jointes](#attachment-structures)
-   [Structures plus sûres](#safer-structures)

## <a name="lsa-policy-management-structures"></a>Structures de gestion des stratégies LSA

Les structures suivantes sont utilisées par les fonctions de gestion de la stratégie LSA ( [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) ).



| Structure                                                                       | Description                                                                                                                                   |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informations d’authentification LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_auth_information)                          | Contient les informations d’authentification d’un domaine approuvé.                                                                                     |
| [**\_informations d’énumération LSA \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_enumeration_information)            | Contient un pointeur vers un [*identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID).    |
| [**\_attributs d’objet LSA \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_object_attributes)                        | Spécifie les attributs d’une connexion à l’objet de [**stratégie**](policy-object.md) .                                                       |
| [**\_liste de domaines référencés LSA \_ \_**](/windows/win32/api/lsalookup/ns-lsalookup-lsa_referenced_domain_list)             | Contient des informations sur les domaines référencés dans une opération de recherche.                                                                      |
| [**\_nom traduit \_ LSA**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_name)                            | Contient des informations sur le compte identifié par un SID.                                                                                   |
| [**\_sid traduit \_ LSA**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-lsa_translated_sid)                              | Contient des informations sur le SID qui identifie un compte.                                                                                |
| [**\_SID2 traduit \_ LSA**](/windows/desktop/api/LsaLookup/ns-lsalookup-lsa_translated_sid2)                            | Contient des informations sur le SID qui identifie un compte.                                                                                |
| [**\_informations d’approbation LSA \_**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information)                        | Identifie un domaine.                                                                                                                          |
| [**\_chaîne Unicode \_ LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string)                              | Contient une chaîne et ses informations de longueur.                                                                                                 |
| [**\_ \_ informations sur le domaine du compte de stratégie \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_account_domain_info)             | Permet de définir et d’interroger le nom et le SID du domaine du compte du système.                                                                        |
| [**\_ \_ informations sur les événements d’audit de stratégie \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_audit_events_info)                 | Permet de définir et d’interroger les règles d’audit du système.                                                                                            |
| [**\_ \_ informations sur le domaine DNS de la stratégie \_**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info)                     | Permet de définir et d’interroger les informations DNS (Domain Name System) relatives au domaine principal associé à un objet de [**stratégie**](policy-object.md) . |
| [**\_ \_ \_ informations sur le rôle de serveur LSA de la stratégie \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_lsa_server_role_info)          | Permet de définir et d’interroger le rôle d’un serveur LSA.                                                                                              |
| [**\_informations sur la modification de la stratégie \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_modification_info)                  | Utilisé pour interroger les informations relatives à l’heure de création et à la dernière modification de la base de données LSA.                                                  |
| [**informations de compte de la stratégie \_ PD \_ \_**](policy-pd-account-info.md)                     | Obsolète. Les stations de travail utilisent le nom de la station de travail, suivi du nom de compte $.                                                          |
| [**\_ \_ informations sur le domaine principal de la stratégie \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-policy_primary_domain_info)             | Obsolète. Utilisez **PolicyDnsDomainInformation** et la structure d' [**\_ \_ \_ informations de domaine DNS**](/windows/desktop/api/LsaLookup/ns-lsalookup-policy_dns_domain_info) de la stratégie à la place.           |
| [**\_informations d' \_ authentification de domaine approuvé \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_auth_information)   | Utilisé pour récupérer les informations d’authentification d’un domaine approuvé.                                                                             |
| [**\_ \_ informations complètes sur le domaine \_ approuvé**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_full_information)   | Utilisé pour récupérer des informations complètes sur un domaine approuvé.                                                                                 |
| [**\_informations sur les domaines approuvés de \_ \_ base**](/previous-versions/windows/desktop/legacy/ms722475(v=vs.85)) | Informations sur un domaine approuvé. Cette structure est identique aux [**\_ \_ informations d’approbation LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_trust_information).                  |
| [**\_informations sur les domaines approuvés par \_ \_ exemple**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_information_ex)       | Utilisé pour récupérer des informations étendues sur un domaine approuvé.                                                                                 |
| [**\_ \_ informations sur le nom de domaine approuvé \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_domain_name_info)                 | Utilisé pour interroger ou définir le nom d’un domaine approuvé.                                                                                            |
| [**\_informations de mot de passe approuvé \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_password_info)                        | Utilisé pour interroger ou définir le mot de passe d’un domaine approuvé.                                                                                       |
| [**\_informations de \_ décalage \_ POSIX approuvées**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-trusted_posix_offset_info)               | Utilisé pour interroger ou définir la valeur utilisée pour générer des identificateurs de groupe et d’utilisateur POSIX.                                                             |



 

Les types de structures suivants sont obsolètes ou réservés pour une utilisation ultérieure :

-   **\_ \_ \_ informations complètes sur la requête \_ d’audit de stratégie**
-   **\_ \_ \_ informations sur le jeu \_ complet de l’audit de stratégie**
-   **\_informations du \_ Journal d’audit de stratégie \_**
-   **\_informations de \_ quota par défaut de la stratégie \_**
-   **\_ \_ informations sur la source du RÉPLICA de stratégie \_**
-   **\_informations sur les contrôleurs approuvés \_**

## <a name="attachment-structures"></a>Structures de pièces jointes

Les structures suivantes sont utilisées par les dll de la configuration de sécurité jointes et leurs fonctions de prise en charge. Ces structures sont définies dans scesvc. h.



| Structure                                                        | Description                                                                                                                                     |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informations de configuration de SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info) | Contient les informations de configuration d’un service.                                                                                               |
| [**\_ligne de configuration SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_line) | Contient des informations sur une ligne de données de configuration.                                                                                        |
| [**\_informations d’analyse SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info)           | Contient les informations d’analyse.                                                                                                              |
| [**\_ligne d’analyse SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_line)           | Contient la clé, la valeur et la longueur de valeur pour une ligne spécifique spécifiée par une structure d' [**\_ \_ informations d’analyse SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info) . |
| [**\_informations de rappel SCESVC \_**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)           | Contient un handle de base de données opaque et des pointeurs de fonction de rappel pour interroger, définir et libérer des informations.                                          |



 

## <a name="safer-structures"></a>Structures plus sûres

Les structures et le type énuméré suivants sont utilisés dans plus de sécurité. Ils sont définis dans WinSafer. h.



| Structure                                                                | Description                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriétés de \_ code plus sûres \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_code_properties_v2)                 | Contient des informations sur l’image de code et des critères à vérifier sur l’image de code. Un tableau de ces structures est passé à la fonction [**SaferIdentifyLevel**](/windows/desktop/api/WinSafer/nf-winsafer-saferidentifylevel) .                                                                  |
| [**\_en-tête d’identification plus sécurisé \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header)     | Structure d’en-tête pour l' [**\_ \_ identification des chemins d’accès plus sûrs**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification), l' [**\_ \_ identification de hachage**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)plus sûre et les structures d' [**\_ \_ identification URLZONE plus sûres**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification) . |
| [**IDENTIFICATION du \_ chemin d’accès plus sécurisé \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_pathname_identification) | Contient le nom de chemin d’accès d’une image de code à vérifier.                                                                                                                                                                                                      |
| [**IDENTIFICATION de \_ hachage plus sûre \_**](/windows/desktop/api/WinSafer/ns-winsafer-safer_hash_identification)         | Identifie un hachage de l’image de code à vérifier.                                                                                                                                                                                                      |
| [**\_identification URLZONE plus \_ sûre**](/windows/desktop/api/WinSafer/ns-winsafer-safer_urlzone_identification)   | Identifie la zone d’URL d’origine de l’image de code à vérifier.                                                                                                                                                                                      |



 

 

 
