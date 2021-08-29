---
description: Les rubriques suivantes décrivent comment utiliser l’API ETW pour le suivi d’événements.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Utilisation du suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de647796862f5b7d5e9477e03c098af7e4463a00973d3055199369c517d3bd62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083119"
---
# <a name="using-event-tracing"></a>Utilisation du suivi d’événements

Les rubriques suivantes décrivent comment utiliser l’API ETW pour le suivi d’événements.



| Rubrique                                                                          | Description                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Contrôle des sessions de suivi d’événements](controlling-event-tracing-sessions.md)   | Décrit comment gérer les sessions de suivi d’événements.                                                                         |
| [Fournir des événements](providing-events.md)                                       | Décrit comment inscrire et instrumenter un fournisseur de suivi d’événements.                                                       |
| [Événements de consommation](consuming-events.md)                                       | Décrit comment implémenter des fonctions de rappel utilisées pour consommer et traiter des événements à partir d’un fichier journal de suivi ou en temps réel. |
| [Windows Préprocesseur de trace logiciel](windows-software-trace-preprocessor.md) | Fournit un mécanisme efficace pour consigner et consommer des événements qui se produisent pendant l’exécution d’une application ou d’un pilote.  |



 

Incluez le fichier d’en-tête Wmistr. h avant d’inclure le fichier d’en-tête Evntrace. h.

 

 



