---
title: Traduction de la coordonnée d’événement
description: Traduction de la coordonnée d’événement
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843c2e5a3f978f405a3c126ef6a246024b55ccd2f73fbf86a8eed285b6181169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993139"
---
# <a name="event-coordinate-translation"></a>Traduction de la coordonnée d’événement

La spécification 96 pour les contrôles exige que les coordonnées passées pour les événements déclenchés par le contrôle changent d’être HIMETRIC à des points basés. Cette modification amène l’événement à passer des coordonnées en ligne avec les propriétés et les méthodes et, par conséquent, la coordination de la correspondance n’est plus la responsabilité du conteneur. Cela soulève certains problèmes de compatibilité lorsqu’un contrôle déclenche des événements à l’aide d’une base de coordonnées qu’il n’attend pas, cela ne doit être qu’un problème où un conteneur de contrôle 96 héberge un contrôle antérieur à 96, comme suit :

-   Quand un conteneur antérieur à 96 héberge un contrôle 96, le contrôle présente les coordonnées d’événement en tant que points. cela ne doit pas entraîner de problèmes au niveau du conteneur, car le conteneur doit reconnaître le type de paramètre.
-   Quand un conteneur 96 héberge un contrôle antérieur à 96, le contrôle présente le conteneur avec des coordonnées et s’attend à ce que la traduction du conteneur soit nécessaire. Toutefois, le conteneur 96 attendra un contrôle pour se conformer à la spécification de contrôles 96 et présentera ses coordonnées en tant que points. Le contrôle utilise la méthode [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) sur l’interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fournie par le conteneur de la même façon que pour les propriétés et les méthodes pour y parvenir.

Par conséquent, l’utilisateur d’un conteneur 96 hébergeant des contrôles antérieurs à 96 devra savoir qu’une traduction supplémentaire de coordonnées peut être nécessaire lorsque des événements sont déclenchés.

 

 




