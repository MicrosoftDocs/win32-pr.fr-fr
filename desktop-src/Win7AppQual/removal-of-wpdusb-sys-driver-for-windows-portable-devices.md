---
description: suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b5d1a815b97049816a618b9e93d0767e321fd60b689e6845318c1605574c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994739"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a>suppression du pilote de WPDUSB.SYS pour les appareils mobiles Windows

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows 7  
**serveurs** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

Microsoft a remplacé le composant mode noyau de la pile de pilotes USB Windows Vista (WPDUSB.SYS) pour les Windows les appareils mobiles (WPD) par le pilote WINUSB.SYS générique. La communication avec le pilote de WPDUSB.SYS d’origine était par le biais de codes de contrôle d’e/s privés (IOCTL). la prise en charge de ces derniers a également été supprimée.

Tout consommateur de ces codes IOCTL aurait été responsable de l’interprétation et de l’implémentation appropriées du protocole MTP (Media Transfer Protocol). Windows Vista ne prenait pas en charge l’utilisation de ces codes IOCTL par les applications tierces.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

Toute application qui dépendait de la disponibilité de ces codes IOCTL privés n’aura plus accès aux périphériques MTP connectés par USB.

## <a name="mitigation"></a>Limitation des risques

Les utilisateurs d’une application qui dépend des codes IOCTL privés doivent utiliser une application différente (ou une version mise à jour de l’application) pour accéder à l’appareil MTP USB.

## <a name="solution"></a>Solution

les Applications doivent utiliser l’API Windows des appareils mobiles (WPD) pour rechercher et interagir avec n’importe quel appareil WPD. Bien qu’un pourcentage important d’appareils WPD implémentent MTP pour la communication avec le PC, WPD n’est pas limité aux seuls appareils MTP. En outre, lorsque l’accès direct à l’appareil via les IOCTL privées aurait limité l’application à la communication avec uniquement les périphériques connectés par USB, l’utilisation de l’API WPD étend la liste des options de connectivité à d’autres protocoles de communication (par exemple, Wi-Fi). Dans les rares cas où l’application doit prendre en charge la MTP, l’API WPD fournit un mécanisme direct pour les commandes MTP brutes.

## <a name="leveraging-feature-capabilities"></a>Exploitation des fonctionnalités de fonctionnalités

l’API WPD est prise en charge dans Windows XP (via le kit de développement logiciel (SDK) Windows Format), Windows Vista et Windows 7. l’implémentation Windows 7 d’WPD ajoute la prise en charge de MTP sur Bluetooth.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

[Windows Appareils mobiles](../windows-portable-devices.md)

 

 
