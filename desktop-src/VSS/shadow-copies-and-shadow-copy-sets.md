---
description: Un cliché instantané est une capture instantanée d’un volume qui duplique toutes les données qui sont conservées sur ce volume à un instant bien défini. VSS identifie chaque cliché instantané par un GUID persistant.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Clichés instantanés et jeux de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18709842b1fb0fbf6d6cce2557b51042dfb024ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527420"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Clichés instantanés et jeux de clichés instantanés

Un cliché [*instantané*](vssgloss-s.md) est une capture instantanée d’un volume qui duplique toutes les données qui sont conservées sur ce volume à un instant bien défini. VSS identifie chaque cliché instantané par un GUID persistant.

Un jeu de clichés [*instantanés*](vssgloss-s.md) est une collection de clichés instantanés de différents volumes exécutés en même temps. VSS identifie chaque jeu de clichés instantanés par un GUID persistant.

La manière dont un fournisseur de matériel ou de logiciels particulier choisit d’implémenter des clichés instantanés est entièrement à sa discrétion. Une fois qu’un cliché instantané est créé, deux images du volume cliché instantané sont effectivement disponibles sur le système : le volume d’origine, qui est accessible de manière conventionnelle. et les données copiées, accessibles via l’API VSS.

Cela permet à deux ensembles d’activités d’avoir lieu en même temps :

-   Les applications ordinaires sur le système peuvent rapidement continuer ou reprendre en utilisant le volume d’origine, en mettant à jour les données sur le disque.
-   Les applications qui utilisent l’API du demandeur VSS pour accéder au volume copié par cliché instantané peuvent effectuer des sauvegardes ou des opérations similaires.

Les clichés instantanés ne doivent pas être implémentés de la même façon pour chaque fichier, répertoire ou volume. Différentes implémentations du mécanisme de cliché instantané ([*fournisseurs*](vssgloss-p.md)) peuvent utiliser des approches différentes pour créer un cliché instantané. Toutefois, pour toutes les applications qui utilisent l’API VSS, tous les clichés instantanés doivent être identiques.

Pour plus d’informations sur l’implémentation par défaut du fournisseur Windows, consultez [fournisseur système](providers.md).

## <a name="default-shadow-copy-state"></a>État du cliché instantané par défaut

Même si le système de fichiers vide toutes les mémoires tampons d’e/s avant de créer un cliché instantané, cela ne garantit pas que les e/s incomplètes sont correctement gérées.

Par conséquent, en supposant que le système ne dispose d’aucune application VSS, les données d’un cliché instantané sont dites dans un [*État de cohérence*](vssgloss-c.md)en cas d’incident. Un cliché instantané dans un état de cohérence en cas d’incident contient une image du disque qui est la même que celle qui existe à la suite d’un arrêt catastrophique du système. Tous les fichiers qui étaient ouverts sont toujours présents sur le volume, mais il n’est pas garanti qu’ils soient exempts d’opérations d’e/s incomplètes ou d’une altération des données.

Bien que l’état de cohérence des incidents ne traite pas entièrement tous les problèmes liés à la définition d’un jeu de sauvegarde stable (voir [problèmes de sauvegarde de volume courants](common-volume-backup-issues.md)), il présente plusieurs avantages par rapport au jeu de sauvegarde que les opérations de sauvegarde conventionnelles devraient utiliser :

-   Un volume contenu dans un cliché instantané, même dans un état cohérent en incident, contient toujours tous les fichiers. Un jeu de sauvegarde créé sans cliché instantané ne contient pas tous les fichiers ouverts au moment de la sauvegarde. Les fichiers maintenus ouverts au moment de l’opération de sauvegarde sont exclus de la sauvegarde.
-   Le cliché instantané du volume est créé à un instant donné et non en parcourant un système de fichiers actif, ce qui nécessite généralement plus de temps.

Les applications sur un système qui ne prennent pas en charge VSS (traitement de texte, éditeurs, etc.) auront probablement leurs fichiers dans un état de cohérence en cas d’incident. Toutefois, les applications prenant en charge VSS (enregistreurs) peuvent coordonner leurs actions afin que l’état de leurs fichiers dans le cliché instantané soit bien défini et cohérent.

## <a name="shadow-copy-freeze-and-thaw"></a>Figer et libérer le cliché instantané

La création de chaque opération de cliché instantané VSS est déplacée entre les événements [*Freeze*](vssgloss-f.md) et [*dégeler*](vssgloss-t.md) , utilisés par les enregistreurs pour mettre leurs fichiers dans un état stable avant le cliché instantané.

Le fait d’avoir des événements Freeze et dégeler dans le cadre du modèle VSS signifie :

-   La gestion de l’événement Freeze signifie que ceux qui développent des enregistreurs doivent avoir un point clairement délimité dans le cycle de sauvegarde, où ils garantissent que toutes les opérations d’écriture sur le disque sont arrêtées et que les fichiers sont dans un état bien défini pour la sauvegarde.
-   La gestion de l’événement de libération fournit le mécanisme permettant aux rédacteurs de reprendre les écritures sur le disque et de nettoyer tous les fichiers temporaires ou autres informations d’état temporaire qui ont été créés en association avec le cliché instantané.
-   La fenêtre par défaut entre les événements Freeze et dégeler est abrégée (en général, 60 secondes). par conséquent, l’interruption réelle d’un service fourni par un writer peut être réduite.
-   La gestion d’autres événements (tels que PrepareForSnapshot) qui précèdent et suivent les événements Freeze et dégeler, fournit respectivement la flexibilité nécessaire pour permettre aux rédacteurs d’effectuer des opérations complexes afin de prendre en charge les clichés instantanés.

 

 



