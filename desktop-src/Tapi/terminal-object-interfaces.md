---
description: Les interfaces d’objet terminal offrent à une application l’accès pour manipuler les appareils utilisés pour créer ou recevoir des flux multimédias.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Interfaces d’objet terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f8a80e088e6182416364798a4a8cfa5d3ebeafaa8d9ccb23c53bc56655d39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118860527"
---
# <a name="terminal-object-interfaces"></a>Interfaces d’objet terminal

Les interfaces d' [objet terminal](terminal-object.md) offrent à une application l’accès pour manipuler les appareils utilisés pour créer ou recevoir des flux multimédias.

Ces interfaces sont implémentées par un MSP et ne sont pas disponibles si l’adresse n’est pas prise en charge par un fournisseur de services de média. Si un MSP associé existe, l’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) est exposée sur l' [objet Address](address-object.md).

Les interfaces [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) et [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) ne sont pas directement exposées sur l’objet terminal, mais sont étroitement liées à celle-ci et sont répertoriées ici pour des raisons de commodité de référence.



| Interface                                                                  | Description                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Interface de base pour l’objet terminal. Il fournit des méthodes pour obtenir des informations telles que la classe de terminal et le support pris en charge. |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | définit et obtient DirectShow format multimédia.                                                                                            |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Fournit des méthodes pour définir et récupérer des caractéristiques de terminal audio standard, telles que le volume.                                          |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Énumère [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal).                                                                                      |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Énumère la [**classe terminal**](terminal-class.md).                                                                              |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Énumère [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo).                                        |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Énumère [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo).                                                  |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Récupère et définit les informations relatives aux pistes des terminaux de fichiers.                                                                   |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Récupère la description des événements de terminal de reconnaissance vocale automatique.                                                        |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Récupère la description des événements de terminal de fichier.                                                                                |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Énumère, crée ou supprime des pistes sur les terminaux multipiste.                                                                   |



 



| Interface                                                                                      | Description                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Récupère des informations concernant un terminal enfichable.                                                                       |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Crée, modifie ou supprime l’entrée de Registre pour un terminal enfichable.                                                   |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Effectue la création d’un objet terminal principal pour les terminaux enfichables, ce qui permet au gestionnaire de terminal d’initialiser le terminal. |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Récupère le nom et le CLSID d’une classe de terminal enfichable.                                                                  |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Récupère et définit des informations sur une superclasse de terminal (nom et CLSID).                                                 |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Avertit les applications clientes des modifications apportées à un terminal enfichable.                                                          |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Inscrit et annule l’inscription d’une application cliente à des fins de notification concernant les événements de terminal enfichables.                             |



 



| Interface                                            | Description                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Récupère la description des événements de terminal de conversion de texte par synthèse vocale (TTS). |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Récupère des informations sur un événement de détection de tonalité.                |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Récupère la description des événements de terminal de tonalité.                 |



 

 

 
