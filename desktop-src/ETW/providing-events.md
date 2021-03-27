---
description: Les fournisseurs sont des applications qui contiennent l’instrumentation de traçage d’événements.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Fournir des événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972190"
---
# <a name="providing-events"></a>Fournir des événements

Les fournisseurs sont des applications qui contiennent l’instrumentation de traçage d’événements. Une fois qu’un fournisseur s’est inscrit lui-même, un contrôleur peut ensuite activer ou désactiver le suivi des événements dans le fournisseur. Le fournisseur définit son interprétation de l’activation ou de la désactivation. En général, un fournisseur activé génère des événements, et un fournisseur désactivé ne le fait pas. Cela vous permet d’ajouter le suivi d’événements à votre application sans qu’il ne soit nécessaire de générer des événements en permanence.

Cette section vous montre comment :

-   [Événements d’écriture](writing-events.md)
-   [Événements liés à l’écriture](writing-related-events-in-an-end-to-end-scenario.md)
-   [Publier votre schéma d’événement à partager avec les consommateurs](publishing-your-event-schema.md)

Pour plus d’informations sur le contrôle des sessions de suivi d’événements, consultez [contrôle des sessions de suivi d’événements](controlling-event-tracing-sessions.md). Pour plus d’informations sur l’utilisation des événements à partir d’un fournisseur de suivi d’événements, consultez [consommation d’événements](consuming-events.md).

 

 



