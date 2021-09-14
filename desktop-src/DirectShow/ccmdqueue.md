---
description: La classe CCmdQueue est une classe de base qui fournit une file d’attente d’objets et de fonctions membres CDeferredCommand pour ajouter, supprimer, vérifier l’État et appeler les commandes mises en file d’attente.
ms.assetid: 6bd0f0f3-3c56-47d2-9fd8-e2863a2afa33
title: CCmdQueue, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue
api_type:
- COM
api_location: ''
ms.openlocfilehash: 78af7a975d54ba832bbdf1fb7f8027f87b747660
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012288"
---
# <a name="ccmdqueue-class"></a>CCmdQueue, classe

La `CCmdQueue` classe est une classe de base qui fournit une file d’attente d’objets [**CDeferredCommand**](cdeferredcommand.md) et des fonctions membres pour ajouter, supprimer, vérifier l’État et appeler les commandes mises en file d’attente. Un `CCmdQueue` objet fait partie d’un objet qui implémente des méthodes [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . Le gestionnaire de graphes de filtre implémente les méthodes **IQueueCommand** afin que les applications puissent mettre les commandes en file d’attente dans le graphique de filtre. Les filtres qui implémentent l’interface **IQueueCommand** utilisent directement cette classe. Si vous souhaitez utiliser des objets **CDeferredCommand** , votre file d’attente doit être dérivée de cette classe.

Il existe deux modes de synchronisation : grossiste et précis. En mode grossiste, l’application attend jusqu’à ce qu’une heure spécifiée arrive, puis exécute la commande. En mode exact, l’application attend que le traitement commence sur l’exemple qui s’affiche à l’heure, puis exécute la commande. Le filtre détermine celui qu’il doit implémenter. Le gestionnaire de graphes de filtre implémente toujours le mode grossiste pour les commandes mises en file d’attente au niveau du gestionnaire de graphique de filtre.

Si vous souhaitez une synchronisation grossière, vous souhaiterez probablement attendre qu’une commande soit en cours, puis l’exécuter. Pour ce faire, vous pouvez appeler [**CCmdQueue :: GetDueCommand**](ccmdqueue-getduecommand.md). Si vous avez plusieurs éléments à attendre, récupérez le descripteur d’événement à partir de [**CCmdQueue :: GetDueHandle**](ccmdqueue-getduehandle.md) , puis appelez **CCmdQueue :: GetDueCommand** quand ce est signalé. le [**temps de flux**](stream-time.md) est avancé uniquement entre les appels aux fonctions membres [**CCmdQueue :: Run**](ccmdqueue-run.md) et [**CCmdQueue :: EndRun**](ccmdqueue-endrun.md) . Il n’y a aucune garantie que si le descripteur est défini, une commande est prête. Chaque fois que l’événement est signalé, appelez la fonction membre **GetDueCommand** (probablement avec un délai d’expiration de zéro); Cela peut retourner E \_ Abort si aucune commande n’est prête.

Si vous souhaitez une synchronisation précise, appelez la fonction membre [**CCmdQueue :: GetCommandDueFor**](ccmdqueue-getcommandduefor.md) et transmettez les exemples que vous allez traiter en tant que paramètre. Cela retourne ce qui suit :

-   Commande de flux de temps due à ou avant cette heure de flux.
-   Commande au moment de la présentation due à ou avant la présentation du temps de flux. Procédez ainsi uniquement entre les fonctions membres [**CCmdQueue :: Run**](ccmdqueue-run.md) et [**CCmdQueue :: EndRun**](ccmdqueue-endrun.md) , car en dehors de ce, le mappage du temps de flux à l’heure de présentation n’est pas connu.
-   Toute commande de présentation en attente.

Si vous souhaitez une synchronisation précise des exemples qui peuvent être traités en mode suspendu, vous devez utiliser des commandes en continu.

Dans tous les cas, les commandes restent mises en file d’attente jusqu’à ce qu’elles soient appelées ou annulées. Le paramètre et la réinitialisation du descripteur d’événement sont gérés entièrement par cet objet de file d’attente.



| Membres de données protégés                                 | Description                                                                                            |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| m \_ bRunning                                            | Indicateur d’État en cours d’exécution ; Affectez la valeur **true** lors de l’exécution de.                                                     |
| m \_ dwAdvise                                            | Identificateur de notification de l’horloge de référence (zéro si aucune notification n’est en suspens).                            |
| m \_ evDue                                               | Définit l’heure d’échéance des commandes.                                                               |
| m \_ listPresentation                                    | Stocke les commandes mises en file d’attente au moment de la présentation.                                                           |
| m \_ listStream                                          | Stocke les commandes mises en file d’attente dans le temps de flux.                                                                 |
| \_verrou m                                                | Protège l’accès aux listes.                                                                              |
| m \_ pClock                                              | Horloge de référence actuelle.                                                                               |
| m \_ StreamTimeOffset                                    | Contient l’offset de temps de flux lorsque **m \_ bRunning** a la **valeur true**.                                      |
| m \_ StreamTimeOffset                                    | Contient l’offset de temps de flux lorsque **m \_ bRunning** a la **valeur true**.                                      |
| Fonctions de membre                                       | Description                                                                                            |
| [**CCmdQueue**](ccmdqueue-ccmdqueue.md)               | Construit un objet **CCmdQueue** .                                                                     |
| [**CheckTime**](ccmdqueue-checktime.md)               | Détermine si une heure donnée est due.                                                                     |
| [**GetDueHandle**](ccmdqueue-getduehandle.md)         | Récupère le handle d’événement qui sera signalé.                                                      |
| Fonctions membres substituables                           | Description                                                                                            |
| [**EndRun**](ccmdqueue-endrun.md)                     | Bascule en mode arrêté ou suspendu.                                                                    |
| [**GetCommandDueFor**](ccmdqueue-getcommandduefor.md) | Récupère une commande différée planifiée à une heure spécifiée.                                    |
| [**GetDueCommand**](ccmdqueue-getduecommand.md)       | Récupère un pointeur vers la commande suivante qui est due.                                                   |
| [**Insérer**](ccmdqueue-insert.md)                     | Ajoute l’objet [**CDeferredCommand**](cdeferredcommand.md) à la file d’attente.                             |
| [**Nouveau**](ccmdqueue-new.md)                           | Initialise une commande à exécuter et retourne un nouvel objet [**CDeferredCommand**](cdeferredcommand.md) . |
| [**Supprimer**](ccmdqueue-remove.md)                     | Supprime l’objet [**CDeferredCommand**](cdeferredcommand.md) de la file d’attente.                        |
| [**Exécuter**](ccmdqueue-run.md)                           | Bascule en mode exécution.                                                                              |
| [**SetSyncSource**](ccmdqueue-setsyncsource.md)       | Définit l’horloge utilisée pour le minutage.                                                                        |
| [**SetTimeAdvise**](ccmdqueue-settimeadvise.md)       | Configure un événement de minuterie avec l’horloge de référence.                                                        |



 

 

 



