---
description: Windows Sockets 2 étend les fonctionnalités de Windows Sockets 1,1 dans un certain nombre de domaines. Le tableau suivant résume quelques-unes des principales modifications apportées aux fonctionnalités.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Considérations sur la programmation Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaee2cd04f03afe050ca539190b51e66c0abff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114286"
---
# <a name="winsock-programming-considerations"></a>Considérations sur la programmation Winsock

Windows Sockets 2 étend les fonctionnalités de Windows Sockets 1,1 dans un certain nombre de domaines. Le tableau suivant résume quelques-unes des principales modifications apportées aux fonctionnalités.



| Fonctionnalités                                                                                                           | Description                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Architecture Windows Sockets 2](windows-sockets-2-architecture-2.md)                                             | Description de l’architecture Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Handles de socket](socket-handles-2.md)                                                                             | Un handle de socket peut éventuellement être un descripteur de fichier dans Windows Sockets 2. Il est possible d’utiliser des descripteurs de socket avec les fonctions d’e/s de fichier Windows standard.                                                                                                                                           |
| [Accès simultané à plusieurs protocoles de transport](simultaneous-access-to-multiple-transport-protocols-2.md)   | Permet à une application d’utiliser l’interface de socket familière pour obtenir un accès simultané à plusieurs protocoles de transport installés.                                                                                                                                                        |
| [Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)                                 | Comprend un ensemble standardisé de fonctions qui permettent d’interroger et d’utiliser les domaines de la résolution de noms Myriad qui existent aujourd’hui (par exemple DNS, SAP et X. 500).                                                                                                                                  |
| [Multidiffusion et multipoint indépendantes des protocoles](protocol-independent-multicast-and-multipoint-2.md)               | Les applications découvrent le type de fonctionnalités multipoint ou de multidiffusion qu’un transport fournit et utilisent ces fonctionnalités de façon générique.                                                                                                                                                     |
| [E/s avec chevauchement](overlapped-i-o-and-event-objects-2.md)                                                           | Intègre le paradigme Overlapped pour les e/s de socket à la suite du modèle établi dans les environnements Windows.                                                                                                                                                                                   |
| [E/s de ventilation/regroupement](scatter-gather-i-o-2.md)                                                                     | Intègre des fonctionnalités de ventilation/regroupement avec le paradigme avec chevauchement pour les e/s de socket, suivant le modèle établi dans les environnements Windows.                                                                                                                                                 |
| [Qualité de service](flow-specification-quality-of-service-2.md) (QoS)                                            | Établit les conventions utilisées par les applications pour négocier des niveaux de service requis pour des paramètres tels que la bande passante et la latence. D’autres améliorations liées à la QoS incluent des mécanismes pour la qualité des extensions de service spécifiques au réseau.                                                         |
| [Mécanisme d’extension spécifique au fournisseur](provider-specific-extension-mechanism-2.md)                               | La fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permet aux fournisseurs de services d’offrir des extensions de fonctionnalités spécifiques au fournisseur.                                                                                                                                                                           |
| [Sockets partagés](shared-sockets-2.md)                                                                             | La fonction [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) est introduite pour permettre le partage de socket entre les processus.                                                                                                                                                                       |
| [Configuration et destruction de la connexion](connection-setup-and-teardown-2.md)                                               | Une application peut obtenir des informations sur l’appelant, telles que l’identificateur de l’appelant et la qualité de service, avant de décider d’accepter ou non une demande de connexion entrante. Il est également possible (pour les protocoles qui le prennent en charge) d’échanger des données utilisateur entre les points de terminaison au moment de la destruction de la connexion. |
| [Arrêt approprié, options de maintien et fermeture de socket](graceful-shutdown-linger-options-and-socket-closure-2.md) | Une application dispose de plusieurs options pour arrêter une connexion de socket (séquence d’arrêt).                                                                                                                                                                                                  |
| [Données hors bande indépendantes des protocoles](protocol-independent-out-of-band-data-2.md)                               | L’abstraction de socket de flux comprend la notion de données hors bande (OOB).                                                                                                                                                                                                                   |
| [Fonctionnalités de débogage et de suivi](debug-and-trace-facilities-2.md)                                                     | Windows Sockets 2 prend en charge une version spéciale du32.dll Ws2 \_ et une dll de débogage/suivi distincte.                                                                                                                                                                                      |
| [Problèmes de compatibilité de Windows Sockets](windows-sockets-compatibility-issues-2.md)                                 | Windows Sockets 2 continue à prendre en charge l’ensemble de la sémantique et des appels de fonction Windows Sockets 1,1, à l’exception de ceux qui traitent d’un Pseudo-blocage.                                                                                                                                              |
| [Gestion des erreurs Winsock](handling-winsock-errors.md)                                                             | Comment les erreurs Winsock peuvent être récupérées et gérées par une application.                                                                                                                                                                                                                             |



 

 

 



