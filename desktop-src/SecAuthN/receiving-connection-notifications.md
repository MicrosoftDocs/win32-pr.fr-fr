---
description: Certaines applications doivent recevoir la notification des événements de connexion avant l’événement, juste après qu’elle ait lieu, ou les deux. Vous pouvez créer une DLL pour recevoir la notification d’avance et de fin des événements de connexion.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Réception des notifications de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a581855ef134536df8c4c728521e796e541c963a780e2f572ad88dc704c677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919688"
---
# <a name="receiving-connection-notifications"></a>Réception des notifications de connexion

Certaines applications doivent recevoir la notification des événements de connexion avant l’événement, juste après qu’elle ait lieu, ou les deux. Vous pouvez créer une DLL pour recevoir la notification d’avance et de fin des événements de connexion.

Le service d’accès à distance (RAS) est un exemple d’application qui doit recevoir la notification préalable d’un événement de connexion. RAS doit être informé avant qu’une connexion soit établie, car il peut être nécessaire d’établir une connexion de modem avant d’établir la connexion réseau.

De même, les applications devront peut-être nettoyer les ressources une fois la connexion établie, ce qui nécessite une notification après la connexion.

Les applications qui souhaitent recevoir une notification anticipée et une notification après le fait des événements de connexion doivent fournir une DLL qui exporte deux fonctions, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) et [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).

Une fois ces fonctions implémentées, vous devez inscrire votre DLL comme décrit dans la rubrique [inscription pour recevoir des notifications de connexion](registering-to-receive-connection-notifications.md).

 

 



