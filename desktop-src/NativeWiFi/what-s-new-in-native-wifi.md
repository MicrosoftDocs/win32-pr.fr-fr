---
description: Nouveautés du Wi-Fi natif
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Nouveautés du Wi-Fi natif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2126627f4cf6431fbac2bf4d1f6ec58561bfd8bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413737"
---
# <a name="whats-new-in-native-wifi"></a>Nouveautés du Wi-Fi natif

## <a name="windows-10-version-2004"></a>Windows 10, version 2004

Consultez [approvisionner un profil de Wi-Fi via un site Web](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10

La prise en charge de hotspot 2,0 a été ajoutée au [ \_ schéma de profil WLAN](wlan-profileschema-schema.md). La zone réactive 2,0 permet la connexion automatique aux services de Wi-Fi publics à l’aide des informations d’identification existantes et de l’appartenance aux réseaux de fournisseurs de services. Les fournisseurs de services spécifient la façon dont les connexions sont établies à l’aide des nouveaux éléments de schéma pour décrire les réseaux à utiliser et comment s’y authentifier. Pour plus d’informations, consultez la documentation de l’élément [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 et Windows Server 2012

les fonctionnalités suivantes ont été ajoutées aux api wi-fi natives sur Windows 8 et Windows Server 2012.

Une fonctionnalité directe Wi-Fi basée sur le développement de la spécification technique d’égal à égal Wi-Fi v 1.1 par l’Alliance d' Wi-Fi (voir [spécifications publiées pour la Wi-Fi Alliance](https://www.wi-fi.org/)). L’objectif de la spécification technique d’égal à égal Wi-Fi consiste à fournir une solution pour Wi-Fi la connectivité appareil-appareil sans avoir besoin d’un point d’accès sans fil (AP sans fil) pour configurer la connexion ou l’utilisation du mécanisme ad hoc (IBSS) Wi-Fi existant.

Les fonctions suivantes prennent en charge la fonctionnalité Wi-Fi directe.

-   [**\_rappel d’ouverture de session WFD \_ \_ terminé \_**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

les fonctionnalités suivantes ont été ajoutées aux api Wifi natives sur Windows 7 et Windows Server 2008 R2.

Le réseau hébergé sans fil permet à un seul adaptateur sans fil physique de se connecter en tant que client à un point d’accès matériel, tout en faisant office de point d’accès logiciel, ce qui permet à d’autres périphériques sans fil de s’y connecter.

Les fonctions suivantes prennent en charge la fonctionnalité de réseau hébergé sans fil.

-   [**WlanHostedNetworkForceStart**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**WlanHostedNetworkForceStop**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**WlanHostedNetworkInitSettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**WlanHostedNetworkQueryProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**WlanHostedNetworkQuerySecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**WlanHostedNetworkQueryStatus**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**WlanHostedNetworkRefreshSecuritySettings**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**WlanHostedNetworkSetProperty**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**WlanHostedNetworkSetSecondaryKey**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**WlanHostedNetworkStartUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**WlanHostedNetworkStopUsing**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**WlanRegisterVirtualStationNotification**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

Les nouvelles structures suivantes fonctionnent avec un réseau hébergé sans fil.

-   [**\_paramètres de \_ \_ connexion réseau hébergée WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**changement d’état de l' \_ \_ \_ homologue des données du réseau hébergé \_ \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**\_État de \_ l' \_ homologue du réseau hébergé WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**\_ \_ État radio du réseau hébergé \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**\_paramètres de \_ \_ sécurité réseau hébergés WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**\_changement d' \_ État du réseau hébergé \_ WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**\_État du \_ réseau \_ hébergé WLAN**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Les nouvelles énumérations suivantes fonctionnent avec un réseau hébergé sans fil.

-   [**\_Code de \_ notification du réseau hébergé \_ WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**\_OPCODE du \_ réseau \_ hébergé WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**\_État d' \_ \_ authentification des homologues du réseau hébergé \_ WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**\_raison du \_ réseau \_ hébergé WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**\_État du \_ réseau \_ hébergé WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du réseau hébergé sans fil](about-the-wireless-hosted-network.md)
</dt> <dt>

[Utilisation du partage de connexion Internet et d’un réseau hébergé sans fil](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



