---
title: Instructions pour plusieurs utilisateurs
description: Instructions pour le développement d’applications pour plusieurs utilisateurs dans un environnement de Services Bureau à distance.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106544145"
---
# <a name="multiple-user-guidelines"></a>Instructions pour plusieurs utilisateurs

Les sections suivantes fournissent des instructions pour le développement d’applications pour plusieurs utilisateurs dans un environnement de Services Bureau à distance.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Configuration des applications](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

L’installation d’une application pour un seul utilisateur peut créer des problèmes dans un environnement multi-utilisateur Services Bureau à distance.

</dd> <dt>

[Stockage des informations spécifiques à l’utilisateur](storing-user-specific-information.md)
</dt> <dd>

Les applications doivent stocker les informations spécifiques à l’utilisateur dans des emplacements spécifiques à l’utilisateur, séparément des informations globales qui s’appliquent à tous les utilisateurs.

</dd> <dt>

[Espaces de noms d’objets de noyau](kernel-object-namespaces.md)
</dt> <dd>

Services Bureau à distance utilise plusieurs espaces de noms pour les objets de noyau ; un espace de noms global est principalement utilisé par les services dans les applications client/serveur.

</dd> <dt>

[Adresses IP et noms d’ordinateurs](ip-addresses-and-computer-names.md)
</dt> <dd>

Il est déconseillé de supposer que le nom d’ordinateur ou l’ adresse IP affectée à l’ordinateur sont associés à un seul utilisateur, étant donné que plusieurs utilisateurs peuvent être connectés simultanément à un serveur hôte de Session Bureau à distance.

</dd> </dl>

Comme toujours, verrouillez les fichiers et les bases de données tout en apportant des modifications pour empêcher toute perte accidentelle de données.

Votre application ne doit pas verrouiller les fichiers d’application d’exécution qui ne sont pas des fichiers par utilisateur. Les fichiers d’exécution verrouillés peuvent empêcher l’exécution de plusieurs instances de l’application, ou des processus sous l’application, tels que les assistants. Un bon moyen de tester les fichiers qui sont des fichiers d’application au moment de l’exécution consiste à effectuer le suivi des fichiers qui sont installés par le programme d’installation de l’application. Les fichiers par utilisateur sont rarement installés par le programme d’installation de. par conséquent, la plupart des fichiers installés par le programme d’installation sont des fichiers d’application au moment de l’exécution.

 

 




