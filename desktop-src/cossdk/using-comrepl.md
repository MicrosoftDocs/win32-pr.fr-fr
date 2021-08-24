---
description: Utilisation de COMREPL
ms.assetid: bf67b434-c082-472d-9eae-ae31969d9cb8
title: Utilisation de COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501cca8d32383e23fc636669e32a80cfdfe96dd658717e41c1618244fc5af81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853879"
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

## <a name="notes"></a>Remarques

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

 

 



