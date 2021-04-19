---
description: L’API graphique de pairs permet aux applications de transmettre des données entre les pairs de manière efficace et fiable. Les concepts de base de la technologie des graphiques homologues sont les nœuds d’un graphique d’homologue et les notifications d’événements.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: À propos de l’API graphique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517715"
---
# <a name="about-the-graphing-api"></a>À propos de l’API graphique

L’API graphique de pairs permet aux applications de transmettre des données entre les pairs de manière efficace et fiable. Les concepts de base de la technologie des graphiques homologues sont les **nœuds** d’un graphique d’homologue et les notifications d’événements.

## <a name="nodes"></a>Nœuds

Un nœud représente une instance spécifique d’un homologue sur un réseau. L’infrastructure de l’API de représentation graphique des homologues garantit que chaque nœud dispose d’une vue cohérente des données dans un graphique. Un nœud possède les fonctionnalités suivantes :

-   Peut se connecter à un nœud différent et former un réseau interdépendants appelé graphique homologue.
-   Peut partager des données avec d’autres nœuds dans un graphique sous la forme d’un [enregistrement](records.md).
-   Peut créer des connexions directes distinctes des graphiques d’homologues établis à l’aide de l' [API de regroupement](about-the-grouping-api.md)pair.
    > [!Note]  
    > Les connexions directes permettent aux nœuds d’envoyer des données privées les unes aux autres.

     

## <a name="event-notices"></a>Notifications d’événements

L’API de représentation graphique d’homologue dispose d’une infrastructure d’événements qui permet à une application de s’inscrire et de recevoir une notification d’un événement homologue dans l’infrastructure de l’API de représentation graphique des homologues. En cas de modification d’un graphique homologue, une application envoie un avis d’événement pour identifier qu’une modification s’est produite.

 

 



