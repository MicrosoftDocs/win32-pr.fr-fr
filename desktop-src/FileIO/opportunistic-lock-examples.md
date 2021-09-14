---
description: Diagrammes de vues du trafic réseau pour un verrou opportuniste de niveau 1, un verrou par lot opportuniste et un verrou opportuniste de filtre.
ms.assetid: 78830113-b18e-40c7-8ec4-8896dbc58030
title: Exemples de verrouillage opportuniste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8b8a0c5b04897ddc2fc8f2e3bdec20f2fdb02d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009880"
---
# <a name="opportunistic-lock-examples"></a>Exemples de verrouillage opportuniste

Les exemples suivants montrent des données et des mouvements de messages SMB en cas de verrouillage opportuniste. Notez que les clients peuvent mettre en cache les données d’attribut de fichier ainsi que les données de fichier.

Notez également que ces exemples sont basés sur des situations où les applications clientes demandent des verrous opportunistes à partir de serveurs distants. Ces processus sont initiés automatiquement par le redirecteur réseau et le serveur distant ; il n’y a aucune implication directe de la part de l’application cliente ou des applications. Les processus décrits dans ces exemples peuvent être généralisés dans des situations où les applications clientes locales demandent directement des verrous opportunistes à partir du système de fichiers local, à l’exception du fait qu’aucun échange de données sur le réseau n’est impliqué.

## <a name="level-1-opportunistic-lock"></a>Verrou opportuniste de niveau 1

Le diagramme suivant montre une vue du trafic réseau d’un verrou opportuniste de niveau 1 sur un fichier. Les flèches indiquent le sens du déplacement des données, le cas échéant.



| Événement | Client X                                          | Serveur                                   | Client Y                                          |
|-------|---------------------------------------------------|------------------------------------------|---------------------------------------------------|
| 1     | Ouvre le fichier, demande le niveau 1 Lock = =>          |                                          |                                                   |
| 2     |                                                   | <= = octroie le niveau 1 de verrouillage opportuniste |                                                   |
| 3     | Effectue les opérations de lecture, d’écriture et d’autres opérations = => |                                          |                                                   |
| 4     |                                                   |                                          | <= = demandes d’ouverture de fichier                      |
| 5     |                                                   | <= = interrompt le verrouillage opportuniste         |                                                   |
| 6     | Ignore les données en lecture anticipée                          |                                          |                                                   |
| 7     | Écrit les données = =>                                |                                          |                                                   |
| 8     | Envoie le message « Close » ou « Done » = =>            |                                          |                                                   |
| 9     |                                                   | Opération d’ouverture OK = =>              |                                                   |
| 10    | Effectue les opérations de lecture, d’écriture et d’autres opérations = => |                                          | <= = effectue des opérations de lecture, d’écriture et d’autres opérations |



 

Dans l’épreuve 1, le client X ouvre un fichier et, dans le cadre de l’opération d’ouverture, demande un verrou opportuniste de niveau 1 sur le fichier. Dans l’événement 2, le serveur accorde le verrou de niveau 1, car aucun autre client n’a ouvert le fichier. Le client continue d’accéder au fichier de la manière habituelle dans l’événement 3.

Dans l’épreuve 4, le client Y tente d’ouvrir le fichier et demande un verrou opportuniste. Le serveur constate que le fichier X est ouvert. Le serveur ignore la demande de Y pendant que le client X vide toutes les données d’écriture et abandonne son cache de lecture pour le fichier.

Le serveur Force X à nettoyer en envoyant à X un message SMB qui rompt le verrou opportuniste, événement 5. Le client X « en mode silencieux » ignore les données en lecture anticipée ; en d’autres termes, ce processus ne génère aucun trafic réseau. Dans l’épreuve 7, le client X écrit toutes les données d’écriture mises en cache sur le serveur. Lorsque le client X écrit des données mises en cache sur le serveur, le client X envoie un message « fermer » ou « terminé » au serveur, événement 8.

Une fois que le serveur a été averti que le client X a terminé le vidage du cache d’écriture sur le serveur ou a fermé le fichier, le serveur peut ouvrir le fichier pour le client Y, dans l’événement 9. Étant donné que le serveur a maintenant deux clients avec le même fichier ouvert, il n’accorde un verrou opportuniste à aucun d’entre eux. Les deux clients poursuivent la lecture à partir du fichier et l’un ou l’autre n’écrit pas dans le fichier.

## <a name="batch-opportunistic-lock"></a>Verrouillage opportuniste par lot

Le diagramme suivant montre une vue du trafic réseau d’un verrou par lot opportuniste. Les flèches indiquent le sens du déplacement des données, le cas échéant.



| Événement | Client X                               | Serveur                                 | Client Y                                          |
|-------|----------------------------------------|----------------------------------------|---------------------------------------------------|
| 1     | Ouvre le fichier, demande un verrou de lot = => |                                        |                                                   |
| 2     |                                        | <= = octroie un verrou opportuniste par lot |                                                   |
| 3     | Lit le fichier = =>                      |                                        |                                                   |
| 4     |                                        | <= = envoie des données                      |                                                   |
| 5     | Ferme le fichier                            |                                        |                                                   |
| 6     | Ouvre le fichier                             |                                        |                                                   |
| 7     | Recherche des données                      |                                        |                                                   |
| 8     | Lit les données = =>                      |                                        |                                                   |
| 9     |                                        | <= = envoie des données                      |                                                   |
| 10    | Ferme le fichier                            |                                        |                                                   |
| 11    |                                        |                                        | <= = ouvre le fichier                                 |
| 12    |                                        | <= = interrompt le verrouillage opportuniste       |                                                   |
| 13    | Ferme le fichier = =>                     |                                        |                                                   |
| 14    |                                        | Opération d’ouverture OK = =>            |                                                   |
| 15    |                                        |                                        | <= = effectue des opérations de lecture, d’écriture et d’autres opérations |



 

Dans le verrouillage opportuniste du lot, le client X ouvre un fichier, événement 1, et le serveur accorde au client X un verrou par lot dans l’événement 2. Le client X tente de lire les données, événement 3, auxquelles le serveur répond avec les données, événement 4.

L’événement 5 illustre le verrouillage opportuniste du lot au travail. L’application sur le client X ferme le fichier. Toutefois, le redirecteur réseau filtre l’opération de fermeture et ne transmet pas de message de fermeture, ce qui effectue une fermeture « silencieuse ». Le redirecteur réseau peut effectuer cette opération, car le client X a la propriété exclusive du fichier. Plus tard, dans l’épreuve 6, l’application ouvre de nouveau le fichier. Là encore, aucun flux de données n’est transmis sur le réseau. En ce qui concerne le serveur, ce client a ouvert le fichier depuis l’événement 2.

Les événements 7, 8 et 9 illustrent le déroulement habituel du trafic réseau. Dans l’événement 10, une autre fermeture silencieuse se produit.

Dans l’événement 11, le client Y tente d’ouvrir le fichier. La vue du fichier du serveur est celle où le client X s’ouvre, même si l’application sur le client X l’a fermée. Par conséquent, le serveur envoie un message de rupture du verrouillage opportuniste au client X. client X envoie maintenant le message de fermeture sur le réseau, l’événement 13. L’événement 14 suit quand le serveur ouvre le fichier pour le client Y. L’application sur le client X a fermé le fichier, de sorte qu’il n’y a plus de transferts vers ou à partir du serveur pour ce fichier. Le client Y commence les transferts de données comme d’habitude dans l’événement 15.

Entre le moment où le client X reçoit le verrou sur le fichier dans l’événement 2 et la dernière clôture à l’événement 13, toutes les données de fichier mises en cache par le client sont valides, en dépit des opérations d’ouverture et de fermeture de l’application intermédiaire. Toutefois, une fois que le verrouillage opportuniste est interrompu, les données mises en cache ne peuvent pas être considérées comme valides.

## <a name="filter-opportunistic-lock"></a>Filtrer le verrou opportuniste

Le diagramme suivant montre une vue du trafic réseau d’un verrou de filtre opportuniste. Les flèches indiquent le sens du déplacement des données, le cas échéant.



| Événement | Client X                                | Serveur                   | Client Y                    |
|-------|-----------------------------------------|--------------------------|-----------------------------|
| 1     | Ouvre le fichier sans droits d’accès = => |                          |                             |
| 2     |                                         | <= = ouvre le fichier    |                             |
| 3     | Filtre des demandes Lock = =>              |                          |                             |
| 4     |                                         | <= = octroie un verrou       |                             |
| 5     | Ouvre le fichier pour lecture = =>           |                          |                             |
| 6     |                                         | <= = ouvre de nouveau le fichier  |                             |
| 7     | Lit les données à l’aide du handle de lecture = => |                          |                             |
| 8     |                                         | <= = envoie des données        |                             |
| 9     |                                         | <= = envoie des données        |                             |
| 10    |                                         | <= = envoie des données        |                             |
| 11    |                                         |                          | <= = ouvre le fichier       |
| 12    |                                         | Ouvre le fichier = =>    |                             |
| 13    |                                         |                          | <= = verrou du filtre des demandes |
| 14    |                                         | Refuse le verrou de filtre = => |                             |
| 15    |                                         |                          | <= = lit les données           |
| 16    |                                         | Envoie les données = =>        |                             |
| 17    | Lit les données (mises en cache)                     |                          |                             |
| 18    | Ferme le fichier = =>                      |                          |                             |
| 19    |                                         |                          | <= = ferme le fichier          |



 

Dans le verrou opportuniste du filtre, le client X ouvre un fichier, événement 1, et le serveur répond dans l’événement 2. Le client demande ensuite un verrou opportuniste de filtre dans l’événement 3, suivi du serveur accordant le verrou opportuniste dans l’événement 4. Le client X ouvre ensuite le fichier à nouveau pour lire l’événement 5, vers lequel le serveur répond dans l’événement 6. Le client essaie ensuite de lire les données auxquelles le serveur répond avec les données, événement 8.

L’événement 9 montre le verrou opportuniste de filtre au travail. Le serveur lit à l’avance le client et envoie les données sur le réseau, même si le client ne l’a pas demandé. Le client met en cache les données. Dans l’épreuve 10, le serveur anticipe également une demande de données ultérieures et envoie une autre partie du fichier à mettre en cache par le client.

Dans les événements 11 et 12, un autre client, Y, ouvre le fichier. Le client Y demande également un verrou opportuniste de filtre. Dans l’événement 14, le serveur le refuse. Dans l’événement 15, le client Y demande des données que le serveur envoie dans l’événement 16. Aucune de ces conséquences n’affecte le client X. À tout moment, un autre client peut ouvrir ce fichier pour l’accès en lecture. Aucun autre client n’affecte le verrou de filtre du client X.

L’événement 17 montre les données de lecture du client X. Toutefois, étant donné que le serveur a déjà envoyé les données et que le client les a mises en cache, aucun trafic ne traverse le réseau.

Dans cet exemple, le client X ne tente jamais de lire toutes les données du fichier. la lecture anticipée indiquée par les événements 9 et 10 est donc « gaspillée ». autrement dit, les données ne sont jamais réellement utilisées. Il s’agit d’une perte acceptable, car la lecture anticipée a accéléré l’application.

Dans l’événement 18, le client X ferme le fichier. Le redirecteur réseau du client abandonne les données mises en cache. Le serveur ferme le fichier.

 

 



