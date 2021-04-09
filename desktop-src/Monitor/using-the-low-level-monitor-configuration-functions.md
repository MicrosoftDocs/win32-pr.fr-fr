---
title: Utilisation des fonctions de configuration de l’analyseur de Low-Level
description: Utilisation des fonctions de configuration de l’analyseur de Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- surveiller, fonctions
- surveiller, fonctions de configuration de bas niveau
- surveiller, DDC/CI
- surveiller, afficher l’interface de commande de canal de données
- configuration de l’analyse, fonctions de configuration de bas niveau
- configuration de l’analyse, fonctions
- configuration de l’analyse, DDC/CI
- configuration de l’analyse, affichage de l’interface de commande du canal de données
- fonctions de configuration de bas niveau
- Afficher l’interface de commande du canal de données
- DDC/CI
- Jeu de commandes de contrôle du moniteur VESA (MCCS)
- Jeu de commandes du contrôle d’analyse (MCCS)
- MCCS (jeu de commandes du contrôle du moniteur)
- Panneau de configuration virtuel (VCP)
- VCP (panneau de configuration virtuel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940935"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Utilisation des fonctions de configuration de l’analyseur de Low-Level

Avant d’utiliser les fonctions de configuration de l’analyse de bas niveau, vous devez vous familiariser avec ces normes :

-   Afficher l’interface de commande de canal de données (DDC/CI)
-   Jeu de commandes de contrôle du moniteur VESA (MCCS)

Les fonctions de bas niveau fonctionnent en obtenant et en définissant les valeurs des codes du panneau de configuration virtuel (VCP). Un code VCP peut être *continu* ou *incontinu*. Les codes continus peuvent supposer toute valeur comprise entre zéro et une valeur maximale spécifique au fournisseur. Les codes non continus prennent en charge un ensemble défini de valeurs, qui est également spécifique au fournisseur.

Pour utiliser les fonctions de configuration de l’analyse de bas niveau, procédez comme suit :

1.  Obtenez un handle **HMONITOR** en appelant [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) ou [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).
2.  Appelez [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) pour connaître le nombre d’analyses physiques associées au descripteur **HMONITOR** .
3.  Appelez [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) pour obtenir la liste des descripteurs des analyses physiques.
4.  Appelez [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) pour obtenir la longueur de la chaîne de fonctionnalités DDC/ci d’un moniteur. La chaîne de fonctionnalités est une chaîne ASCII qui contient des informations statiques sur le moniteur. Une partie de la chaîne répertorie les codes VCP pris en charge par le moniteur. La chaîne répertorie également les valeurs prises en charge par les codes VCP qui ne sont pas continus.
5.  Allouez une mémoire tampon pour stocker la chaîne de fonctionnalités et appelez [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) pour obtenir la chaîne.
6.  Analyser la chaîne de fonctionnalités pour déterminer les codes VCP pris en charge par le moniteur.
7.  Pour un code VCP continu, appelez [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) pour obtenir les valeurs actuelles et maximales du code. Pour un code VCP non continu, analysez la chaîne Capabilities pour obtenir les valeurs prises en charge.
8.  Appelez [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) pour définir une nouvelle valeur pour un code VCP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation de la configuration de l’analyse**](using-monitor-configuration.md)
</dt> </dl>

 

 