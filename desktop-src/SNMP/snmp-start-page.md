---
title: Service SNMP
description: L’implémentation Microsoft Windows du protocole SNMP (simple Network Management Protocol) est utilisée pour configurer des appareils distants, surveiller les performances du réseau, auditer l’utilisation du réseau et détecter les erreurs réseau ou un accès inapproprié. Important l’API Microsoft Windows SNMP ne prend en charge que les versions de protocole jusqu’à SNMPv2C. Elle ne prend pas en charge les versions ultérieures du protocole.
ms.assetid: fbaddb10-804b-4230-8986-717edc19a2f5
keywords:
- SNMP SNMP
- SNMP SNMP, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71df55c79244c0f74ef685271834adc01ca7e981
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031737"
---
# <a name="snmp-service"></a>Service SNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

## <a name="purpose"></a>Objectif

L’implémentation Microsoft Windows du protocole SNMP (simple Network Management Protocol) est utilisée pour configurer des appareils distants, surveiller les performances du réseau, auditer l’utilisation du réseau et détecter les erreurs réseau ou un accès inapproprié.

> [!IMPORTANT]
> L’API Microsoft Windows SNMP ne prend en charge que les versions de protocole allant jusqu’à SNMPv2C. Elle ne prend pas en charge les versions ultérieures du protocole.

 

## <a name="where-applicable"></a>Le cas échéant

SNMP utilise une architecture distribuée composée d’applications de gestion et d’applications d’agent. Le service SNMP implémente un agent SNMP. Pour utiliser les informations fournies par le service SNMP, vous devez disposer d’au moins un ordinateur hôte exécutant une application de gestion SNMP. Vous pouvez utiliser un logiciel de gestion SNMP tiers ou vous pouvez développer votre propre application de gestion SNMP. Les API suivantes sont disponibles à cet effet :

-   API de gestion SNMP, un ensemble de fonctions qui peuvent être utilisées pour développer rapidement des systèmes de gestion SNMP de base
-   API WinSNMP, version 2,0, un ensemble de fonctions pour l’encodage, le décodage, l’envoi et la réception de messages SNMP

En outre, l’API de l’agent d’extension SNMP définit l’interface entre le service SNMP et les dll d’agent d’extension SNMP tierces. Les fonctions de l’API de l’utilitaire SNMP peuvent être utilisées pour simplifier le traitement des messages SNMP.

## <a name="developer-audience"></a>Développeurs concernés

Les API répertoriées dans la section précédente sont conçues pour être utilisées par les programmeurs C/C++. Vous devez vous familiariser avec SNMP et SNMPv2C, ainsi que pour connaître les concepts de gestion de réseau et de réseau.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur le système d’exploitation requis pour utiliser une fonction particulière, consultez la section Configuration requise de la page de référence pour cette fonction.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                | Description                                                                                                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nouveautés dans SNMP](new-in-snmp.md)<br/>                                                            | Informations sur les mises à jour de SNMP.<br/>                                                                                                      |
| [Simple Network Management Protocol (SNMP)](simple-network-management-protocol-snmp-.md)<br/> | Informations et informations de référence sur l’API pour SNMP, y compris l’API de gestion SNMP, l’API de l’agent d’extension SNMP et les fonctions de l’API de l’utilitaire SNMP.<br/> |
| [API WinSNMP](snmp-reference.md)<br/>                                                         | Informations et informations de référence sur l’API pour l’interface de programmation d’applications SNMP Microsoft Windows (API WinSNMP). <br/>                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Protocole DHCP (Dynamic Host Configuration Protocol)](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[Gestion du réseau](/windows/desktop/NetMgmt/network-management)
</dt> <dt>

[Service de routage et d’accès à distance](/windows/desktop/RRAS/portal)
</dt> </dl>

 

