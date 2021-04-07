---
title: Protocole de téléchargement BITS
description: Cette section décrit le protocole réseau pour les types de tâches chargement BITS et chargement-réponse.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671629"
---
# <a name="bits-upload-protocol"></a>Protocole de téléchargement BITS

Cette section décrit le protocole réseau pour les types de tâches chargement BITS et chargement-réponse. Le protocole de téléchargement BITS est superposé sur HTTP 1,1 et utilise un grand nombre d’en-têtes HTTP existants et définit de nouveaux en-têtes. Le protocole de téléchargement BITS prend en charge un seul fichier de téléchargement par session.

BITS utilise des paquets pour décrire les demandes du client et les réponses du serveur. L’en-tête BITS-Packet-type spécifie le type de paquet envoyé. Chaque paquet contient des en-têtes spécifiques. BITS utilise le \_ verbe de publication bits pour identifier les paquets de chargement bits. Les paquets de réponse utilisent toujours le type de paquet ACK qui correspond à la reconnaissance. Le paquet ACK est envoyé dans le contexte de la demande précédente ; il ne peut y avoir qu’une seule demande en suspens à la fois.

Pour les travaux de chargement-réponse, BITS utilise ce protocole pour télécharger le fichier, mais n’utilise pas ce protocole pour envoyer la réponse au client. Au lieu de cela, le serveur BITS envoie l’emplacement du fichier de réponse au client et le client crée un travail de téléchargement BITS pour télécharger le fichier de réponse.

Utilisez le protocole de téléchargement pour remplacer le logiciel client ou serveur BITS par votre propre implémentation. Pour obtenir la liste des paquets de demande envoyés par le client BITS, consultez [paquets de demande bits](bits-request-packets.md). Pour obtenir la liste des paquets de réponse envoyés par le serveur BITS, consultez [paquets de réponse bits](bits-response-packets.md).

Le client détermine comment il répond aux erreurs ou aux paquets inattendus du serveur BITS. Si le serveur reçoit un paquet qui ne s’attend pas, le serveur doit envoyer un paquet ACK avec un code de retour 400 (demande incorrecte).

 

 




