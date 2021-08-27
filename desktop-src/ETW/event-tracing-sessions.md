---
description: Les sessions de suivi d’événements enregistrent les événements d’un ou plusieurs fournisseurs qu’un contrôleur active.
ms.assetid: 6e446ee3-47a3-4fe1-9eb7-3dd74cad4e56
title: Sessions de suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2edfe4bdfaf621575d8f2f8ab7d81a09aae8bfbddcb3f63890c4083378bb905b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083239"
---
# <a name="event-tracing-sessions"></a>Sessions de suivi d’événements

Les sessions de suivi d’événements enregistrent les événements d’un ou plusieurs [fournisseurs](providing-events.md) qu’un [contrôleur](controlling-event-tracing-sessions.md) active. La session est également responsable de la gestion et du vidage des mémoires tampons. Le contrôleur définit la session, qui comprend généralement la spécification du nom de la session et du fichier journal, du type de fichier journal à utiliser et de la résolution de l’horodatage utilisé pour enregistrer les événements.

Le suivi d’événements prend en charge un maximum de 64 sessions de suivi d’événements s’exécutant simultanément. De ces sessions, il existe deux sessions à usage spécial. Les sessions restantes sont disponibles pour une utilisation générale. Les deux sessions à usage spécial sont les suivantes :

-   Session d’enregistreur d’événements globale
-   Session d’enregistrement du noyau NT

La session de suivi d’événements de journalisation globale enregistre les événements qui se produisent au début du processus de démarrage du système d’exploitation, tels que ceux générés par les pilotes de périphérique. Pour plus d’informations sur la configuration de la session de suivi d’événements de journalisation globale, consultez [configuration et démarrage de la session de journalisation globale](configuring-and-starting-the-global-logger-session.md).

La session de suivi d’événements du journal du noyau NT enregistre les événements système prédéfinis générés par le système d’exploitation, par exemple, les e/s de disque ou les événements de défaillance de page. Pour plus d’informations sur la configuration de la session de suivi d’événements du journal de noyau NT, [configuration et démarrage de la session de journalisation du noyau NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Pour plus d’informations sur la définition d’une session de suivi d’événements standard, consultez [configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md).

**Windows 2000 :** Prend en charge uniquement les sessions de suivi d’événements 32.

 

 



