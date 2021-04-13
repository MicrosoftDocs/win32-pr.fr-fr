---
title: Client Input-Active
description: Client Input-Active
ms.assetid: b46e91d3-eca7-4a4a-b1ce-27b5e6ad92a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3223ddc7bb412b333d628f93cc56b27efd0abb7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310666"
---
# <a name="input-active-client"></a>Client Input-Active

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Étant donné que plusieurs applications clientes peuvent partager le même caractère et que plusieurs clients peuvent utiliser des caractères différents en même temps, le serveur désigne un client en tant que client *d’entrée-actif* et envoie une entrée de la souris et de la voix uniquement à cette application cliente. Cela permet de gérer la gestion ordonnée des entrées utilisateur, afin qu’un client approprié réponde à l’entrée.

En règle générale, l’interaction de l’utilisateur détermine l’application cliente qui devient active en entrée. Par exemple, si l’utilisateur clique sur un caractère, l’application cliente de ce caractère devient entrée-active. De même, si un utilisateur parle du nom d’un caractère, il devient en entrée-actif. En outre, lorsque le serveur traite la méthode [**Show**](show-method.md) d’un caractère, le client de ce caractère devient Input-active.

Lorsqu’un caractère est masqué, le client de ce caractère n’est plus en entrée-actif pour ce caractère. Le serveur rend automatiquement le client actif de tous les caractères restants en entrée-actif. Lorsque tous les caractères sont masqués, aucun client n’est en entrée-actif. Toutefois, dans cette situation, si l’utilisateur appuie sur la touche d’écoute, l’agent continue à écouter ses commandes (à l’aide du moteur de reconnaissance vocale qui correspond au premier caractère du dernier client d’entrée-actif).

Si plusieurs clients partagent le même caractère, le serveur désigne son *client actif* en tant que client d’entrée-actif. Le caractère actif est le plus haut dans l’ordre du client. Vous pouvez définir votre client comme client actif ou non actif à l’aide de la méthode [**Activate**](activate-method.md) . Vous pouvez également utiliser la méthode **Activate** pour rendre votre client en entrée-active de manière explicite ; mais pour éviter d’interrompre les autres clients du personnage, vous devez le faire uniquement lorsque votre application cliente est active. Par exemple, si l’utilisateur clique sur la fenêtre de votre application, en activant votre application, vous pouvez appeler la méthode **Activate** pour recevoir et traiter l’entrée de la souris et de la parole dirigée vers le caractère.

 

 




