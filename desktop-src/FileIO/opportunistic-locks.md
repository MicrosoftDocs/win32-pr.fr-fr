---
description: Un verrou opportuniste (également appelé oplock) est un verrou placé par un client sur un fichier résidant sur un serveur.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Verrous opportunistes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faec833caae05bff247a7a3655885b1a967f3435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752397"
---
# <a name="opportunistic-locks"></a>Verrous opportunistes

Un verrou opportuniste (également appelé oplock) est un verrou placé par un client sur un fichier résidant sur un serveur. Dans la plupart des cas, un client demande un verrou opportuniste pour pouvoir mettre en cache les données localement, ce qui réduit le trafic réseau et améliore le temps de réponse apparent. Les verrous opportunistes sont utilisés par les redirecteurs réseau sur les clients avec des serveurs distants, ainsi que par les applications clientes sur les serveurs locaux.

Les verrous opportunistes coordonnent la mise en cache et la cohérence des données entre les clients et les serveurs et entre plusieurs clients. Les données cohérentes sont des données qui sont identiques sur le réseau. En d’autres termes, si les données sont cohérentes, les données sur le serveur et tous les clients sont synchronisées.

Les verrous opportunistes ne sont pas des commandes du client sur le serveur. Il s’agit de requêtes du client vers le serveur. Du point de vue du client, ils sont opportunistes. En d’autres termes, le serveur accorde ces verrous chaque fois que d’autres facteurs rendent les verrous possibles.

Lorsqu’une application locale demande l’accès à un fichier distant, l’implémentation de verrous opportunistes est transparente pour l’application. Le redirecteur réseau et le serveur impliqués ouvrent et ferment automatiquement les verrous opportunistes. Toutefois, les verrous opportunistes peuvent également être utilisés lorsqu’une application locale demande l’accès à un fichier local, et l’accès par d’autres applications et processus doit être délégué pour empêcher l’altération du fichier. Dans ce cas, l’application locale demande directement un verrou opportuniste à partir du système de fichiers local et met en cache le fichier localement. Lorsqu’il est utilisé de cette manière, le verrou opportuniste est effectivement un sémaphore géré par le serveur local et est principalement utilisé dans le cadre de la cohérence des données dans la notification d’accès aux fichiers et aux fichiers.

Avant d’utiliser des verrous opportunistes dans votre application, vous devez être familiarisé avec les modes d’accès et de partage des fichiers décrits dans [création et ouverture de fichiers](creating-and-opening-files.md).

Le nombre maximal de verrous opportunistes simultanés que vous pouvez créer est limité uniquement par la quantité de mémoire disponible.

Les applications locales ne doivent pas tenter de demander des verrous opportunistes à partir de serveurs distants. Une erreur est renvoyée par [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) si une tentative est effectuée.

Les verrous opportunistes sont très peu utilisés pour les applications. La seule pratique consiste à tester un redirecteur réseau ou un gestionnaire de verrouillage opportuniste de serveur. En règle générale, les systèmes de fichiers implémentent la prise en charge des verrous opportunistes. Les applications laissent généralement la gestion des verrous opportunistes aux pilotes du système de fichiers. Toute personne qui implémente un système de fichiers doit utiliser le [Kit IFS (Installable File System)](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx). Toute personne développant un pilote de périphérique autre qu’un système de fichiers installable doit utiliser le [Kit WDK (Windows Driver Kit)](https://www.microsoft.com/?ref=go).

Les verrous opportunistes et les opérations associées sont un sur-ensemble de la portion de verrouillage opportuniste du protocole CIFS (Common Internet File System), un brouillon Internet. Le protocole CIFS est une version améliorée du protocole SMB (Server Message Block). Pour plus d’informations, consultez [vue d’ensemble du protocole SMB Microsoft et du protocole CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md). La version préliminaire d’Internet CIFS identifie explicitement qu’une implémentation CIFS peut implémenter des verrous opportunistes en refusant de les accorder.

Les rubriques suivantes identifient les verrous opportunistes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                               | Description                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mise en cache locale](local-caching.md)<br/>                                                                       | *La mise en cache locale* des données est une technique utilisée pour accélérer l’accès réseau aux fichiers de données. Cela implique la mise en cache des données sur les clients plutôt que sur des serveurs lorsque cela est possible.<br/>                                                                                                                           |
| [Cohérence des données](data-coherency.md)<br/>                                                                     | Si les données sont cohérentes, les données sur le serveur et tous les clients sont synchronisées. Un système logiciel qui assure la cohérence des données est un système de contrôle de révision (RCS).<br/>                                                                                                              |
| [Comment demander un verrou opportuniste](how-to-request-an-opportunistic-lock.md)<br/>                         | Les verrous opportunistes sont demandés en ouvrant un fichier avec les autorisations et les indicateurs appropriés à l’application ouvrant le fichier. Tous les fichiers pour lesquels des verrous opportunistes seront demandés doivent être ouverts pour une opération avec chevauchement (asynchrone).<br/>                                |
| [Réponse du serveur pour les demandes d’ouverture sur les fichiers verrouillés](server-response-to-open-requests-on-locked-files.md)<br/> | Vous pouvez réduire l’impact de votre application sur d’autres clients et l’impact qu’elle a sur votre application en accordant autant de partage que possible, en demandant le niveau d’accès minimal nécessaire et en utilisant le verrou opportuniste le moins intrusif adapté à votre application.<br/> |
| [Types de verrous opportunistes](types-of-opportunistic-locks.md)<br/>                                         | Décrit les verrous de niveau 1, de niveau 2, de traitement par lots et de filtrage opportuniste.<br/>                                                                                                                                                                                                                     |
| [Interruption des verrous opportunistes](breaking-opportunistic-locks.md)<br/>                                         | La rupture d’un verrou opportuniste est le processus qui consiste à dégrader le verrou d’un client sur un fichier de sorte qu’un autre client puisse ouvrir le fichier, avec ou sans verrou opportuniste.<br/>                                                                                                     |
| [Exemples de verrouillage opportuniste](opportunistic-lock-examples.md)<br/>                                           | Diagrammes de vues du trafic réseau pour un verrou opportuniste de niveau 1, un verrou par lot opportuniste et un verrou opportuniste de filtre.<br/>                                                                                                                                                       |
| [Opérations de verrouillage opportuniste](opportunistic-lock-operations.md)<br/>                                       | Si une application demande des verrous opportunistes, tous les fichiers pour lesquels elle demande des verrous doivent être ouverts pour les entrées et sorties avec chevauchement (asynchrone) à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) avec l’indicateur de **\_ \_ chevauchement** de l’indicateur de fichier.<br/>                                   |



 

Pour plus d’informations sur les verrous opportunistes, consultez le document préliminaire CIFS Internet. Toutes les incohérences entre cette rubrique et le brouillon Internet CIFS actuel doivent être résolues en faveur du projet Internet CIFS.

 

