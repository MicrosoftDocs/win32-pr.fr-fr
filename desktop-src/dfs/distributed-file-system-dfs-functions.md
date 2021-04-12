---
title: Fonctions de système de fichiers DFS (DFS)
description: Les fonctions de système de fichiers DFS (DFS) offrent la possibilité de regrouper logiquement des partages sur plusieurs serveurs et de lier en toute transparence des partages dans un espace de noms hiérarchique unique. DFS organise les ressources partagées sur un réseau dans une structure arborescent.
ms.assetid: a29cde3e-483a-4658-94d4-27398f66abfb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73738d4f503d10e7668f0f323583f49604e3a90d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201096"
---
# <a name="distributed-file-system-dfs-functions"></a>Fonctions de système de fichiers DFS (DFS)

Les fonctions de système de fichiers DFS (DFS) offrent la possibilité de regrouper logiquement des partages sur plusieurs serveurs et de lier en toute transparence des partages dans un espace de noms hiérarchique unique. DFS organise les ressources partagées sur un réseau dans une structure arborescent.

DFS prend en charge les espaces de noms DFS *autonomes* , ceux avec un serveur hôte et les espaces de noms *basés sur un domaine* qui ont plusieurs serveurs hôtes et une haute disponibilité. Les *données de topologie* DFS pour les espaces de noms basés sur un domaine sont stockées dans Active Directory. Les données incluent la racine DFS, les liens DFS et les cibles DFS.

Chaque structure d’arborescence DFS a une ou plusieurs *cibles racines*. La cible racine est un serveur hôte qui exécute le service DFS. Une structure d’arborescence DFS peut contenir un ou plusieurs *liens DFS*. Chaque lien DFS pointe vers un ou plusieurs dossiers partagés sur le réseau. Vous pouvez ajouter, modifier et supprimer des liens DFS à partir d’un espace de noms DFS. Lorsque vous supprimez la dernière cible associée à un lien DFS, DFS supprime le lien DFS dans l’espace de noms DFS. (Dans la documentation précédente, les liens DFS étaient appelés « points de jonction ».)

Un lien DFS peut pointer vers un ou plusieurs dossiers partagés. les dossiers sont appelés *cibles*. Lorsque les utilisateurs accèdent à un lien DFS, le serveur DFS sélectionne un ensemble de cibles en fonction des informations de site d’un client. Le client accède à la première cible disponible dans le jeu. Cela permet de distribuer les demandes des clients sur les cibles possibles et peut fournir une accessibilité continue aux utilisateurs même en cas de défaillance de certains serveurs.

Une application peut utiliser les fonctions DFS pour effectuer les opérations suivantes :

- Ajoutez un lien DFS à une racine DFS.
- Créez ou supprimez des espaces de noms DFS autonomes et basés sur un domaine.
- Ajoutez des cibles à un lien DFS existant.
- Supprimer un lien DFS d’une racine DFS.
- Supprimer une cible d’un lien DFS.
- Affichez et configurez des informations sur les racines et les liens DFS.

Pour obtenir la liste des fonctions DFS, consultez [système de fichiers DFS Functions](distributed-file-system-functions.md).

Pour obtenir la liste des structures DFS, consultez [système de fichiers DFS structures](distributed-file-system-structures.md).

Les cibles sur les ordinateurs qui exécutent Microsoft Windows peuvent être publiées dans un espace de noms DFS. Vous pouvez également publier les partages non Microsoft pour lesquels les redirecteurs clients sont disponibles dans un espace de noms DFS. Toutefois, contrairement à un partage qui est publié sur un serveur qui exécute Windows Server, il ne peut pas héberger de racine DFS ou fournir des références à d’autres cibles DFS.

DFS utilise le service de réplication de fichiers de Windows Server pour copier les modifications entre les cibles répliquées. Les utilisateurs peuvent modifier des fichiers stockés sur une cible et le service de réplication de fichiers propage les modifications vers les autres cibles désignées. Le service conserve la modification la plus récente apportée à un document ou à des fichiers.
