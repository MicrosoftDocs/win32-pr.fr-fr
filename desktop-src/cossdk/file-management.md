---
description: Pour activer le transfert de fichiers d’application, COMREPL gère automatiquement les jeux de dossiers du système de fichiers sur la source et la cible. Ces dossiers COMREPL sont tous enracinés dans \\ la réplication com% systemdir% \\ .
ms.assetid: 8c59577b-34ea-4675-aaea-a2732fd5ce14
title: Gestion des fichiers (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e785b8fd39d94bcf623810bca950862d22ec8762
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523428"
---
# <a name="file-management"></a>Gestion des fichiers

Pour activer le transfert de fichiers d’application, COMREPL gère automatiquement les jeux de dossiers du système de fichiers sur la source et la cible. Ces dossiers COMREPL sont tous enracinés dans \\ la réplication com% systemdir% \\ .

## <a name="source-folders"></a>Dossiers sources



| Dossier                   | Objectif                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaSource<br/> | Les applications exportées pendant la phase de préparation sont stockées ici.<br/> Ce dossier est remplacé chaque fois que la phase de préparation est exécutée sur un ordinateur source donné. Ce dossier n’étant jamais explicitement supprimé, la réplication vers des cibles peut avoir lieu à tout moment après la préparation de la source.<br/> Chaque application est stockée dans son propre sous-dossier nommé <appName> + <appID> .<br/> |



 

## <a name="target-folders"></a>Dossiers cibles



| Dossier                    | Objectif                                                                                                                                                                                                                                                                                                                                      |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReplicaNew<br/>     | La phase de copie copie tous les fichiers et sous-dossiers de ReplicaSource sur la source vers ReplicaNew sur la cible. Tout contenu précédent de ReplicaNew est supprimé chaque fois que la phase de copie est exécutée sur une cible donnée.<br/> Ce dossier existe uniquement pendant l’exécution du processus de réplication. (Voir ReplicaCurrent.)<br/>           |
| ReplicaCurrent<br/> | Les applications répliquées actuellement installées sur la cible sont stockées ici.<br/> Lorsque la phase d’installation est démarrée, le dossier ReplicaNew est renommé en ReplicaCurrent. S’il existe déjà un dossier ReplicaCurrent, il est renommé en ReplicaOld. S’il existe déjà un dossier ReplicaOld, son contenu est supprimé.<br/> |
| ReplicaOld<br/>     | Enregistre les fichiers d’application installés lors de la prochaine réplication. Ces fichiers sont enregistrés à des fins de sauvegarde uniquement.<br/>                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Journalisation et rapports d’erreurs](logging-and-error-reporting.md)
</dt> <dt>

[Phases de réplication](replication-phases.md)
</dt> <dt>

[Utilisation de COMREPL](using-comrepl.md)
</dt> <dt>

[Ce qui est répliqué](what-gets-replicated.md)
</dt> </dl>

 

 




