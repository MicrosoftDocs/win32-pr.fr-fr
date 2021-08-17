---
title: Gel des événements
description: Gel des événements
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba439ebce12a48d78e1eb1d2daa31990c02f4a42082d3425e9b6ef2f842b3ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736799"
---
# <a name="event-freezing"></a>Gel des événements

Un conteneur peut notifier un contrôle qu’il n’est pas prêt à répondre aux événements en appelant [**IOleControl :: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec **true**. Il peut libérer les événements en appelant **FreezeEvents** avec **false**. Lorsqu’un conteneur gèle des événements, il fige le traitement des événements, pas la réception d’événements ; autrement dit, un conteneur peut toujours recevoir des événements tandis que les événements sont figés. Si un conteneur reçoit une notification d’événement alors que ses événements sont figés, le conteneur doit ignorer l’événement. Aucune autre action n’est appropriée.

Un contrôle doit prendre note de l’appel d’un conteneur à [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec **true** s’il est important pour le contrôle qu’un événement ne soit pas manqué. Tandis que le traitement des événements d’un conteneur est figé, un contrôle doit implémenter l’une des techniques suivantes :

-   Déclenchez les événements dans la connaissance totale selon laquelle le conteneur n’effectuera aucune action.
-   Ignorer tous les événements que le contrôle aurait déclenchés.
-   Met en file d’attente tous les événements en attente et les déclenche après que le conteneur a appelé [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec la **valeur false**.
-   Met en file d’attente uniquement les événements pertinents ou importants et les déclenche après que le conteneur a appelé [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) avec la **valeur false**.

Chaque technique est acceptable et appropriée dans différentes circonstances. Le développeur de contrôle est responsable de la détermination et de l’implémentation de la technique appropriée pour les fonctionnalités du contrôle.

 

 




