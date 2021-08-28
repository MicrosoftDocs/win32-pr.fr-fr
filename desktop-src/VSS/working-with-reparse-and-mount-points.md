---
description: Le traitement de l’un des jeux de fichiers d’un composant peut demander à un demandeur de traverser une arborescence de répertoires de manière récursive, ce qui peut obliger le demandeur à gérer les dossiers montés et les points d’analyse (tels que les liens) qui pointent vers des données qui ne sont pas sur le volume actuel.
ms.assetid: d0e08598-a8a2-489b-9cb2-e989bed1ce53
title: Utilisation des dossiers montés et des points d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1162d1d7da5869f588ae61d9235ec3d5827265c5eb9deaa23c38b8b9e85db68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905059"
---
# <a name="working-with-mounted-folders-and-reparse-points"></a>Utilisation des dossiers montés et des points d’analyse

Le traitement de l’un des jeux de fichiers d’un composant peut demander à un demandeur de traverser une arborescence de répertoires de manière récursive, ce qui peut obliger le demandeur à gérer les dossiers montés et les points d’analyse (tels que les liens) qui pointent vers des données qui ne sont pas sur le volume actuel.

Les demandeurs doivent suivre les dossiers montés et les points d’analyse lors du parcours d’une arborescence de répertoires, et VSS a des instructions bien définies pour les gérer pour les opérations de sauvegarde et de restauration.

Pour illustrer ces instructions, prenons l’exemple suivant :

-   Le volume \\ \\ ? \\ Le volume {GUID \_ 1} contient la lettre de lecteur C : \\ .
-   Un jeu de fichiers a un chemin d’accès de C : \\ WriterData.
-   Une spécification de fichier \* . dat est utilisée par le jeu de fichiers.
-   La récursivité du jeu de fichiers est définie sur **true**.
-   Le répertoire C : \\ WriterData se trouve sur le volume \\ \\ ? \\ Volume {GUID \_ 1}.
-   Le répertoire C : \\ WriterData \\ archive est un dossier monté.
-   Le volume \\ \\ ? \\ Le volume {GUID \_ 2} est associé au dossier monté C : \\ WriterData \\ archive.

## <a name="handling-mounted-folders-and-reparse-points-during-backup"></a>Gestion des dossiers montés et des points d’analyse pendant la sauvegarde

Les règles de base pour gérer les dossiers montés et les points d’analyse sous VSS lors de l’exécution d’une sauvegarde récursive peuvent être résumées comme suit :

-   Les chemins d’accès sont suivis des dossiers montés et des points d’analyse.
-   Si un dossier monté ou un point d’analyse pointe vers un volume, ce volume doit être un cliché instantané.
-   Si un volume contient des dossiers montés ou des points d’analyse, ceux-ci s’affichent dans le cliché instantané du volume.
-   Les données qui se trouvent sous le dossier monté ou le point d’analyse sont capturées dans le cliché instantané du volume vers lequel pointe le dossier monté ou le point d’analyse.

Pour illustrer l’utilisation de l’exemple ci-dessus, étant donné que l’indicateur récursif est défini, le demandeur doit examiner toutes les données de l’archive C : \\ WriterData \\ et ci-dessous.

Le demandeur doit ajouter le volume avec la lettre de lecteur C : \\ ( \\ \\ ? \\ Volume {GUID \_ 1}) et le volume associé au dossier monté C : \\ WriterData \\ Archive ( \\ \\ ? \\ Volume {GUID \_ 2}) au jeu de clichés instantanés à l’aide de [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Le dossier monté C : \\ \\ Archive WriterData apparaît dans le cliché instantané du volume \\ \\ ? \\ Volume {GUID \_ 1}, qui a un objet d’appareil nommé deviceObject1.

Toutefois, VSS ne copiera aucune donnée dans ce dossier monté (données sur \\ \\ ? \\ Volume {GUID \_ 2}) au cliché instantané référencé par deviceObject1. Au lieu de cela, les données sont capturées dans le cliché instantané de \\ \\ ? \\ Volume {GUID \_ 2}, qui a un objet d’appareil nommé deviceObject2.

Par conséquent, un demandeur qui sauvegarde des fichiers copiés par des clichés instantanés sous C : \\ WriterData utilise le chemin d’accès deviceObject1 \\ WriterData pour rechercher les fichiers correspondant à c : \\ WriterData \\ \* . dat.

Pour sauvegarder les fichiers de clichés instantanés sous C : \\ WriterData \\ Archive, le demandeur utilise le chemin d’accès deviceObject2 (car le répertoire racine de \\ \\ ? \\ Le volume {GUID \_ 2} a été associé au dossier monté c : \\ writer \\ Archive) pour rechercher les fichiers correspondant à c : \\ WriterData \\ Archive \\ \* . dat.

Notez qu’un point d’analyse est géré de la même façon qu’un dossier monté. Le point d’analyse apparaît dans le cliché instantané du premier volume. Les données sous le point d’analyse apparaissent dans le cliché instantané du deuxième volume.

Lors de la sauvegarde, les demandeurs doivent stocker des informations sur les dossiers montés et les volumes qui leur sont associés, ainsi que sur les points d’analyse et leurs cibles pour s’assurer que toutes les données sont sauvegardées et restaurées correctement.

## <a name="handling-mount-and-reparse-points-during-restore"></a>Gestion des points de montage et d’analyse lors de la restauration

Lors de la restauration de fichiers, le demandeur doit suivre des instructions légèrement différentes de celles qui ont été utilisées pendant la sauvegarde (sans tenir compte des problèmes tels que le [*mappage d’emplacement secondaire*](vssgloss-a.md) et le [*nouvel emplacement cible*](vssgloss-n.md)) :

-   Comme précédemment, si la récursivité est requise, les chemins d’accès sont suivis sur les dossiers montés et les points d’analyse.
-   Les dossiers montés doivent être restaurés.
-   Les emplacements de restauration des dossiers montés et des points d’analyse sont ceux qui sont déterminés par leurs chemins d’accès d’origine.

Si les noms de volume persistent entre la sauvegarde et la restauration (c’est-à-dire que vous ne recréez pas les volumes), les dossiers montés restaurés et les points d’analyse doivent pointer vers les volumes appropriés.

Par conséquent, dans l’exemple ci-dessus, si le dossier monté C : \\ WriterData \\ Archive a été restauré sur ( \\ \\ ? \\ Le volume {GUID \_ 1}) et le volume précédemment associé ont été restaurés à ( \\ \\ ? \\ Volume {GUID \_ 2}), les fichiers et la structure de fichiers restaurés sont corrects et cohérents.

Il se peut que les données soient restaurées sur un système où les noms de volume changent. Cela peut être dû à des pannes de disque, dans lesquelles vous devrez peut-être effectuer une récupération manuelle du système et recréer des volumes. Dans ce type de situation, les dossiers montés et les points d’analyse ne seront plus valides après la restauration. Pour recréer les fichiers et la structure de fichiers sur le volume restauré, vous devez supprimer les dossiers montés et les points d’analyse restaurés, puis les recréer sur le disque. C’est à l’application de sauvegarde de décider si cela est approprié.

Notez qu’il est possible que la destination de restauration d’un dossier monté soit déjà occupée. Par exemple, l’archive C : \\ WriterData \\ contient peut-être déjà certains fichiers. C’est à l’application de sauvegarde de décider comment gérer cette situation.

 

 



