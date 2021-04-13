---
title: Structures IKE/AuthIP
description: Structures IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2020
ms.locfileid: "104381626"
---
# <a name="ikeauthip-structures"></a>Structures IKE/AuthIP

## <a name="in-this-section"></a>Dans cette section

-   [**\_METHOD0 d’authentification IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [**\_Méthode1 d’authentification IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [**\_Authentification IKEEXT \_ méthode2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ CONFIG0 racine du certificat IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [**\_AUTHENTICATION0 de certificat IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [**\_AUTHENTICATION1 de certificat IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [**\_AUTHENTICATION2 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CREDENTIAL0 de certificat IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [**\_CREDENTIAL1 de certificat IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [**\_CRITERIA0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 de chiffrement IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [**\_STATISTICS0 commun de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [**\_STATISTICS1 commun de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [**\_PAIR0 cookie \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [**\_CREDENTIAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [**\_CREDENTIAL1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [**\_CREDENTIAL2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [**\_CREDENTIALS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [**\_CREDENTIALS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [**\_CREDENTIALS2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [**\_PAIR0 d’informations d’identification IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [**\_PAIR1 d’informations d’identification IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [**\_PAIR2 d’informations d’identification IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [**\_AUTHENTICATION0 EAP \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [**POLICY0 de l’EM de la IKEEXT \_ \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [**IKEEXT \_ em \_ Stratégie1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [**POLICY2 de l’EM de la IKEEXT \_ \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_ALGORITHM0 intégrité de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [**\_ \_ \_ \_ STATISTICS0 commun spécifique à la version IP de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [**\_ \_ \_ \_ STATISTICS1 commun spécifique à la version IP de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [**\_ \_ \_ STATISTICS0 spécifique à la version IP \_ de \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [**\_ \_ \_ STATISTICS1 spécifique à la version IP \_ de \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [**IKEEXT \_ IPv6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [**\_AUTHENTICATION0 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [**\_AUTHENTICATION1 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_STATISTICS0 de KEYMODULE IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [**\_STATISTICS1 de KEYMODULE IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [**Nom de IKEEXT \_ \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**AUTHENTICATION0 à la fois \_ NTLM \_ v2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [**\_POLICY0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [**IKEEXT \_ Stratégie1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_AUTHENTICATION0 clé PRÉpartagée IKEEXT \_ \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [**\_AUTHENTICATION1 clé PRÉpartagée IKEEXT \_ \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_AUTHENTICATION0 réservé \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [**IKEEXT \_ sa \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [**IKEEXT \_ sa \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [**IKEEXT \_ sa \_ DETAILS2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [**TEMPLATE0 de l' \_ \_ énumération sa de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [**\_STATISTICS0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [**\_STATISTICS1 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




