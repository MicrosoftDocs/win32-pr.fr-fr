---
description: Le fournisseur principal WMI définit des classes qui composent les fonctionnalités de base de WMI.
ms.assetid: 6EEA4284-CCFE-4206-9EAA-B4BCF988DE03
title: Fournisseur WMI Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9927be7208d9133d65257292950913972e96483
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403593"
---
# <a name="wmi-core-provider"></a>Fournisseur WMI Core

Le fournisseur principal WMI définit des classes qui composent les fonctionnalités de base de WMI.

La plupart des classes de fournisseur WMI Core contiennent des données fournies par le [fournisseur WDM](wdm-provider.md)et décrivent des moniteurs d’affichage. Les classes sont définies dans WMI. mof et se trouvent dans l’espace de \\ noms WMI racine.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                           | Description                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSMonitorClass**](msmonitorclass.md)<br/>                                             | est une classe de base WMI abstraite. Les classes qui décrivent les moniteurs d’affichage vidéo héritent de cette [**MSMonitorClass**](msmonitorclass.md).<br/>                                                                         |
| [Classes MSMCA](msmca-classes.md)<br/>                                                   | ensemble de classes WMI qui exposent l’architecture de vérification automatique (MCA). La couche d’abstraction système (SAL) fournit tous les événements signalés dans la classe MSMCA. Intel Corporation développe et possède l’MCA.<br/>         |
| [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md)<br/>                         | représente un conteneur pour les caractéristiques d’une plage de fréquences prise en charge.<br/>                                                                                                                                          |
| [**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)<br/>     | représente les fonctionnalités d’affichage prises en charge de l’analyse.<br/>                                                                                                                                                           |
| [**VideoModeDescriptor**](videomodedescriptor.md)<br/>                                   | contient des éléments de descripteur de mode pour le tableau **MonitorSourceModes** dans la classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .<br/>                                           |
| [**WMIEvent**](wmievent.md)<br/>                                                         | La classe [**WmiEvent**](wmievent.md) est une classe de base à partir de laquelle toutes les classes d’événements WMI sont dérivées.<br/>                                                                                                                |
| [**WmiMonitorAnalogVideoInputParams**](wmimonitoranalogvideoinputparams.md)<br/>         | représente les paramètres d’entrée de vidéo analogique d’un moniteur d’ordinateur.<br/>                                                                                                                                                 |
| [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md)<br/>                 | représente les fonctionnalités d’affichage de base d’un moniteur d’ordinateur.<br/>                                                                                                                                                        |
| [**WmiMonitorBrightness**](wmimonitorbrightness.md)<br/>                                 | représente les paramètres de luminosité d’un moniteur d’ordinateur.<br/>                                                                                                                                                         |
| [**WmiMonitorBrightnessEvent**](wmimonitorbrightnessevent.md)<br/>                       | représente une modification de la luminosité d’une analyse.<br/>                                                                                                                                                                 |
| [**WmiMonitorBrightnessMethods**](wmimonitorbrightnessmethods.md)<br/>                   | contient des méthodes qui gèrent la luminosité de l’analyse.<br/>                                                                                                                                                                    |
| [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md)<br/>             | représente les caractéristiques de couleur CIE (International Commission on illumination) d’un moniteur d’ordinateur.<br/>                                                                                                          |
| [**WmiMonitorConnectionParams**](wmimonitorconnectionparams.md)<br/>                     | contient le type de connexion du moniteur.<br/>                                                                                                                                                                        |
| [**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)<br/>                   | contient des méthodes qui obtiennent le contenu brut de la définition d’entrée vidéo de la norme VESA (Video Electronics standard Association) (E-EDID) améliorée des données d’identification d’affichage étendu (E-EDID) v. 1. x blocs de données 128 octets standard.<br/> |
| [**WmiMonitorDigitalVideoInputParams**](wmimonitordigitalvideoinputparams.md)<br/>       | représente les paramètres d’entrée de la vidéo numérique.<br/>                                                                                                                                                                      |
| [**WmiMonitorID**](wmimonitorid.md)<br/>                                                 | représente les informations d’identification relatives à un moniteur vidéo, telles que le nom du fabricant, l’année de fabrication ou le numéro de série.<br/>                                                                                     |
| [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md)<br/>           | répertorie les plages de fréquences prises en charge par l’analyse.<br/>                                                                                                                                                                |
| [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md)<br/> | répertorie les modes source pris en charge pour un moniteur vidéo dans son descripteur de moniteur, le cas échéant.<br/>                                                                                                                       |
| [**WmiMonitorRawEEdidV1Block**](wmimonitorraweedidv1block.md)<br/>                       | représente les données brutes d’une structure E-EDID (Extended Display Identification Data) améliorée d’une association Video Electronics standard Association (VESA).<br/>                                                                      |
| [**XYZinCIE**](xyzincie.md)<br/>                                                         | contient les coordonnées de l’affichage dans l’espace de couleurs CIE (International Commission on illumination) XYZ.<br/>                                                                                                      |



 

 

 




