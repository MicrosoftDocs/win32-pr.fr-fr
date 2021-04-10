---
description: Les fonctions suivantes sont utilisées dans la gestion des périphériques.
ms.assetid: 3918ba49-1549-4f0c-b9fd-303ef46b810e
title: Fonctions de gestion des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587778b489b16355046b0b5af5cbba31c1a39639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950582"
---
# <a name="device-management-functions"></a>Fonctions de gestion des appareils

Les fonctions suivantes sont utilisées dans la gestion des périphériques.



| Fonction                                                             | Description                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)                           | Envoie un code de contrôle directement à un pilote de périphérique spécifié.                           |
| [**InstallNewDevice**](installnewdevice.md)                         | Installe un nouvel appareil. L’utilisateur est invité à sélectionner l’appareil.                     |
| [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)     | Inscrit l’appareil ou le type d’appareil pour lequel une fenêtre recevra des notifications. |
| [**UnregisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-unregisterdevicenotification) | Ferme le handle de notification de périphérique spécifié.                                      |



 

Les fonctions suivantes sont utilisées avec les lecteurs de CD-ROM et de DVD.



| Fonction                                                               | Description                                                                                         |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**CdromDisableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromdisabledigitalplayback)     | Désactive la lecture numérique pour le lecteur de CD-ROM ou de DVD spécifié.                                    |
| [**CdromEnableDigitalPlayback**](/windows/desktop/api/StorProp/nf-storprop-cdromenabledigitalplayback)       | Active la lecture numérique pour le lecteur de CD-ROM ou de DVD spécifié.                                     |
| [**CdromIsDigitalPlaybackEnabled**](/windows/desktop/api/StorProp/nf-storprop-cdromisdigitalplaybackenabled) | Détermine si la lecture numérique est activée pour le lecteur de CD-ROM ou de DVD spécifié.               |
| [**CdromKnownGoodDigitalPlayback**](/windows/desktop/api/Storprop/nf-storprop-cdromknowngooddigitalplayback) | Détermine si le lecteur de CD-ROM ou de DVD spécifié a une lecture numérique reconnue comme correcte. |
| [**DvdLauncher**](dvdlauncher.md)                                     | Vérifie que la région du média du lecteur de DVD correspond à la région du lecteur de DVD.                       |



 

 

 
