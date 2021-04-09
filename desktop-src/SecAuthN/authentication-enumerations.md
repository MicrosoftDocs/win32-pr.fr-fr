---
description: Répertorie les énumérations utilisées dans les API d’authentification.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Énumérations d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750933"
---
# <a name="authentication-enumerations"></a>Énumérations d’authentification

Les énumérations d’authentification sont classées en fonction de l’utilisation comme suit :

-   [Énumérations de la gestion des informations d’identification](#credentials-management-enumerations)
-   [Énumérations LSA](#lsa-enumerations)
-   [Énumérations de fournisseur réseau](#network-provider-enumerations)
-   [Énumérations CredSSP (Credential Security Support Provider)](#credential-security-support-provider-credssp-enumerations)
-   [Autres énumérations](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Énumérations de la gestion des informations d’identification

La gestion des informations d’identification utilise les énumérations suivantes.



| Énumération                                            | Description                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type de Marshal de cred \_**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contient les types d’informations d’identification qui peuvent être marshalés par [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) ou démarshalés par [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala).<br/> |
| [**\_type de protection cred \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Spécifie le contexte de sécurité dans lequel les informations d’identification sont chiffrées lors de l’utilisation de la fonction [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) .<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Énumérations LSA

LSA utilise les énumérations suivantes.



| Énumération                                                                                   | Description                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_type d' \_ envoi de connexion KERB \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Répertorie le type d’ouverture de session demandé.<br/>                                                                                                                                                                                                                  |
| [**\_type de \_ tampon du profil KERB \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Répertorie le type de profil d’ouverture de session retourné.<br/>                                                                                                                                                                                                                 |
| [**\_type de \_ message de protocole KERB \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Répertorie les types de messages qui peuvent être envoyés au package d’authentification [*Kerberos*](/windows/desktop/SecGloss/k-gly) en appelant [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**\_type d' \_ \_ enregistrement collision \_ d’approbation de forêt LSA \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Définit les types de collisions qui peuvent se produire entre des enregistrements d’approbation de forêt LSA.<br/>                                                                                                                                                                           |
| [**\_type d' \_ enregistrement d’approbation de forêt LSA \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Définit le type d’un enregistrement d’approbation de forêt LSA.<br/>                                                                                                                                                                                                           |
| [**\_type d' \_ informations de jeton LSA \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Spécifie les niveaux d’informations qui peuvent être inclus dans un jeton d’ouverture de session.<br/>                                                                                                                                                                                |
| [**\_ \_ Type d’envoi d’ouverture de session MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Répertorie le type d’ouverture de session demandé.<br/>                                                                                                                                                                                                                  |
| [**\_Type de \_ tampon de profil MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Répertorie le type de profil d’ouverture de session retourné.<br/>                                                                                                                                                                                                                 |
| [**\_Type de \_ message de protocole MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Répertorie les types de messages qui peuvent être envoyés au [ \_ package d’authentification MSV1 0](msv1-0-authentication-package.md) en appelant [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**\_classe d' \_ informations du domaine de stratégie \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Définit le type d’informations de domaine de stratégie.<br/>                                                                                                                                                                                                            |
| [**\_type de connexion de sécurité \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indique le type d’ouverture de session demandé par un processus d’ouverture de session.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Énumérations de fournisseur réseau

Le fournisseur réseau utilise les énumérations suivantes.



| Énumération                                                                       | Description                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_classe d' \_ informations ÉTENDUEs SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Type d’énumération qui spécifie le type d’informations à définir ou à obtenir pour un [*package de sécurité*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**\_type de nom SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valeur d’énumération qui spécifie le type de nom spécifié pour un compte.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Énumérations CredSSP (Credential Security Support Provider)

CredSSP utilise les énumérations suivantes.



| Énumération                                          | Description                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_type d’envoi CREDSPP \_**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Spécifie le type d’informations d’identification spécifié par une structure [**CREDSSP \_ cred**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) .<br/> |



 

## <a name="other-enumerations"></a>Autres énumérations

Voici les autres énumérations utilisées par l’authentification.



| Énumération                                                   | Description                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TYPE d’identité \_**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Spécifie le type d’identités à énumérer.<br/>                                                                                                                                                                  |
| [**\_Type d' \_ envoi de connexion PKU2U \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indique le type de message d’ouverture de session transmis dans une structure de [**\_ \_ \_ connexion S4U du certificat PKU2U**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) .<br/>                                                                                |
| [**État de SECPKG \_ attr \_ LCT \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indique si le jeton de l’appel le plus récent à la fonction [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) est le dernier jeton du client.<br/>                               |
| [**\_classe cred \_ SECPKG**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indique le type d’informations d’identification utilisé dans un contexte client. L’énumération de la [**\_ \_ classe SECPKG cred**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) est utilisée dans la structure [**SecPkgContext \_ CredInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) .<br/> |



 

 

