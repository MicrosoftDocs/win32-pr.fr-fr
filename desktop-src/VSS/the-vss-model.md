---
description: VSS est conçu pour résoudre les problèmes décrits dans problèmes de sauvegarde de volume courantes.
ms.assetid: f9a3efea-d6e8-40df-92ac-f6faaa4fca60
title: Le modèle VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e65061b9496fe04769a9b2429f7e05a2064de63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516880"
---
# <a name="the-vss-model"></a>Le modèle VSS

VSS est conçu pour résoudre les problèmes décrits dans [problèmes de sauvegarde de volume courantes](common-volume-backup-issues.md).

Le modèle VSS comprend les éléments suivants :

-   Mécanisme de clichés instantanés. Le service VSS fournit une capture de volume rapide de l’état d’un disque à un instant donné, un [*cliché instantané*](vssgloss-s.md) du volume. Cette copie de volume existe côte à côte avec le volume actif et contient des copies de tous les fichiers sur le disque enregistrés et disponibles en tant qu’appareil distinct.
-   État cohérent des fichiers via la coordination des applications. VSS fournit un mécanisme COM de communication interprocessus basé sur les événements, que les processus participants peuvent utiliser pour déterminer l’état du système en ce qui concerne les opérations de sauvegarde, de restauration et de cliché instantané (capture de volume). Ces événements définissent les étapes par lesquelles les applications qui modifient les données sur le disque ([*Écritures*](vssgloss-w.md)) peuvent ramener tous leurs fichiers dans un état cohérent avant la création du cliché instantané.
-   Minimisation des temps d’arrêt des applications. Le cliché instantané VSS existe en parallèle avec une copie en direct du volume à sauvegarder. par conséquent, à l’exception de la courte période de préparation et de création du cliché instantané, une application peut continuer son travail. Le temps nécessaire pour créer réellement un cliché instantané, qui se produit entre les événements de [*gel*](vssgloss-f.md) et de [*libération*](vssgloss-t.md) , prend généralement environ une minute.

    Alors que la préparation d’un enregistreur pour un cliché instantané, notamment le vidage des e/s et de l’état de l’enregistrement (consultez [vue d’ensemble des tâches de présauvegarde](overview-of-pre-backup-tasks.md)), peut être non triviale, il est beaucoup plus rapide que le temps requis pour sauvegarder un volume, ce qui peut prendre des heures pour des volumes importants.

-   Interface unifiée avec VSS. VSS résume les mécanismes de clichés instantanés dans une interface commune tout en permettant à un fournisseur de matériel d’ajouter et de gérer les fonctionnalités uniques de ses propres fournisseurs. Toute application de sauvegarde ([*demandeur*](vssgloss-r.md)) et tout enregistreur doivent pouvoir s’exécuter sur n’importe quel système de stockage sur disque qui prend en charge l’interface VSS.
-   Sauvegarde multivolume. VSS prend en charge les jeux de clichés [*instantanés*](vssgloss-s.md), qui sont des collections de clichés instantanés, sur plusieurs types de volumes de disque de plusieurs fournisseurs. Tous les clichés instantanés d’un jeu de clichés instantanés sont créés avec le même horodatage et présentent le même état de disque pour un état de disque multivolume.
-   Prise en charge native des clichés instantanés. À partir de Windows XP, la prise en charge des clichés instantanés est disponible via VSS en tant que partie native du système d’exploitation Windows. Tant qu’au moins un disque NTFS est présent sur un système, ces systèmes peuvent être configurés pour prendre en charge les clichés instantanés de tous les systèmes de disques montés sur ceux-ci.

 

 



