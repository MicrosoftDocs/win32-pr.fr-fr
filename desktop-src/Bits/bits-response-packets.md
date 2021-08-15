---
title: Paquets de réponse BITS
description: Paquets de réponse BITS
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0a77cab49b990cc736b652382555861ecc569e030bb3ddd2bf255f717d455f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323559"
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



 

 

 




