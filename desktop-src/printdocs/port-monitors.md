---
description: Une fois qu’un pilote de périphérique a converti un fichier journal entier en commandes d’appareils brutes, le fichier de commandes converties est renvoyé au spouleur.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Moniteurs de port
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536494"
---
# <a name="port-monitors"></a>Moniteurs de port

Une fois qu’un pilote de périphérique a converti un fichier journal entier en commandes d’appareils brutes, le fichier de commandes converties est renvoyé au spouleur. Le spouleur envoie ces commandes de bas niveau à une analyse. Un moniteur de port est un fichier. dll qui transmet les commandes d’appareil brutes sur le réseau, via un port parallèle ou via un port série à l’appareil de l’imprimante. Des moniteurs de port personnalisés peuvent être installés pour prendre en charge le passage des données de l’appareil via d’autres ports de communication.

Utilisez les fonctions suivantes pour travailler avec les moniteurs de port.



| Fonction                               | Description                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Installe un moniteur de port local et relie les fichiers de configuration, de données et de surveillance. |
| [**DeleteMonitor**](deletemonitor.md) | Supprime un moniteur de port ajouté par la fonction [**AddMonitor**](addmonitor.md) .      |
| [**EnumMonitors**](enummonitors.md)   | Énumère les moniteurs de port installés sur un serveur spécifié.                       |



 

 

 



