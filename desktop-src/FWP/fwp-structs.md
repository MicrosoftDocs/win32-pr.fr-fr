---
title: Structures WFP
description: les structures de l’API de la plateforme de filtrage Windows (WFP) sont les suivantes.
ms.assetid: e957132f-417b-40c1-afe3-5aec0e2192f7
keywords:
- Windows Filtrage des types énumérés de l’API de plateforme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b1bd45efbe1a93ddeb0c95161aa52764bf1812ecc5f8e914e01317b657f251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069169"
---
# <a name="wfp-structures"></a>Structures WFP

les structures de l’API de la plateforme de filtrage Windows (WFP) sont les suivantes.

Structures de gestion

-   [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
-   [**FWPM \_ CALLOUT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout0)
-   [**FWPM \_ légende \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_change0)
-   [**FWPM \_ \_ enum \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_enum_template0)
-   [**FWPM \_ légende \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_callout_subscription0)
-   [**FWPM \_ classifier \_ OPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0)
-   [**FWPM \_ classifier \_ OPTIONS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_options0)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ énumération de la connexion \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM de \_ connexion \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ afficher \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0)
-   [**FWPM \_ FIELD0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_field0)
-   [**FWPM \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)
-   [**FWPM \_ filtre \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_change0)
-   [**FWPM \_ filtre \_ CONDITION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_condition0)
-   [**\_Énumération de filtre FWPM \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_enum_template0)
-   [**FWPM \_ filtre \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter_subscription0)
-   [**FWPM \_ LAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer0)
-   [**\_Énumération de la couche FWPM \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_enum_template0)
-   [**FWPM de la \_ couche \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_layer_statistics0)
-   \_événement réseau FWPM \_ :
    -   [**FWPM \_ NET \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event0) (Windows Vista)
    -   [**FWPM \_ \_EVENT1 NET**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event1) (Windows 7)
    -   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2) (Windows 8)
-   [**FWPM \_ NET \_ Event \_ Capability \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ Event \_ Capability \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ Event \_ classifier \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   \_Suppression de \_ classification d’événement FWPM NET \_ \_ :
    -   [**FWPM \_ NET \_ EVENT \_ classifier \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop0) (Windows Vista)
    -   [**FWPM \_ NET \_ EVENT \_ classifier \_ DROP1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop1) (Windows 7 et versions ultérieures)
    -   [**FWPM \_ NET \_ EVENT \_ classifier \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2) (Windows 8)
-   [**FWPM \_ NET \_ Event \_ classification \_ DROP \_ Mac0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ NET \_ Event \_ enum \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_enum_template0)
-   \_ \_ en-tête d’événement .net FWPM \_ :
    -   [**FWPM \_ \_ \_ HEADER0 d’événements .net**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header0) (Windows Vista)
    -   [**FWPM \_ \_ \_ HEADER1 d’événements .net**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_header1) (Windows 7)
    -   [**FWPM \_ \_ \_ HEADER2 d’événements .net**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2) (Windows 8)
-   échec de la \_ diffusion en em d’événement net FWPM \_ \_ \_ \_ :
    -   [**FWPM \_ \_événement NET \_ IKEEXT \_ EM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure0) (Windows Vista)
    -   [**FWPM \_ \_événement NET \_ IKEEXT \_ EM \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_em_failure1) (Windows 7 et versions ultérieures)
-   échec de l' \_ événement réseau FWPM NET \_ \_ \_ \_ :
    -   [**FWPM \_ \_événement NET \_ IKEEXT \_ MM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure0) (Windows Vista)
    -   [**FWPM \_ \_événement NET \_ IKEEXT \_ \_ FAILURE1**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_mm_failure1) (Windows 7 et versions ultérieures)
-   [**FWPM \_ NET \_ Event \_ IKEEXT \_ QM \_ FAILURE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ikeext_qm_failure0)
-   [**FWPM \_ NET \_ Event \_ \_ DOSP IPSec \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_dosp_drop0)
-   [**FWPM \_ NET \_ Event \_ \_ DROP0 kernel \_ IPSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_ipsec_kernel_drop0)
-   [**FWPM \_ net, \_ événement \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_subscription0)
-   [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)
-   [**\_Fournisseur FWPM \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_change0)
-   \_contexte du fournisseur FWPM \_ :
    -   [**FWPM \_ fournisseur \_ CONTEXT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context0) (Windows Vista)
    -   [**FWPM \_ \_CONTEXT1 du fournisseur**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context1) (Windows 7)
    -   \_Fournisseur FWPM \_ CONTEXT2 (Windows 8)
-   [**\_Contexte du fournisseur FWPM \_ \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_change0)
-   [**\_Énumération du contexte du fournisseur FWPM \_ \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0)
-   [**\_Contexte du fournisseur FWPM \_ \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_context_subscription0)
-   [**\_Énumération du fournisseur FWPM \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)
-   [**\_Fournisseur FWPM \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider_subscription0)
-   [**FWPM \_ SESSION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0)
-   [**\_Énumération de la session FWPM \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session_enum_template0)
-   [**FWPM \_ STATISTICS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_statistics0)
-   [**FWPM \_ SUBLAYER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer0)
-   [**FWPM sous- \_ couche \_ CHANGE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_change0)
-   [**FWPM sous- \_ couche \_ enum \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_enum_template0)
-   [**FWPM sous- \_ couche \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_sublayer_subscription0)
-   [**FWPM \_ système \_ PORTS0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports0)
-   [**FWPM \_ les \_ ports système \_ par \_ TYPE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_system_ports_by_type0)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**\_Événement FWPM \_ VSWITCH \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

Structures partagées

-   [**FWP \_ Byte \_ ARRAY6**](/windows/win32/api/fwptypes/ns-fwptypes-fwp_byte_array6)
-   [**FWP \_ Byte \_ ARRAY16**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_array16)
-   [**\_objet blob d’octets fwp \_**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_byte_blob)
-   [**\_Condition fwp \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0)
-   [**FWP \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0)
-   [**\_type de correspondance fwp \_**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type)
-   [**\_ \_ ADR \_ et masque fwp \_ v4**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v4_addr_and_mask)
-   [**\_ \_ ADR \_ et masque fwp \_ V6**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_v6_addr_and_mask)
-   [**FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0)

Structures IKE/AuthIP

-   \_méthode d’authentification IKEEXT \_ :
    -   [**IKEEXT \_ \_METHOD0 d’authentification**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0) (Windows Vista)
    -   [**IKEEXT \_ authentification \_ méthode1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1) (Windows 7)
    -   [**IKEEXT \_ authentification \_ méthode2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2) (Windows 8)
-   [**\_EKUS0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_ \_ CONFIG0 racine du certificat IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   \_authentification du certificat IKEEXT \_ :
    -   [**IKEEXT \_ certificate \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0) (Windows Vista)
    -   [**IKEEXT \_ \_AUTHENTICATION1 de certificat**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1) (Windows 7)
    -   [**IKEEXT \_ \_AUTHENTICATION2 de certificat**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2) (Windows 8)
-   \_ \_ informations d’identification du certificat IKEEXT :
    -   [**IKEEXT \_ certificate \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0) (Windows Vista)
    -   [**IKEEXT \_ \_CREDENTIAL1 de certificat**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1) (Windows 7 et versions ultérieures)
-   [**\_CRITERIA0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**\_ALGORITHM0 de chiffrement IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   \_statistiques courantes IKEEXT \_ :
    -   [**IKEEXT \_ \_STATISTICS0 courants**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_STATISTICS1 courants**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1) (Windows 7 et versions ultérieures)
-   [**\_PAIR0 cookie \_ IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   \_informations d’identification IKEEXT :
    -   [**IKEEXT \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIAL1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1) (Windows 7 et versions ultérieures)
-   \_paire d’informations d’identification IKEEXT \_ :
    -   [**IKEEXT \_ informations d’identification \_ PAIR0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0) (Windows Vista)
    -   [**IKEEXT \_ informations d’identification \_ PAIR1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1) (Windows 7 et versions ultérieures)
-   \_informations d’identification IKEEXT :
    -   [**IKEEXT \_ CREDENTIALS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0) (Windows Vista)
    -   [**IKEEXT \_ CREDENTIALS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1) (Windows 7 et versions ultérieures)
-   [**\_AUTHENTICATION0 EAP \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   stratégie de IKEEXT \_ em \_ :
    -   [**IKEEXT \_ EM \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0) (Windows Vista)
    -   [**IKEEXT \_ EM \_ stratégie1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1) (Windows 7)
    -   [**IKEEXT \_ \_POLICY2 EM**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2) (Windows 8)
-   [**\_ALGORITHM0 intégrité de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   \_ \_ \_ \_ statistiques courantes spécifiques \_ à la version d’IP IKEEXT :
    -   [**IKEEXT \_ \_ \_ \_ \_ STATISTICS0 commun spécifique à la VERSION IP**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_ \_ \_ \_ STATISTICS1 commun spécifique à la VERSION IP**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1) (Windows 7 et versions ultérieures)
-   \_statistiques du \_ MODULE de module spécifique à la version IP de IKEEXT \_ \_ \_ :
    -   [**IKEEXT \_ \_ \_ \_ \_ STATISTICS0 spécifique à la VERSION IP**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ \_ \_ \_ \_ STATISTICS1 de VERSION IP spécifique**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1) (Windows 7 et versions ultérieures)
-   [**IKEEXT \_ IPv6 \_ CGA \_ AUTHENTICATION0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   \_statistiques du KEYMODULE IKEEXT \_ :
    -   [**IKEEXT \_ \_AUTHENTICATION0 KERBEROS**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0) (Windows Vista et Windows 7)
    -   [**IKEEXT \_ \_AUTHENTICATION1 KERBEROS**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1) (Windows 8)
-   -   \_statistiques du KEYMODULE IKEEXT \_ :
    -   [**IKEEXT \_ keymodule \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0) (Windows Vista)
    -   [**IKEEXT \_ keymodule \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1) (Windows 7 et versions ultérieures)
-   [**Nom de IKEEXT \_ \_ CREDENTIAL0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [**AUTHENTICATION0 à la fois \_ NTLM \_ v2 \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   \_stratégie IKEEXT :
    -   [**IKEEXT \_ POLICY0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0) (Windows Vista)
    -   [**IKEEXT \_ stratégie1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1) (Windows 7)
    -   [**IKEEXT \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2) (Windows 8)
-   \_authentification par clé PRÉpartagée IKEEXT \_ \_ :
    -   [**IKEEXT \_ \_ \_ AUTHENTICATION0 clé prépartagée**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0) (Windows Vista)
    -   [**IKEEXT \_ clé prépartagée \_ \_ AUTHENTICATION1**](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1) (Windows 7 et versions ultérieures)
-   [**\_PROPOSAL0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [**\_AUTHENTICATION0 réservé \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   Détails de la \_ sa IKEEXT \_ :
    -   [**IKEEXT \_ SA \_ DETAILS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0) (Windows Vista)
    -   [**IKEEXT \_ SA \_ DETAILS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1) (Windows 7 et versions ultérieures)
-   [**TEMPLATE0 de l' \_ \_ énumération sa de IKEEXT \_**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   statistiques de IKEEXT \_ :
    -   [**IKEEXT \_ STATISTICS0**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0) (Windows Vista)
    -   [**IKEEXT \_ STATISTICS1**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1) (Windows 7 et versions ultérieures)
-   [**\_TRAFFIC0 IKEEXT**](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

Structures IPsec

-   [**\_Adresse IPSec \_ INFO0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   \_statistiques des \_ paquets Drop IPSec Aggregate \_ \_ :
    -   [**IPSec \_ \_STATISTICS0 de \_ paquets \_ de dépôt d’agrégats**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0) (Windows Vista)
    -   [**IPSec \_ \_ \_ \_ STATISTICS1 de suppression de paquets d’agrégats**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1) (Windows 7 et versions ultérieures)
-   [**\_STATISTICS0 d’agrégation IPSec \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**\_STATISTICS0 de \_ suppression du \_ paquet \_ IPSec Ah**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**\_Authentification \_ et \_ chiffrement IPSec \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**\_TRANSFORM0 d’authentification IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**\_ID0 de \_ transformation d’authentification IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**\_TRANSFORM0 de chiffrement IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**\_Transformation de chiffrement IPSec \_ \_ ID0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**IPSEC \_ DOSP \_ OPTIONS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**IPSEC \_ DOSP \_ STATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**\_ \_ Énumération d’État DOSP IPSec \_ \_ TEMPLATE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**IPSEC \_ DOSP \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**\_STATISTICS0 de \_ Suppression de \_ paquets \_ IPSec ESP**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   \_GETSPI IPSec :
    -   [**IPSec \_ GETSPI0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0) (Windows Vista)
    -   [**IPSec \_ GETSPI1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1) (Windows 7 et versions ultérieures)
-   [**\_ID0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_Clé IPSec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_Gestionnaire de clés IPSec \_ \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   \_stratégie de génération de clés IPSec \_ :
    -   [**IPSec \_ génération de clés \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0) (Windows Vista et Windows 7)
    -   [**IPSec \_ masquage de \_ stratégie1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1) (Windows 8)
-   [**STATE0 du MODULE de sécurité IPSEC \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_SA0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_Authentification sa \_ \_ et \_ chiffrement \_ INFORMATION0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**Autorité de sécurité \_ sa \_ \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   Bundle d’association de sécurité IPSEC \_ \_ :
    -   [**IPSec \_ SA \_ BUNDLE0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0) (Windows Vista)
    -   [**IPSec \_ SA \_ BUNDLE1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1) (Windows 7 et versions ultérieures)
-   [**\_INFORMATION0 de \_ chiffrement d’association de sécurité IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   \_contexte sa IPSec \_ :
    -   [**IPSec \_ SA \_ CONTEXT0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0) (Windows Vista)
    -   [**IPSec \_ SA \_ CONTEXT1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1) (Windows 7 et versions ultérieures)
-   [**\_CHANGE0 de \_ contexte \_ sa IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_TEMPLATE0 d' \_ énumération de contexte sa IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**\_SUBSCRIPTION0 de \_ contexte \_ sa IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   Détails de l’Association de sécurité IPSEC \_ \_ :
    -   [**IPSec \_ SA \_ DETAILS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0) (Windows Vista)
    -   [**IPSec \_ SA \_ DETAILS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1) (Windows 7 et versions ultérieures)
-   [**TEMPLATE0 de l' \_ énumération d’association de sécurité IPSec \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**\_TIMEOUT0 d' \_ inactivité de l’Association de sécurité IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**\_LIFETIME0 sa \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**\_TRANSFORM0 sa \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   \_statistiques IPSec :
    -   [**IPSec \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0) (Windows Vista)
    -   [**IPSec \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1) (Windows 7 et versions ultérieures)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   \_trafic IPSec :
    -   [**IPSec \_ TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) (Windows Vista)
    -   [**IPSec \_ gestion1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1) (Windows 7 et versions ultérieures)
-   \_statistiques du trafic IPSec \_ :
    -   [**IPSec \_ trafic \_ STATISTICS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0) (Windows Vista)
    -   [**IPSec \_ trafic \_ STATISTICS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1) (Windows 7 et versions ultérieures)
-   \_stratégie de transport IPSec \_ :
    -   [**IPSec \_ \_POLICY0 de TRANSPORT**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) (Windows Vista)
    -   [**IPSec \_ TRANSPORT \_ stratégie1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1) (Windows 7)
    -   [**IPSec \_ \_POLICY2 de TRANSPORT**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2) (Windows 8)
-   [**\_Tunnel IPSec \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   \_points de terminaison de tunnel IPSec \_ :
    -   [**IPSec \_ TUNNEL \_ ENDPOINTS0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0) (Windows Vista)
    -   [**IPSec \_ TUNNEL \_ ENDPOINTS1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1) (Windows 7)
    -   [**IPSec \_ TUNNEL \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2) (Windows 8)
-   \_stratégie de tunnel IPSec \_ :
    -   [**IPSec \_ TUNNEL \_ POLICY0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0) (Windows Vista)
    -   [**IPSec \_ TUNNEL \_ stratégie1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1) (Windows 7)
    -   [**IPSec \_ TUNNEL \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2) (Windows 8)
-   [**\_ \_ ENCAPSULATION0 UDP v4 \_ UDP**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ virtuel \_ si \_ tunnel \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




