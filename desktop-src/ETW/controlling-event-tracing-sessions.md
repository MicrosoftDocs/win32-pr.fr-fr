---
description: Les sessions de suivi d’événements enregistrent des événements à partir d’un ou de plusieurs fournisseurs.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Contrôle des sessions de suivi d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5970eb160812991677aac775af60d08458c269152edca4aa2e30cdf30c111d96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130659"
---
# <a name="controlling-event-tracing-sessions"></a>Contrôle des sessions de suivi d’événements

Les sessions de suivi d’événements enregistrent des événements à partir d’un ou de plusieurs [fournisseurs](providing-events.md). Le contrôleur définit la session et active les fournisseurs. La définition de la session comprend généralement la spécification du nom de la session et du fichier journal, du type de fichier journal à utiliser et de la résolution de l’horodatage utilisé pour enregistrer les événements. Les contrôleurs peuvent également mettre à jour et interroger les sessions de suivi d’événements.

Les rubriques suivantes montrent comment définir et mettre à jour une session et activer les fournisseurs de suivi d’événements :

-   [Configuration et démarrage d’une session de suivi d’événements](configuring-and-starting-an-event-tracing-session.md)
-   [Configuration et démarrage d’une session SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configuration et démarrage d’une session de journalisation automatique](configuring-and-starting-an-autologger-session.md)
-   [Configuration et démarrage d’une session de journalisation privée](configuring-and-starting-a-private-logger-session.md)
-   [Mise à jour d’une session de suivi d’événements](updating-an-event-tracing-session.md)
-   [Récupération de données de suivi d’événements supplémentaires](retrieving-additional-event-tracing-data.md)

Pour plus d’informations sur le vidage et l’interrogation des sessions, consultez [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) et [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectivement.

Seuls les utilisateurs qui exécutent des privilèges d’administration élevés, les utilisateurs du groupe utilisateurs du journal de performances et les applications qui s’exécutent en tant que LocalSystem, LocalService ou NetworkService peuvent contrôler les sessions de suivi d’événements. Pour accorder à un utilisateur restreint la possibilité de contrôler les sessions de suivi, ajoutez-les au groupe utilisateurs du journal de performances.

**Windows XP et Windows 2000 :** Tout le monde peut contrôler une session de suivi.

 

 
