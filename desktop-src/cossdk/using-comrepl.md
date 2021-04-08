---
description: Utilisation de COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Utilisation de COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb39640998b3b27ac25cbab2ae60948418d6cee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748637"
---
# <a name="using-comrepl"></a>Utilisation de COMREPL

Pour lancer l’utilitaire de ligne de commande COMREPL, procédez comme suit :

1.  Ajoutez% windir% \\ system32 \\ com au chemin d’accès de l’environnement par défaut en tapant ce qui suit dans l’invite de commandes :

    **définir le chemin d’accès =% PATH%;% WINDIR% \\ system32 \\ com**

2.  Entrez la commande COMREPL suivante :

    **Comrepl** *ordinateursource sera* *targetComputerList* **\[ \[ /n \] /v \]**

    où :

    -   *ordinateursource sera* est le nom d’ordinateur de la source

    -   *targetComputerList* est le nom de l’ordinateur des cibles séparées par des espaces

    -   **/n** supprime l’invite de confirmation avant de démarrer la réplication

    -   **/v** renvoie la sortie du fichier journal vers la console

## <a name="notes"></a>Notes

-   Étant donné que COM+ n’est pas répliqué (uniquement les données de configuration et les applications), COM+ doit déjà être installé sur tous les ordinateurs cibles.
-   L’utilisateur doit passer des vérifications de rôle pour l’application système sur les ordinateurs source et cible.
-   Aucun compte d’ordinateur local pouvant être utilisé par des rôles n’est répliqué.
-   Le ou les ordinateurs cibles doivent être en ligne.
-   L’utilisateur est responsable de la réplication de toutes les données non-COM + (par exemple, les tables de base de données, les fichiers de données, etc.) sur le ou les ordinateurs cibles.
-   Les clusters peuvent participer à la réplication, mais notez que COMREPL est répliqué uniquement sur les ordinateurs nommés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des fichiers](file-management.md)
</dt> <dt>

[Journalisation et rapports d’erreurs](logging-and-error-reporting.md)
</dt> <dt>

[Phases de réplication](replication-phases.md)
</dt> <dt>

[Ce qui est répliqué](what-gets-replicated.md)
</dt> </dl>

 

 



