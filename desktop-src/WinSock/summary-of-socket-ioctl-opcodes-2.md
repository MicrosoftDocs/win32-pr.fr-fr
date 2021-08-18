---
description: certains opcodes IOCTL de socket pour Windows sockets 2 sont résumés dans le tableau suivant.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Résumé des OpCodes IOCTL de socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f0d6163e4ef36598dad56dd4d81201bdda3c2a3b1bb0473a0ef9ffb4675b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559659"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Résumé des OpCodes IOCTL de socket

certains opcodes IOCTL de socket pour Windows sockets 2 sont résumés dans le tableau suivant. Des informations plus détaillées se trouvent dans les informations de référence sur Winsock sur [**Winsock IOCTL**](winsock-ioctls.md) et la fonction [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) . Il existe d’autres nouveaux OpCodes IOCTL spécifiques au protocole qui se trouvent dans l’annexe spécifique au protocole.

Une liste complète des [**IOCTL Winsock**](winsock-ioctls.md) est disponible dans les informations de référence sur Winsock.



| Opcode                                                      | Type d’entrée                               | Type de sortie                                 | Signification                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Long non signé                            | <Not used>                            | Active ou désactive le mode non bloquant sur le Socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Long non signé                               | Détermine la quantité de données qui peuvent être lues de manière atomique à partir du Socket.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Détermine si toutes les données OOB ont été lues.                                                                                                                                                              |
| \_descripteur Associate SIO \_                                      | Fonction de l’API associée                  | <Not used>                            | Associe le socket au handle spécifié d’une interface auxiliaire.                                                                                                                                          |
| SIO \_ activer \_ la \_ file d’attente circulaire                             | <Not used>                         | <Not used>                            | Active la mise en file d’attente circulaire.                                                                                                                                                                                          |
| SIO \_ Rechercher l' \_ itinéraire                                            | [**sockaddr**](sockaddr-2.md) , structure | <Not used>                            | Demande l’itinéraire vers l’adresse spécifiée à découvrir.                                                                                                                                                      |
| \_vidage SIO                                                  | <Not used>                         | <Not used>                            | Ignore le contenu actuel de la file d’attente d’envoi.                                                                                                                                                                    |
| SIO \_ Obtient \_ l' \_ adresse de diffusion                                | <Not used>                         | [**sockaddr**](sockaddr-2.md) , structure    | Récupère l’adresse de diffusion spécifique au protocole à utiliser dans [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)).                                                                                                                  |
| SIO \_ Obtient \_ QoS                                               | <Not used>                         | [**Quality**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Récupère les spécifications de workflow actuelles pour le Socket.                                                                                                                                                              |
| SIO \_ récupérer le \_ groupe \_ QoS                                        | <Not used>                         | [**Quality**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Réservé.                                                                                                                                                                                                          |
| \_bouclage multipoint \_ SIO                                   | BOOL                                     | <Not used>                            | Contrôle si les données envoyées dans une session multipoint seront également reçues par le même socket sur l’hôte local.                                                                                                     |
| \_étendue de multidiffusion SIO \_                                       | int                                      | <Not used>                            | Spécifie la portée sur laquelle les transmissions par multidiffusion auront lieu.                                                                                                                                                 |
| SIO \_ définir la qualité de service \_                                               | [**Quality**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Établit de nouvelles spécifications de Flow pour le Socket.                                                                                                                                                                |
| SIO définir la qualité de service du \_ \_ groupe \_                                        | [**Quality**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Réservé.                                                                                                                                                                                                          |
| \_handle SIO translate \_                                      | int                                      | Fonction associée-API                     | Obtient un handle correspondant pour *le socket qui* est valide dans le contexte d’une interface auxiliaire.                                                                                                               |
| requête de l' \_ interface de routage SIO \_ \_                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Obtient l’adresse de l’interface locale qui doit être utilisée pour envoyer à l’adresse spécifiée.                                                                                                                   |
| modification de l' \_ interface de routage SIO \_ \_                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Demande la notification des modifications apportées aux informations signalées par \_ \_ le biais \_ de la requête de l’interface de routage SIO pour l’adresse spécifiée.                                                                                         |
| [**\_requête de \_ liste d’adresses SIO \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**adresse du SOCKET \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Obtient la liste des adresses de transport locales de la famille de protocoles du socket à laquelle l’application peut se lier. La liste des adresses varie en fonction de la famille d’adresses et certaines adresses sont exclues de la liste. |
| modification de la \_ liste d’adresses SIO \_ \_                                  | <Not used>                         | <Not used>                            | Demande la notification des modifications apportées aux informations transmises via la requête de liste d' \_ adresses SIO \_ \_                                                                                                                         |
| \_handle de \_ \_ cible PNP de requête \_ SIO                             | <Not used>                         | SOCLE                                      | Obtient le descripteur de socket du fournisseur suivant dans la chaîne dont dépend le socket actuel en ce qui concerne PnP.                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IOCTL Winsock**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
