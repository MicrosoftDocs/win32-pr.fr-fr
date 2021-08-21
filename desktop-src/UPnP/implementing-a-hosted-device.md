---
title: Implémentation d’un appareil hébergé
description: L’hôte d’appareil avec la technologie UPnP implémente la détection, la description, le contrôle et les événements des principaux protocoles UPnP.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fd12788c40d21dc84e896f1aba83085b440b86fbb54b68b4fbcfddbbe910c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008049"
---
# <a name="implementing-a-hosted-device"></a>Implémentation d’un appareil hébergé

L’hôte d’appareil avec la technologie UPnP implémente les principaux protocoles UPnP : découverte, description, contrôle et événement. Le développeur qui implémente un appareil hébergé doit uniquement fournir les éléments suivants :

-   Description de l’appareil et de ses services.
-   Implémentation de la fonctionnalité de l’appareil.

Par exemple, le développeur d’un appareil horloge doit fournir des descriptions de service et d’appareil UPnP, ainsi qu’une implémentation des fonctions d’horloge (telles que la conservation de l’heure, la définition du temps et la réponse aux requêtes pour l’heure actuelle). L’hôte de l’appareil :

-   Annonce l’appareil conformément au protocole de découverte UPnP.
-   Répond aux requêtes de la description de l’appareil.
-   Achemine les demandes de contrôle vers la partie du code de l’appareil qui implémente les fonctions d’horloge.
-   Gère les abonnements aux services.
-   Envoie des notifications d’événements aux abonnés lorsque l’état du service change.

 

 




