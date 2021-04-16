---
description: Réception d’une réponse
ms.assetid: 48919608-a102-43e2-9ca0-80b17344b5eb
title: Réception d’une réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9e05ec392b7db828ad1efd1360c4d4fb232210
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524180"
---
# <a name="receiving-a-response"></a>Réception d’une réponse

Étant donné que les composants mis en file d’attente sont conçus pour fonctionner de manière asynchrone, les applications clientes ne doivent pas se bloquer en attendant une réponse d’une demande en file d’attente. Néanmoins, il est souvent utile pour l’application cliente ou une application associée sur l’ordinateur client de recevoir une réponse. Par exemple, un client peut vouloir être averti lorsqu’une transaction demandée s’est terminée avec succès.

Un composant mis en file d’attente peut renvoyer une réponse de façon asynchrone à son appelant de différentes façons. Par exemple, il peut envoyer un message électronique. Le serveur peut également publier des événements faiblement couplés auxquels le client peut s’abonner.

Une autre façon pour un client d’obtenir une réponse à partir d’un composant mis en file d’attente qui s’exécute sur un serveur est que le client passe la méthode appelée à un objet de notification. Un objet de notification est une instance d’un composant mis en file d’attente qui s’exécute sur le client. Un tel objet de notification peut être assez simple, contenant uniquement un entier qui est utilisé pour représenter une valeur d’erreur, ou il peut être assez complexe, contenant toutes les informations nécessaires à la restauration d’une transaction sur le client. Dans les deux cas, le client appelant transmet un objet de notification en tant que paramètre d’entrée lorsqu’il désire une réponse d’un composant en file d’attente qui s’exécute sur un serveur. Étant donné que l’objet de notification est mis en file d’attente, le serveur peut appeler sur ses méthodes pour modifier son état, qui peut ensuite être lu par le client. Dans ce scénario, le service COM+ Queued Components est utilisé à la fois sur le client et sur le serveur pour autoriser les communications asynchrones dans les deux sens.

 

 



