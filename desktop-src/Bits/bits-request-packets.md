---
title: Paquets de demande BITS
description: Paquets de demande BITS
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939713"
---
# <a name="bits-request-packets"></a>Paquets de demande BITS

Les paquets de demande décrivent les demandes des clients. Il ne peut y avoir qu’une seule demande en suspens à un moment donné. vous devez recevoir un [accusé](bits-response-packets.md) de réception pour la demande en cours à partir du serveur avant d’envoyer une autre demande.

Le tableau suivant répertorie les paquets de demande envoyés au serveur BITS pour les travaux de chargement et de chargement-réponse. Le tableau répertorie les paquets dans la séquence type qu’ils envoient au serveur.



| Paquet de demande                       | Objectif                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ping](ping.md)                     | Établit une connexion et négocie la sécurité avec le serveur.                                                                                              |
| [Créer une session](create-session.md) | Demande une session de chargement avec le serveur BITS.                                                                                                               |
| [Fragment](fragment.md)             | Envoie un fragment du fichier au serveur BITS. Le nombre de requêtes de fragment envoyées dépend de la taille de fragment que vous choisissez et de la taille du fichier de téléchargement. |
| [Fermer-session](close-session.md)   | Met fin à la session de chargement de fichier avec le serveur BITS.                                                                                                             |
| [Annuler-session](cancel-session.md) | Met fin à la session de chargement de fichier avec le serveur BITS. En règle générale, vous envoyez le paquet Cancel-Session si l’utilisateur a annulé le travail.                                 |



 

Le paquet ping est facultatif. Au lieu d’envoyer un paquet ping, vous pouvez utiliser le paquet Create-Session pour établir une connexion et négocier la sécurité. Toutefois, il est plus efficace d’utiliser le paquet ping à cet effet.

 

 




