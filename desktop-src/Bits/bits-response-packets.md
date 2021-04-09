---
title: Paquets de réponse BITS
description: Paquets de réponse BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839369"
---
# <a name="bits-response-packets"></a>Paquets de réponse BITS

Le tableau suivant répertorie les paquets de réponse envoyés au client BITS pour les travaux de chargement et de chargement-réponse. Le tableau répertorie les paquets dans la séquence type qu’ils envoient au client.



| Paquet de réponse                                      | Objectif                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ACK pour ping](ack-for-ping.md)                     | Accuse réception de la demande [ping](ping.md) .                                                                                                                                                  |
| [ACK pour Create-session](ack-for-create-session.md) | Accuse réception de la demande de [création de session](create-session.md) et retourne un identificateur de session que le client bits utilise sur toutes les demandes suivantes pour identifier cette session de transfert de fichiers. |
| [ACK pour fragment](ack-for-fragment.md)             | Accuse réception de la demande de [fragment](fragment.md) et écrit le fragment dans le fichier de téléchargement sur le serveur.                                                                                 |
| [ACK pour Close-session](ack-for-close-session.md)   | Accuse réception de la demande de [fermeture de session](close-session.md) et libère toutes les ressources associées à la session.                                                                         |
| [ACK pour Cancel-session](ack-for-cancel-session.md) | Accuse réception de la demande d' [annulation de session](cancel-session.md) et libère toutes les ressources associées à la session.                                                                       |



 

 

 




