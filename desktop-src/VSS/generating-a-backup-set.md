---
description: Un jeu de sauvegarde est une liste de tous les fichiers à sauvegarder, de leur emplacement et de la manière de les sauvegarder.
ms.assetid: 34a66a9c-c1bc-437d-b034-59dc0c88228c
title: Génération d’un jeu de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120643c827afdabfbb9a2c347fa16290e03969f0e87f913b0c5d9fdb682f2619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122117"
---
# <a name="generating-a-backup-set"></a>Génération d’un jeu de sauvegarde

Un jeu de sauvegarde est une liste de tous les fichiers à sauvegarder, de leur emplacement et de la manière de les sauvegarder.

Un demandeur doit utiliser les fichiers contenus sur les volumes clichés instantanés une fois que le [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) a réussi à générer la liste complète des fichiers à sauvegarder.

En outre, un demandeur doit gérer la possibilité que certains fichiers aient [*d’autres chemins d’accès*](vssgloss-a.md) et que certains fichiers aient été exclus.

Un algorithme permettant de sélectionner les fichiers à sauvegarder doit être placé sur une [*instance de writer*](vssgloss-w.md) par l’instance de writer, composant par composant (comme c’est le cas lors de la restauration ; consultez [génération d’un jeu de restauration](generating-a-restore-set.md)) et peut continuer en procédant comme suit :

1.  Détermination des volumes contenant les fichiers de l’enregistreur et des objets périphériques correspondants
2.  À l’aide des informations sur le [*jeu de fichiers*](vssgloss-f.md) (contenues dans les objets [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) retournés par [**IVssExamineWriterMetadata :: GetExcludeFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)) pour créer une liste des fichiers explicitement exclus, si nécessaire, à l’aide de **FindFileFirst**, **FindFileFirstEx** et **FindNextFile**.
3.  Itération sur tous les composants d’un enregistreur, à l’aide de [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). Si un composant sélectionnable est sélectionné, utilisez le [*chemin d’accès logique*](vssgloss-l.md) pour obtenir les composants qui ne sont pas sélectionnables associés dans un jeu de composants. (Voir [utilisation de la sélectivité et des chemins logiques](working-with-selectability-and-logical-paths.md).)
4.  Obtention des [*jeux de fichiers*](vssgloss-f.md) contenus dans chaque composant sélectionné à l’aide de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) correspondant à chaque composant qu’il contient.
5.  Génération d’une liste de fichiers à partir des spécifications, si nécessaire, à l’aide de **FindFileFirst**, **FindFileFirstEx** et **FindNextFile**.
6.  Vérification de chaque fichier de la liste générée à partir des informations relatives aux composants par rapport à la liste des fichiers exclus générés ci-dessus. Cela doit être fait à l’aide du chemin d’accès par défaut pour le fichier (retourné par [**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), et non par le chemin d’accès de remplacement retourné par [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)). Si le fichier correspond à la liste exclue, il ne sera pas sauvegardé.
7.  Choix de l’emplacement réel à partir duquel effectuer la sauvegarde (en utilisant le chemin alternatif s’il a été défini)
8.  À ce stade, une liste complète de fichiers et de leurs emplacements est disponible et une sauvegarde peut commencer.

Après la génération d’un jeu de sauvegarde initial pour tous les enregistreurs présents sur le système, le demandeur vérifie ensuite la clé de Registre suivante :

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ FilesNotToBackup**

Le demandeur utilise les sous-clés sous cette clé comme suit :

-   Si un enregistreur est présent sur le système, et qu’il existe une sous-clé dont le nom correspond au nom du writer, cette sous-clé doit être ignorée.
-   Si un enregistreur est présent sur le système mais qu’il est actuellement absent du jeu de sauvegarde et qu’il existe une sous-clé correspondante, tous les fichiers spécifiés dans les données de la sous-clé sont exclus et doivent être supprimés du jeu de sauvegarde.
-   L’application de sauvegarde ajoute des fichiers aux données de sous-clé en créant une valeur à plusieurs \_ valeurs SZ contenant une liste de spécifications de fichiers pour les fichiers qui ne doivent pas être sauvegardés. Chaque chaîne dans la valeur à plusieurs \_ SZ doit contenir une spécification de fichier.
-   Les spécifications de fichier peuvent contenir le ? et les \* caractères génériques. Une spécification peut être rendue récursive en ajoutant la valeur/s à la fin. Par exemple, si vous spécifiez « % TEMP% \\ \* /s », tous les fichiers du répertoire% Temp% et de tous ses sous-répertoires ne sont pas sauvegardés.

 

 



