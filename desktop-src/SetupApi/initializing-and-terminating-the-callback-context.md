---
description: Avant de pouvoir utiliser la routine de rappel de file d’attente par défaut, soit en la spécifiant comme routine de rappel lors de la validation d’une file d’attente de fichiers, soit en l’appelant à partir d’une routine de rappel personnalisée, elle doit être initialisée.
ms.assetid: e25a9787-a4a3-4d06-bf55-f6f7cfb23481
title: Initialisation et fin du contexte de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cb4c144cb9069d395ccd688e2a172680df8a12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521856"
---
# <a name="initializing-and-terminating-the-callback-context"></a>Initialisation et fin du contexte de rappel

Avant de pouvoir utiliser la routine de rappel de file d’attente par défaut, soit en la spécifiant comme routine de rappel lors de la validation d’une file d’attente de fichiers, soit en l’appelant à partir d’une routine de rappel personnalisée, elle doit être initialisée.

La fonction [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) crée la structure de contexte qui est utilisée par la routine de rappel de file d’attente par défaut. Elle retourne un pointeur void vers cette structure. Cette structure est essentielle pour l’opération de la routine de rappel par défaut et doit être passée à la routine de rappel. Vous pouvez le faire soit en spécifiant le pointeur void comme contexte dans un appel à [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), soit en spécifiant le pointeur void comme paramètre de contexte lors de l’appel de [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) à partir d’une routine de rappel personnalisée. Cette structure de contexte ne doit pas être modifiée ou référencée par l’application d’installation.

La fonction [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) initialise également un contexte pour la routine de rappel de file d’attente par défaut, mais elle spécifie une deuxième fenêtre pour recevoir un message de progression spécifié par l’appelant chaque fois que la file d’attente envoie une notification. Cela vous permet d’utiliser les boîtes de dialogue d’invite et d’erreur de disque par défaut et d’incorporer une barre de progression dans une deuxième fenêtre, par exemple dans une page d’un assistant d’installation.

Que vous ayez initialisé ou non le contexte utilisé par la routine de rappel de file d’attente par défaut avec [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex), une fois le traitement des opérations en file d’attente terminé, appelez [**SetupTermDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setuptermdefaultqueuecallback) pour libérer les ressources allouées lors de l’initialisation de la structure de contexte.

 

 



