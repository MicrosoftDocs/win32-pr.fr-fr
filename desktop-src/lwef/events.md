---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031162"
---
# <a name="iagentnotifysink"></a>IAgentNotifySink

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

IAgentNotifySink notifie les clients lorsque certains changements d’État se produisent. Ces fonctions sont également disponibles à partir de [IAgentNotifySinkEx](iagentnotifysinkex.md).

**Méthodes dans l'ordre Vtable**



| IAgentNotifySink                                                      | Description                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**Commande**](command-method.md)                                     | Se produit lorsque le serveur traite une commande définie par le client.                               |
| [**ActivateInputState**](iagentnotifysink--activateinputstate.md)    | Se produit lorsqu’un caractère devient ou cesse d’être actif.                            |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Se produit lorsque l’état **visible** du caractère change.                                   |
| [**Événement clic**](click-event.md)                                    | Se produit lors d’un clic sur un caractère.                                                      |
| [**DblClick, événement**](dblclick-event.md)                              | Se produit lors d’un double-clic sur un caractère.                                               |
| [**DragStart**](/windows/desktop/lwef/dragstart-event)                                | Se produit lorsqu’un utilisateur commence à faire glisser un caractère.                                          |
| [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)                          | Se produit lorsqu’un utilisateur arrête de faire glisser un caractère.                                           |
| [**RequestStart**](iagentnotifysink--requeststart.md)                | Se produit lorsque le serveur commence à traiter un objet de [**requête**](/windows/desktop/lwef/the-request-object) .    |
| [**RequestComplete**](iagentnotifysink--requestcomplete.md)          | Se produit lorsque le serveur termine le traitement d’un objet de [**requête**](/windows/desktop/lwef/the-request-object) . |
| [**Signet**](iagentnotifysink--bookmark.md)                        | Se produit lorsque le serveur traite un signet.                                             |
| [**Périodes**](iagentnotifysink--idle.md)                                | Se produit lorsque le serveur démarre ou termine le traitement de l’inactivité.                                   |
| [**Activer**](iagentnotifysink--move.md)                                | Se produit lorsqu’un caractère a été déplacé.                                                  |
| [**Taille**](iagentnotifysink---size.md)                               | Se produit lorsqu’un caractère a été redimensionné.                                                |
| [**BalloonVisibleState**](iagentnotifysink---balloonvisiblestate.md) | Se produit lorsque l’état de visibilité de la bulle de texte d’un caractère change.                  |



 

Les événements IAgentNotifySink :: restart et IAgentNotifySink :: Shutdown, pris en charge dans les versions antérieures de Microsoft Agent, sont désormais obsolètes. Bien qu’pris en charge pour la compatibilité descendante, le serveur n’envoie plus ces événements.

 

 