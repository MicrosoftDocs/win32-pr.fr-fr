---
description: Glossaire des termes Moniteur réseau qui commencent par la lettre N.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: a9b0e907-45c0-4301-9e83-398dd1c1c39a
title: N (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54404640b13bff3b098b9d223e656e8f1905c055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867018"
---
# <a name="n-network-monitor"></a>N (Moniteur réseau)

<dl> <dt>

<span id="_netmon_ndis_gly"></span><span id="_NETMON_NDIS_GLY"></span>**NDIS**
</dt> <dd>

Voir spécification de l’interface du pilote réseau.

</dd> <dt>

<span id="_netmon_network_driver_interface_specification_gly"></span><span id="_NETMON_NETWORK_DRIVER_INTERFACE_SPECIFICATION_GLY"></span>**NDIS (Network Driver Interface Specification)**
</dt> <dd>

Spécification de l’interface entre les pilotes de périphérique et un réseau. Tous les transports appellent l’interface NDIS pour accéder à et utiliser des cartes d’interface réseau.

</dd> <dt>

<span id="_netmon_network_monitor_agent_gly"></span><span id="_NETMON_NETWORK_MONITOR_AGENT_GLY"></span>**Agent de Moniteur réseau**
</dt> <dd>

Composant Moniteur réseau. L’agent permet à un ordinateur distant de capturer des données à partir du réseau. Lorsqu’une installation Moniteur réseau se connecte à distance à l’agent Moniteur réseau et lance une capture, les statistiques de la capture sont transférées sur le réseau vers l’ordinateur de gestion. Le transfert se poursuit à intervalles spécifiés lorsque la connexion est établie.

</dd> <dt>

<span id="_netmon_network_packet_provider_gly"></span><span id="_NETMON_NETWORK_PACKET_PROVIDER_GLY"></span>**fournisseur de paquets réseau (NPP)**
</dt> <dd>

Le composant Moniteur réseau qui collecte le trafic réseau dans les trames, puis transmet les trames à un expert et à une application NPP. Un NPP utilise le pilote de système de Moniteur réseau (Nmnt.sys) pour récupérer les trames collectées sur le réseau et fournit plusieurs interfaces COM qui transmettent les trames à un expert, une analyse et une application de fournisseur de paquets réseau (NPP) où elles peuvent être affichées et analysées.

</dd> <dt>

<span id="_netmon_npp_gly"></span><span id="_NETMON_NPP_GLY"></span>**NPP**
</dt> <dd>

Consultez fournisseur de paquets réseau.

</dd> <dt>

<span id="_netmon_npp_application_gly"></span><span id="_NETMON_NPP_APPLICATION_GLY"></span>**Application NPP**
</dt> <dd>

Une application qui contourne à la fois l’Moniteur réseau l’outil de contrôle de l’interface utilisateur et du contrôle d’analyse et se connecte directement au fournisseur de paquets réseau (NPP). Une application NPP peut se connecter au composant NPP avec l’une des cinq interfaces COM NPP.

</dd> <dt>

<span id="_netmon_npp_finder_gly"></span><span id="_NETMON_NPP_FINDER_GLY"></span>**Recherche NPP**
</dt> <dd>

Composant Moniteur réseau qui communique avec NPPs.

</dd> </dl>

 

 



