---
title: Interfaces NLM
description: Interfaces NLM
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322086a2860ff9bade47c9971662931f9ecada60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119417"
---
# <a name="nlm-interfaces"></a>Interfaces NLM

Voici les interfaces NLM.

| Interface                                                            | Description                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Fournit un énumérateur standard pour les connexions réseau. Il énumère les connexions actives, déconnectées ou toutes les connexions réseau au sein d’un réseau. Cette interface peut être obtenue à partir de l’interface [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) . |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Énumère tous les réseaux disponibles sur le serveur. Cette interface peut être obtenue à partir de l’interface [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) .                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Représente un réseau sur le serveur. Il peut également représenter une collection de connexions réseau avec une signature réseau similaire.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Représente une connexion réseau unique.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Utilisé pour interroger le coût réseau actuel et l’état du plan de données associé à une connexion.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Utilisé pour notifier une application de coûts et d’événements de changement d’État du plan de données pour une connexion.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Interface de récepteur qu’un client implémente pour recevoir des événements liés aux connexions réseau. Les applications qui s’intéressent à des événements de niveau granulaire inférieurs tels que les modifications d’authentification, implémentent cette interface.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Utilisé pour interroger les informations sur l’état du coût et du plan de données au niveau de l’ordinateur associées à une connexion utilisée pour la connectivité Internet à l’ensemble de l’ordinateur ou au premier tronçon de routage vers une destination spécifique sur une connexion. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Utilisé pour notifier une application d’événements liés aux coûts et aux plans de données à l’ensemble de l’ordinateur.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Interface de récepteur qu’un client implémente pour recevoir des événements liés au réseau. Ces API sont toutes des fonctions de rappel qui sont appelées automatiquement lorsque les événements respectifs sont déclenchés.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Fournit un ensemble de méthodes pour exécuter des fonctions de gestion des listes de réseaux.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Interface de récepteur qu’un client implémente pour recevoir des événements liés au gestionnaire de listes de réseaux. Les applications qui s’intéressent à des événements de niveau granulaire plus élevés tels que la connectivité Internet, implémentent l’interface.   |



 

 

 




