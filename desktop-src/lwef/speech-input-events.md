---
title: Événements d’entrée vocale
description: Événements d’entrée vocale
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0dc75bb010286b7645c206d192913017472829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029880"
---
# <a name="speech-input-events"></a>Événements d’entrée vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

En outre, pour la notification d’événement de [**commande**](command-event.md) , l’agent notifie également le client d’entrée-actif lorsque le serveur Active ou désactive le mode d’écoute, à l’aide des événements [**ListenStart**](listenstart-event.md) et [**ListenComplete**](listencomplete-event.md) ([**IAgentNotifySinkEx :: ListeningState**](iagentnotifysinkex--listeningstate.md)). Toutefois, si l’utilisateur appuie sur la touche mode d’écoute et qu’aucun moteur de reconnaissance vocale correspondant n’est disponible pour le premier caractère du client d’entrée-actif, le serveur démarre le délai d’attente du mode de raccourci d’écoute, mais ne génère pas d’événement **ListenStart** pour le client actif du caractère. Si, avant la fin du délai d’attente, l’utilisateur active un autre caractère avec la prise en charge du moteur de reconnaissance vocale, le serveur tente d’activer l’entrée vocale et génère l’événement **ListenStart** .

De même, si un client tente d’activer le mode d’écoute à l’aide de la méthode [**Listen**](listen-method.md) et qu’aucun moteur de reconnaissance vocale correspondant n’est disponible, l’appel échoue et le serveur ne génère pas d’événement [**ListenStart**](listenstart-event.md). Dans le contrôle Microsoft Agent, la méthode **Listen** retourne la **valeur false**, mais l’appel ne génère pas d’erreur.

Lorsque le mode de la clé d’écoute est activé et que l’utilisateur bascule vers un caractère qui utilise un autre moteur de reconnaissance vocale, le serveur bascule vers et active ce moteur, puis déclenche un [**ListenComplete**](listencomplete-event.md) et un événement [**ListenStart**](listenstart-event.md) . Si le caractère activé ne dispose pas d’un moteur de reconnaissance vocale (parce qu’aucun n’est installé ou qu’il ne correspond pas au paramètre ID de langue du caractère activé), le serveur déclenche l’événement **ListenComplete** pour le caractère précédemment activé et transmet une valeur dans le paramètre **cause** . Toutefois, le serveur ne génère pas d’événements **ListenStart** ou **ListenComplete** pour les clients qui n’ont pas de prise en charge de la reconnaissance vocale.

Si un client appelle correctement la méthode [**Listen**](listen-method.md) et qu’un caractère sans prise en charge du moteur de reconnaissance vocale devient inactif avant la fin du délai d’attente du mode d’écoute, puis l’utilisateur revient au caractère du client d’origine, le serveur génère un événement [**ListenStart**](listenstart-event.md) pour ce client.

Si le client d’entrée/de sortie active bascule les moteurs de reconnaissance vocale en modifiant [**SRModeID**](srmodeid-property.md) en mode d’écoute, le serveur bascule vers et active ce moteur sans redéclencher l’événement [**ListenStart**](listenstart-event.md) . Toutefois, si le moteur spécifié n’est pas disponible, l’appel échoue (génère une erreur dans le contrôle) et le serveur appelle également l’événement [**ListenComplete**](listencomplete-event.md) .

 

 




