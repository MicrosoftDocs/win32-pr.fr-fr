---
description: .
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d602c8277a5c256332b3eaec6a383997d5c63d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519526"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>Suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**Serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

Microsoft a remplacé le composant mode noyau de la pile de pilotes USB Windows Vista (WPDUSB.SYS) pour les appareils mobiles Windows (WPD) par le pilote de WINUSB.SYS générique. La communication avec le pilote de WPDUSB.SYS d’origine était par le biais de codes de contrôle d’e/s privés (IOCTL). la prise en charge de ces derniers a également été supprimée.

Tout consommateur de ces codes IOCTL aurait été responsable de l’interprétation et de l’implémentation appropriées du protocole MTP (Media Transfer Protocol). Windows Vista ne prenait pas en charge l’utilisation de ces codes IOCTL par des applications tierces.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Toute application qui dépendait de la disponibilité de ces codes IOCTL privés n’aura plus accès aux périphériques MTP connectés par USB.

## <a name="mitigation"></a>Limitation des risques

Les utilisateurs d’une application qui dépend des codes IOCTL privés doivent utiliser une application différente (ou une version mise à jour de l’application) pour accéder à l’appareil MTP USB.

## <a name="solution"></a>Solution

Les applications doivent utiliser l’API des appareils mobiles Windows (WPD) pour rechercher et interagir avec n’importe quel appareil WPD. Bien qu’un pourcentage important d’appareils WPD implémentent MTP pour la communication avec le PC, WPD n’est pas limité aux seuls appareils MTP. En outre, lorsque l’accès direct à l’appareil via les IOCTL privées aurait limité l’application à la communication avec uniquement les périphériques connectés par USB, l’utilisation de l’API WPD étend la liste des options de connectivité à d’autres protocoles de communication (par exemple, Wi-Fi). Dans les rares cas où l’application doit prendre en charge la MTP, l’API WPD fournit un mécanisme direct pour les commandes MTP brutes.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

L’API WPD est prise en charge dans Windows XP (via le kit de développement logiciel (SDK) Windows format), Windows Vista et Windows 7. L’implémentation de Windows 7 d’WPD ajoute la prise en charge de MTP sur Bluetooth.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

[Appareils mobiles Windows](../windows-portable-devices.md)

 

 
