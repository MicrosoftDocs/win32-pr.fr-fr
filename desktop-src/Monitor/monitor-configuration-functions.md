---
title: Surveiller les fonctions de configuration
description: Surveiller les fonctions de configuration
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- surveiller, fonctions
- surveiller, fonctions de haut niveau
- surveiller, fonctions de bas niveau
- surveiller, fonctions d’énumération
- fonctions de haut niveau
- fonctions de bas niveau
- fonctions d’énumération
- configuration de l’analyse, fonctions
- configuration de l’analyse, fonctions de haut niveau
- configuration de l’analyse, fonctions de bas niveau
- configuration de l’analyse, fonctions d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b4eca3e18b5a5254ef9adc8cd55e123c26a773149d323caf517c5429d972f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013437"
---
# <a name="monitor-configuration-functions"></a>Surveiller les fonctions de configuration

Les fonctions suivantes permettent d’obtenir des informations à partir d’une analyse et de modifier les paramètres d’un analyseur. Les fonctions de configuration du moniteur sont classées en fonctions de haut niveau, fonctions de bas niveau et fonctions d’énumération. Pour plus d’informations, consultez Utilisation de la [configuration de l’analyse](using-monitor-configuration.md).

## <a name="high-level-functions"></a>Fonctions High-Level



| Fonction                                                                         | Description                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DegaussMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Démagnétise une analyse.                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Récupère les paramètres de luminosité minimale, maximale et actuelle d’un analyseur.             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Récupère les fonctionnalités de configuration d’une analyse.                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Récupère la température de couleur actuelle d’un moniteur.                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Récupère les paramètres de contraste minimal, maximal et actuel d’un moniteur.               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Récupère la position minimale, maximale et horizontale actuelle d’un moniteur. |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Récupère la largeur ou la hauteur minimale, maximale et actuelle d’un moniteur.                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Récupère la valeur du lecteur rouge, vert ou bleu d’un moniteur.                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Récupère la valeur du gain rouge, vert ou bleu d’un moniteur.                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Récupère le type de technologie utilisé par une analyse.                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Restaure les paramètres d’usine des paramètres de couleur d’un moniteur.                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Restaure les paramètres d’usine des paramètres d’un analyseur.                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Enregistre les paramètres actuels du moniteur dans le stockage non volatile de l’affichage.             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Définit la valeur de luminosité d’un moniteur.                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Définit la température de couleur d’un moniteur.                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Définit la valeur de contraste d’un moniteur.                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Définit la position horizontale ou verticale de la zone d’affichage d’un moniteur.                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Définit la largeur ou la hauteur de la zone d’affichage d’un moniteur.                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Définit la valeur du lecteur rouge, vert ou bleu d’un moniteur.                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Définit la valeur du gain rouge, vert ou bleu d’un moniteur.                                     |



 

## <a name="low-level-functions"></a>Fonctions Low-Level



| Fonction                                                                                   | Description                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Récupère une chaîne décrivant les fonctionnalités d’un analyseur.                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Récupère la longueur de la chaîne de fonctionnalités d’un analyseur.                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Récupère les fréquences de synchronisation horizontale et verticale d’un moniteur.                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Récupère la valeur actuelle, la valeur maximale et le type de code d’un code du panneau de configuration virtuel (VCP) pour une analyse. |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Enregistre les paramètres actuels du moniteur dans le stockage non volatile de l’affichage.                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Définit la valeur d’un code du panneau de configuration virtuel (VCP) pour une analyse.                                            |



 

## <a name="enumeration-functions"></a>Fonctions d’énumération



| Fonction                                                                                                   | Description                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Ferme un handle vers une analyse physique.                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Ferme un tableau de handles de moniteur physiques.                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Récupère le nombre de moniteurs physiques associés à un handle de moniteur **HMONITOR** . |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Récupère le nombre de moniteurs physiques associés à un appareil Direct3D.              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Récupère les moniteurs physiques associés à un handle de moniteur **HMONITOR** .           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Récupère les moniteurs physiques associés à un appareil Direct3D.                        |



 

## <a name="internal-functions"></a>Fonctions internes

Les fonctions suivantes sont utilisées par l’API de configuration de l’analyse pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler ces fonctions.

-   [**DDCCIGetCapabilitiesString**](ddccigetcapabilitiesstring.md)
-   [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)
-   [**DDCCIGetTimingReport**](ddccigettimingreport.md)
-   [**DDCCIGetVCPFeature**](ddccigetvcpfeature.md)
-   [**DDCCISaveCurrentSettings**](ddccisavecurrentsettings.md)
-   [**DDCCISetVCPFeature**](ddccisetvcpfeature.md)
-   [**DestroyPhysicalMonitorInternal**](destroyphysicalmonitorinternal.md)
-   [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)
-   [**GetPhysicalMonitorDescription**](getphysicalmonitordescription.md)
-   [**GetPhysicalMonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de configuration de l’analyse](monitor-configuration-reference.md)
</dt> </dl>

 

 




