---
description: Décrit les verrous de niveau 1, de niveau 2, de traitement par lots et de filtrage opportuniste.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Types de verrous opportunistes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dc450b038013454ea2d0ddd9c78a701dc8f977b4fa3b0aca7cdda076e8b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047849"
---
# <a name="types-of-opportunistic-locks"></a>Types de verrous opportunistes

Les opérations de verrouillage opportuniste fonctionnent avec quatre types de verrous opportunistes : niveau 1, niveau 2, lot et filtre. Les *verrous opportunistes exclusifs* sont les verrous de niveau 1, de lot et de filtre. Si un thread a un verrou exclusif sur un fichier, il ne peut pas également avoir un verrou de niveau 2 sur le même fichier.

## <a name="level-1-opportunistic-locks"></a>Verrous opportunistes de niveau 1

Un verrou opportuniste de niveau 1 sur un fichier permet à un client de lire à l’avance dans le fichier et de mettre en cache les données en lecture anticipée et d’écrire les données à partir du fichier localement. Tant que le client dispose d’un seul accès à un fichier, il n’y a aucun danger pour la cohérence des données dans la fourniture d’un verrou opportuniste de niveau 1.

Le client peut demander un verrou opportuniste de niveau 1 après l’ouverture d’un fichier. Si aucun autre client (ou aucun autre thread sur le même client) n’a ouvert le fichier, le serveur peut accorder le verrou opportuniste. Le client peut ensuite mettre en cache les données en lecture et en écriture à partir du fichier localement. Si un autre client a ouvert le fichier, le serveur refuse le verrou opportuniste et le client ne fait pas de mise en cache locale. (Le serveur peut refuser le verrouillage opportuniste pour d’autres raisons, par exemple pour ne pas prendre en charge les verrous opportunistes.)

Lorsque le serveur ouvre un fichier qui a déjà un verrou opportuniste de niveau 1, le serveur examine l’état de partage du fichier avant de rompre le verrou opportuniste de niveau 1. Si le serveur interrompt le verrou après cet examen, l’heure à laquelle le client avec le verrou précédent passe de vider son cache d’écriture est le temps que le client qui demande le fichier doit attendre. Cette dépense de temps signifie que les verrous opportunistes de niveau 1 doivent être évités sur les fichiers ouverts par de nombreux clients.

Toutefois, étant donné que le serveur vérifie l’état de partage avant de rompre le verrou, dans le cas où le serveur refuse une demande d’ouverture en raison d’un conflit de partage, le serveur n’interrompt pas le verrou. Par exemple, si vous avez ouvert un fichier, refusé le partage pour les opérations d’écriture et obtenu un verrou de niveau 1, le serveur refuse la demande d’ouverture du fichier par un autre client pour l’écriture avant même qu’il n’examine le verrou sur le fichier. Dans ce cas, le verrouillage opportuniste n’est pas interrompu.

Pour obtenir un exemple de fonctionnement d’un verrouillage opportuniste de niveau 1, consultez exemple de verrouillage opportuniste de niveau 1. Pour plus d’informations sur la rupture des verrous opportunistes, consultez [interruption des verrous opportunistes](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Verrous opportunistes de niveau 2

Un verrou opportuniste de niveau 2 informe un client qu’il existe plusieurs clients simultanés d’un fichier et qu’aucun ne l’a encore modifié. Ce verrou permet au client d’effectuer des opérations de lecture et d’obtenir des attributs de fichier à l’aide d’informations locales mises en cache ou en lecture anticipée, mais le client doit envoyer toutes les autres requêtes (telles que les opérations d’écriture) au serveur. Votre application doit utiliser le verrou opportuniste de niveau 2 lorsque vous vous attendez à ce que d’autres applications écrivent dans le fichier au hasard ou lisent le fichier de façon aléatoire ou séquentielle.

Un verrou opportuniste de niveau 2 est très similaire à un verrou opportuniste de filtre. Dans la plupart des cas, votre application doit utiliser le verrou opportuniste de niveau 2. Utilisez le verrou de filtre uniquement si vous ne souhaitez pas que les opérations d’ouverture pour la lecture entraînent des violations du mode de partage dans l’intervalle de temps entre l’ouverture du fichier par votre application et la réception du verrou. Pour plus d’informations, consultez filtrer les verrous opportunistes et [réponse du serveur pour ouvrir des demandes sur des fichiers verrouillés](server-response-to-open-requests-on-locked-files.md).

Pour plus d’informations sur la rupture des verrous opportunistes, consultez [interruption des verrous opportunistes](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Verrouillages opportunistes par lots

Un verrou opportuniste de traitement par lots manipule les ouvertures et les fermetures de fichiers. Par exemple, dans l’exécution d’un fichier de commandes, le fichier de commandes peut être ouvert et fermé une fois pour chaque ligne du fichier. Un verrou par lot opportuniste ouvre le fichier de commandes sur le serveur et le maintient ouvert. À mesure que le processeur de commandes « s’ouvre » et « ferme » le fichier de commandes, le redirecteur réseau intercepte les commandes d’ouverture et de fermeture. Tout le serveur reçoit les commandes Seek et Read. Si le client est également en lecture anticipée, le serveur reçoit une demande de lecture particulière au plus une fois.

Lors de l’ouverture d’un fichier qui a déjà un verrou opportuniste par lot, le serveur vérifie l’état de partage du fichier après avoir endommagé le verrou. Cette vérification donne au détenteur du verrou la possibilité de terminer le vidage de son cache et de fermer le descripteur de fichier. Une opération d’ouverture tentée pendant la vérification du partage n’entraîne pas l’échec de la vérification du partage si le détenteur du verrou libère le verrou.

Pour obtenir un exemple illustrant le fonctionnement d’un verrouillage opportuniste par lot, consultez exemple de verrouillage opportuniste par lots. Pour plus d’informations sur la rupture des verrous opportunistes, consultez [interruption des verrous opportunistes](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtrer les verrous opportunistes

Un verrou opportuniste de filtre verrouille un fichier afin qu’il ne puisse pas être ouvert pour l’accès en écriture ou en suppression. Tous les clients doivent être en mesure de partager le fichier. Les verrous de filtre permettent aux applications d’effectuer des opérations de filtrage non intrusives sur des données de fichier (par exemple, un compilateur ouvrant du code source ou un programme de catalogage).

Un verrou opportuniste de filtre diffère d’un verrou opportuniste de niveau 2 dans la mesure où il permet aux opérations d’ouverture de lecture de se produire sans violations du mode de partage dans l’intervalle de temps entre l’ouverture du fichier par votre application et la réception du verrou. Le verrou opportuniste de filtre est le meilleur verrou à utiliser lorsqu’il est important d’autoriser d’autres clients à lire l’accès. Dans d’autres cas, votre application doit utiliser un verrou opportuniste de niveau 2. Un verrou opportuniste de filtre diffère d’un verrou par lot opportuniste dans le sens où il ne permet pas à plusieurs ouvertures et fermetures d’être gérées par le redirecteur réseau à l’aide d’un verrou par lot opportuniste.

Votre application doit demander un verrou opportuniste de filtre sur un fichier en trois étapes :

1.  Utilisez la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir un handle vers le fichier avec le paramètre *desiredAccess* défini sur zéro, indiquant qu’il n’y a pas d’accès, et le paramètre *dwShareMode* défini sur l’indicateur de **\_ \_ lecture de partage de fichiers** pour autoriser le partage pour la lecture. Le descripteur obtenu à ce stade est appelé handle de verrouillage.
2.  Demandez un verrou sur ce descripteur à l’aide du code de contrôle [**\_ OPLOCK de \_ filtre \_ de requête FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock) .
3.  Lorsque le verrou est accordé, utilisez [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir à nouveau le fichier avec *desiredAccess* défini sur l’indicateur de **\_ lecture générique** . Définissez *dwShareMode* sur l’indicateur de **\_ \_ lecture de partage de fichiers** pour permettre à d’autres utilisateurs de lire le fichier quand vous l’avez ouvert, l’indicateur de **\_ \_ Suppression de partage de fichiers** pour permettre à d’autres utilisateurs de marquer le fichier pour qu’il soit supprimé, ou les deux. Le descripteur obtenu à ce stade est appelé handle de lecture.

Utilisez le handle de lecture pour lire ou écrire dans le contenu du fichier.

Lors de l’ouverture d’un fichier qui a déjà un verrou opportuniste de filtre, le serveur interrompt le verrou, puis vérifie l’état de partage du fichier. Cette vérification donne au client qui détenait l’ancien verrou opportuniste la possibilité d’abandonner toutes les données mises en cache et d’accuser réception de l’arrêt. Une opération d’ouverture tentée pendant cette vérification du partage n’entraîne pas l’échec de la vérification du partage si le détenteur du verrouillage précédent libère le verrou. Le système de fichiers contient dans abeyance l’opération d’ouverture jusqu’à ce que le propriétaire du verrou ferme à la fois le handle de lecture et le handle de verrouillage. Une fois cette opération terminée, la demande d’ouverture de l’autre client peut se poursuivre.

Pour plus d’informations sur la rupture des verrous opportunistes, consultez [interruption des verrous opportunistes](breaking-opportunistic-locks.md).

 

 
