---
title: Nouveautés de la plateforme de filtrage Windows
description: Windows 8 et Windows Server 2012 introduisent de nouveaux éléments de programmation de plateforme de filtrage Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316926"
---
# <a name="whats-new-in-windows-filtering-platform"></a>Nouveautés de la plateforme de filtrage Windows

Windows 8 et Windows Server 2012 introduisent de nouveaux éléments de programmation de plateforme de filtrage Windows. Les nouvelles fonctionnalités incluent les éléments suivants :

-   *Filtrage de couche 2*: permet d’accéder à la couche L2 (Mac), ce qui permet de filtrer le trafic au niveau de cette couche.
-   *filtrage vswitch*: autorise l’inspection et/ou la modification des paquets traversant un vswitch. Des filtres ou des légendes WFP peuvent être utilisés au niveau de l’entrée et de la sortie du vSwitch.
-   *Gestion* des conteneurs d’applications : permet d’accéder aux informations sur les conteneurs d’applications et les problèmes de connectivité d’isolement réseau.
-   *Mises à jour IPSec*: fonctionnalités IPSec étendues, notamment la surveillance de l’état de connexion, la sélection des certificats et la gestion des clés.

Le kit de pilotes Windows comprend également des informations sur [les modifications de WFP pour Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Mises à jour de l’API Windows 8

De nombreuses nouvelles API ont été ajoutées pour Windows 8 et Windows Server 2012.

## <a name="new-functions"></a>Nouvelles fonctions

-   [**FWPM \_ net, \_ événement \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**\_Dictée de clé du gestionnaire de clés IPSec \_ \_ \_ \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**Le \_ Gestionnaire de clés IPSec \_ \_ dicte \_ Key0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**Gestionnaire de clés IPSEC- \_ \_ \_ notifier \_ Key0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**\_CALLBACK0 de \_ contexte \_ sa IPSec**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**NetworkIsolationDiagnoseConnectFailureAndGetInfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**NetworkIsolationEnumAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**NetworkIsolationEnumerateAppContainerRules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**NetworkIsolationFreeAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**NetworkIsolationGetAppContainerConfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**NetworkIsolationRegisterForAppContainerChanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**NetworkIsolationSetAppContainerConfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**NetworkIsolationSetupAppContainerBinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**rappel des modifications du PAC \_ \_ \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Nouvelles structures

-   [**\_Authentification IKEEXT \_ méthode2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_AUTHENTICATION2 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CRITERIA0 de certificat IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**POLICY2 de l’EM de la IKEEXT \_ \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_AUTHENTICATION1 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_Clé IPSec \_ MANAGER0**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_Gestionnaire de clés IPSec \_ \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_Génération de clés IPSec \_ Stratégie1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**\_CHANGE0 de \_ contexte \_ sa IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_SUBSCRIPTION0 de \_ contexte \_ sa IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_POLICY2 de transport IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_Tunnel IPSec \_ ENDPOINT0**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_Tunnel IPSec \_ ENDPOINTS2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_Tunnel IPSec \_ POLICY2**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**FWPM \_ énumération de la connexion \_ \_ TEMPLATE0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM de \_ connexion \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ NET \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**FWPM \_ NET \_ Event \_ Capability \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**FWPM \_ NET \_ Event \_ Capability \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**FWPM \_ NET \_ Event \_ classifier \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**FWPM \_ NET \_ Event \_ classifier \_ DROP2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**FWPM \_ NET \_ Event \_ classification \_ DROP \_ Mac0**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ net, \_ événement \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**\_Fournisseur FWPM \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**\_Événement FWPM \_ VSWITCH \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Nouveaux types énumérés

-   [**\_type de \_ réseau \_ VSWITCH fwp**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**\_type de \_ \_ capacité réseau APPC FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_type d' \_ événement de connexion FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**\_type d' \_ événement FWPM VSWITCH \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**\_type de \_ nom des critères de certificat IKEEXT \_ \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**\_TYPE0 d' \_ événement de contexte sa \_ IPSec \_**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Nouveaux identificateurs de couche de filtrage

[**Filtrage des identificateurs de couche :**](management-filtering-layer-identifiers-.md)

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native
-   entrée de \_ couche FWPM \_ \_ vswitch \_ Ethernet
-   FWPM de sortie de la \_ couche de \_ sortie \_ \_ Ethernet
-   Entrée de \_ couche FWPM \_ -entrée \_ vswitch \_ transport \_ v4/FWPM couche d’entrée de \_ \_ \_ \_ transport vswitch \_ V6
-   Sortie de la couche FWPM \_ \_ sortie de \_ \_ transport vswitch \_ v4/FWPM de \_ sortie de la couche de sortie \_ \_ vswitch \_ \_ V6

## <a name="new-filtering-condition-identifiers"></a>Nouveaux identificateurs de condition de filtrage

[**Filtrage des identificateurs de condition :**](filtering-condition-identifiers-.md)

-   \_ \_ \_ adresse MAC de l’interface de condition FWPM \_
-   \_ \_ \_ adresse locale Mac de la condition FWPM \_
-   \_ \_ \_ adresse distante Mac de la condition FWPM \_
-   \_type d' \_ éther de condition FWPM \_
-   \_ \_ ID VLAN de condition FWPM \_
-   \_ \_ port NDIS de condition FWPM \_
-   \_type de \_ \_ média NDIS de condition \_ FWPM
-   \_type de \_ \_ média physique \_ NDIS \_ condition FWPM
-   \_ \_ Indicateurs L2 de condition FWPM \_
-   \_type d' \_ \_ adresse locale \_ Mac \_ de condition FWPM
-   FWPM \_ condition \_ Mac \_ \_ type d’adresse distante \_
-   \_ID de \_ \_ package ALE de condition \_ FWPM
-   \_ \_ \_ adresse source Mac de la condition FWPM \_
-   \_adresse de \_ \_ destination Mac \_ de la condition FWPM
-   \_type d' \_ \_ adresse source \_ Mac \_ de la condition FWPM
-   \_type d' \_ \_ adresse de destination Mac \_ \_ de la condition FWPM
-   \_port de \_ \_ source IP \_ de la condition FWPM
-   \_port de \_ \_ destination IP de condition \_ FWPM
-   \_ \_ ID VSWITCH de condition FWPM \_
-   FWPM \_ condition \_ \_ type de réseau VSWITCH \_
-   \_condition FWPM \_ \_ ID d' \_ interface source VSWITCH \_
-   \_condition FWPM \_ \_ ID d’interface de destination VSWITCH \_ \_
-   FWPM \_ condition \_ VSWITCH \_ ID de la \_ machine virtuelle source \_
-   FWPM \_ condition \_ VSWITCH \_ ID de la \_ machine virtuelle de destination \_
-   FWPM \_ condition \_ \_ type d' \_ interface \_ source VSWITCH
-   FWPM \_ état \_ \_ réseau du locataire VSWITCH \_ \_

## <a name="new-filtering-condition-flags"></a>Nouveaux indicateurs de condition de filtrage

[**Indicateurs de condition de filtrage :**](filtering-condition-flags-.md)

-   l' \_ indicateur de condition fwp \_ est une \_ \_ \_ connexion proxy
-   l' \_ indicateur de condition fwp \_ est un \_ \_ \_ bouclage APPCONTAINER
-   l' \_ indicateur de condition fwp \_ est un \_ \_ \_ bouclage non APPCONTAINER \_
-   l’indicateur de condition FWP respecte l' \_ \_ \_ autorisation de \_ \_ stratégie \_
-   La \_ condition fwp \_ L2 \_ est \_ native \_ Ethernet
-   La \_ condition fwp \_ L2 \_ est \_ WiFi
-   La \_ condition fwp \_ L2 \_ est \_ Mobile \_ Broadband
-   \_La condition fwp \_ L2 \_ est \_ WiFi \_ direct \_ Data
-   La \_ condition fwp \_ L2 \_ est \_ VM2VM
-   La \_ condition fwp \_ L2 \_ est un \_ paquet mal formé \_
-   La \_ condition fwp \_ L2 \_ est un \_ \_ groupe de fragments IP \_
-   \_Condition fwp \_ L2 \_ si le \_ connecteur est \_ présent

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Mises à jour de Windows 7 sur la plateforme de filtrage Windows

Le document [Nouveautés de la plateforme de filtrage Windows]() détaille la plupart des mises à jour apportées à Windows 7. Les informations sont également disponibles dans le kit de pilotes Windows sur [les modifications de WFP pour Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 