---
title: Passage à l’État en cours d’exécution
description: Passage à l’État en cours d’exécution
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855537"
---
# <a name="entering-the-running-state"></a>Passage à l’État en cours d’exécution

Lorsqu’un objet incorporé effectue la transition vers l’État en cours d’exécution, le gestionnaire d’objets doit localiser et exécuter l’application serveur afin d’utiliser les services fournis par le serveur. Les objets incorporés sont placés à l’État en cours d’exécution, soit explicitement via une requête du conteneur, par exemple, il est nécessaire de dessiner un format qui n’est pas actuellement mis en cache, ou implicitement par OLE en réponse à l’appel d’une opération, par exemple lorsqu’un utilisateur du conteneur double-clique sur l’objet.

Lorsqu’un objet lié rend la transition à l’État en cours d’exécution, le processus est appelé *liaison*. Dans le processus de liaison, le gestionnaire d’objets demande à son moniker stocké de localiser les données du lien, puis exécute l’application serveur.

À première vue, la liaison d’un objet lié semble ne pas être plus compliquée que l’exécution d’un objet incorporé. Toutefois, les points suivants compliquent le processus :

-   Un lien peut faire référence à un objet, ou une partie de celui-ci, qui est incorporé dans un autre conteneur. Cette fonctionnalité implique un potentiel pour les incorporations imbriquées. Pour résoudre les références à une telle hiérarchie, vous devez parcourir de manière récursive un *moniker composite*, en commençant par le membre le plus à droite.
-   Lorsque la source de la liaison est en cours d’exécution, OLE se lie à l’instance en cours d’exécution de l’objet au lieu d’exécuter une autre instance. Dans le cas d’objets incorporés imbriqués, dont l’un est la source de la liaison, OLE doit être en mesure d’effectuer une liaison à un objet déjà en cours d’exécution à tout moment.
-   L’exécution d’un objet requiert l’accès à la zone de stockage pour l’objet. Lorsqu’un objet incorporé est exécuté, OLE reçoit un pointeur vers le stockage pendant le processus de chargement, qu’il transmet à l’application serveur OLE. Toutefois, pour les objets liés, il n’existe pas d’interface standard pour accéder au stockage. L’application serveur OLE peut utiliser l’interface du système de fichiers ou un autre mécanisme.

 

 




