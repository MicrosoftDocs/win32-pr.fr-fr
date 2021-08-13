---
description: Une fois qu’un pilote de périphérique a converti un fichier journal entier en commandes d’appareils brutes, le fichier de commandes converties est renvoyé au spouleur.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Moniteurs de port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470929"
---
# <a name="port-monitors"></a>Moniteurs de port

Une fois qu’un pilote de périphérique a converti un fichier journal entier en commandes d’appareils brutes, le fichier de commandes converties est renvoyé au spouleur. Le spouleur envoie ces commandes de bas niveau à une analyse. Un moniteur de port est un .dll qui transmet les commandes de l’appareil brut sur le réseau, via un port parallèle ou via un port série à l’appareil de l’imprimante. Des moniteurs de port personnalisés peuvent être installés pour prendre en charge le passage des données de l’appareil via d’autres ports de communication.

Utilisez les fonctions suivantes pour travailler avec les moniteurs de port.



| Fonction                               | Description                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Installe un moniteur de port local et relie les fichiers de configuration, de données et de surveillance. |
| [**DeleteMonitor**](deletemonitor.md) | Supprime un moniteur de port ajouté par la fonction [**AddMonitor**](addmonitor.md) .      |
| [**EnumMonitors**](enummonitors.md)   | Énumère les moniteurs de port installés sur un serveur spécifié.                       |



 

 

 



