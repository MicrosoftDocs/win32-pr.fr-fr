---
description: VSS permet à un demandeur d’accéder au cliché instantané de volumes contenant des données pour la sauvegarde et de copier des données sur un support de sauvegarde.
ms.assetid: 187f26f2-f191-4703-9bde-3357f1ceef0c
title: Vue d’ensemble de la sauvegarde réelle des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a504ff5a41725e33a2eb27792a3c6c89d00276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539087"
---
# <a name="overview-of-actual-backup-of-files"></a>Vue d’ensemble de la sauvegarde réelle des fichiers

VSS permet à un demandeur d’accéder au cliché instantané de volumes contenant des données pour la sauvegarde et de copier des données sur un support de sauvegarde. Les enregistreurs poursuivent généralement le fonctionnement normal au cours de ce processus. Pour plus d’informations, consultez [vue d’ensemble du traitement d’une sauvegarde sous VSS](overview-of-processing-a-backup-under-vss.md).

Le tableau suivant présente la séquence des actions et des événements qui sont requis pour la sauvegarde des fichiers.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Action du demandeur</th>
<th>Événement</th>
<th>Action d’écriture</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Accéder aux fichiers sur le volume de clichés instantanés (voir <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties"><strong>IVssBackupComponents :: GetSnapshotProperties</strong></a>, <a href="/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop"><strong>VSS_SNAPSHOT_PROP</strong></a>)</td>
<td>Aucune</td>
<td>Aucune</td>
</tr>
<tr class="even">
<td>Générez la liste des fichiers à sauvegarder et copiez les données du fichier sur le support de sauvegarde.</td>
<td>Aucune</td>
<td>Aucune</td>
</tr>
<tr class="odd">
<td>Indique la réussite ou l’échec de la sauvegarde avec <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded"><strong>IVssBackupComponents :: SetBackupSucceeded</strong></a>.</td>
<td>Aucune</td>
<td>Aucune</td>
</tr>
<tr class="even">
<td>Le demandeur indique que la sauvegarde s’est terminée en appelant <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents :: BackupComplete</strong></a>.</td>
<td><a href="vssgloss-b.md"><em>BackupComplete</em></a></td>
<td>Effectuez un nettoyage après la sauvegarde (consultez <a href="/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete"><strong>CVssWriter :: OnBackupComplete</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents"><strong>IVssWriterComponents</strong></a>, <a href="/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent"><strong>IVssComponent</strong></a>).</td>
</tr>
<tr class="odd">
<td>Le demandeur attend que tous les enregistreurs accusent réception de l’événement <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete"><strong>IVssBackupComponents :: BackupComplete</strong></a> à l’aide de <a href="/windows/desktop/api/Vss/nn-vss-ivssasync"><strong>IVssAsync</strong></a>. Il doit également vérifier l’état de l’enregistreur (consultez <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus"><strong>IVssBackupComponents :: GatherWriterStatus</strong></a>, <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus"><strong>IVssBackupComponents :: GetWriterStatus</strong></a>). Le demandeur doit appeler <strong>GatherWriterStatus</strong> à ce stade pour que la session de l’enregistreur soit définie sur un état terminé.
<blockquote>
[!Note]<br />
Cela n’est nécessaire que sur Windows Server 2008 avec Service Pack 2 (SP2) et versions antérieures.
</blockquote>
<br/></td>
<td>Aucune</td>
<td>Aucune</td>
</tr>
<tr class="even">
<td>Enregistrez le document des composants de sauvegarde et chaque document de métadonnées de l’enregistreur dans des documents XML, qui peuvent être écrits sur le support de sauvegarde (consultez <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml"><strong>IVssBackupComponents :: SaveAsXML</strong></a> et <a href="/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml"><strong>IVssExamineWriterMetadata :: SaveAsXML</strong></a>).</td>
<td>Aucune</td>
<td>Aucune</td>
</tr>
</tbody>
</table>



 

## <a name="writer-actions-during-backup-of-files"></a>Actions d’écriture lors de la sauvegarde de fichiers

Une fois le cliché instantané terminé, toutes les opérations d’e/s sur le système sauvegardées doivent pouvoir reprendre sans interrompre l’intégrité de la sauvegarde. Il s’agit de l’une des principales motivations pour disposer de la fonctionnalité de cliché instantané.

Par conséquent, comme dans la phase de découverte (voir [vue d’ensemble de la phase de découverte de sauvegarde](overview-of-the-backup-discovery-phase.md)), il y a peu de demandes placées sur les enregistreurs lors de la sauvegarde de fichiers.

Une fois qu’une sauvegarde est terminée et qu’un demandeur a généré un événement [*BackupComplete*](vssgloss-b.md) , VSS appelle la méthode [**CVssWriter :: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) de chaque enregistreur, une méthode virtuelle qui, par défaut, retourne simplement **true**. Toutefois, les Writers peuvent remplacer l’implémentation par défaut et effectuer des actions telles que la suppression des fichiers temporaires restants, ou utiliser l’interface [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) avec laquelle elle est appelée pour vérifier l’état de la sauvegarde de chacun de ses composants [*inclus explicitement*](vssgloss-e.md) (et de tout [*ensemble de composants*](vssgloss-c.md) qu’ils peuvent définir) en extrayant l’objet [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondant. Le rédacteur peut ensuite déterminer et agir sur la réussite ou l’échec de la sauvegarde en appelant [**IVssComponent : GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded). La valeur retournée par **IVssComponent : GetBackupSucceeded** est **true** uniquement si tous les fichiers inclus explicitement dans le composant et tous les éléments [*implicitement inclus*](vssgloss-i.md) de l’un de ses sous- [*composants*](vssgloss-s.md) ont été correctement sauvegardés.

Lorsque l’appel à [**CVssWriter :: OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) est terminé, le demandeur doit appeler [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (pour chaque Writer) une dernière fois. La mémoire de l’état de session du writer est une ressource limitée et les enregistreurs doivent finalement réutiliser les États de session. Cette étape marque l’état de la session de sauvegarde du writer comme étant terminé et notifie à VSS que cet emplacement de session de sauvegarde peut être réutilisé par une opération de sauvegarde ultérieure.

## <a name="requester-actions-during-backup-of-files"></a>Actions du demandeur pendant la sauvegarde des fichiers

Comme indiqué dans [vue d’ensemble de la phase de découverte de la sauvegarde](overview-of-the-backup-discovery-phase.md), vous ne devez pas générer la liste réelle des fichiers à sauvegarder tant que le cliché instantané n’est pas terminé.

L' [*objet appareil*](vssgloss-d.md) correspondant au cliché instantané d’un volume donné est utilisé pour obtenir l’accès aux fichiers sur le volume des clichés instantanés une fois que le cliché instantané est terminé. L’objet appareil est obtenu à partir de l’objet [**\_ \_ prop instantané VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) renvoyé par [**IVssBackupComponents :: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties). Chaque cliché instantané d’un jeu de clichés instantanés aura son propre objet appareil.

L’objet appareil et les chemins obtenus à partir des spécifications du document de métadonnées de l’enregistreur sont ensuite utilisés pour sélectionner les fichiers à sauvegarder. Pour plus d’informations, consultez [l’accès du demandeur aux clichés instantanés des données](requestor-access-to-shadow-copied-data.md) .

Les fichiers qui seront inclus dans la liste de sauvegarde dépendent de la nature de la sauvegarde particulière, de la sélectivité des composants [*pour la sauvegarde*](vssgloss-s.md)et de la structure du chemin d’accès logique du writer (voir utilisation de la [sélectivité pour la sauvegarde](working-with-selectability-for-backup.md)).

En plus des fichiers spécifiés dans les composants, un writer donné peut également avoir des fichiers explicitement exclus. L’exclusion de fichier doit toujours être respectée, quels que soient les composants sélectionnés.

Comme indiqué dans [vue d’ensemble de la phase de découverte de sauvegarde](overview-of-the-backup-discovery-phase.md), un dossier monté ou un point d’analyse peut apparaître dans un cliché instantané et peut être sauvegardé. Toutefois, un dossier monté ou un point d’analyse ne peut pas être parcouru sur le volume cliché instantané (voir [utilisation des dossiers montés et des points d’analyse](working-with-reparse-and-mount-points.md)).

Vous devez également prendre garde pendant une opération de sauvegarde, si le [*chemin alternatif*](vssgloss-a.md) retourné par [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) n’est pas vide. Un autre chemin d’accès diffère d’un [*autre mappage d’emplacement*](vssgloss-a.md) en ce qu’il est utilisé uniquement pendant les sauvegardes, alors qu’un autre mappage d’emplacement est utilisé uniquement pendant les restaurations.

Dans ce cas, les données ne doivent pas être sauvegardées à partir de leur emplacement normal (indiqué par [**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), mais à partir de l’emplacement retourné par [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation). Lors de la restauration, le fichier doit être renvoyé à son emplacement normal. Pour plus d’informations, consultez [emplacements de sauvegarde et de restauration non par défaut](non-default-backup-and-restore-locations.md) .

VSS n’impose aucune restriction sur le mécanisme réel de sauvegarde des données sur un support de stockage ou sur le choix de cette moyenne. Toutefois, il est recommandé de traiter les fichiers de chaque composant de chaque [*instance de writer*](vssgloss-w.md) comme une unité. Pour plus d’informations sur les meilleures pratiques pour la génération de la liste des fichiers de sauvegarde, consultez [génération d’un jeu de sauvegarde](generating-a-backup-set.md) .

La réussite ou l’échec de la sauvegarde de tous les fichiers gérés par un composant donné et (s’il définit un [*jeu de composants*](vssgloss-c.md)). ses sous- [*composants*](vssgloss-s.md) pour une instance de writer donnée doivent être conservés dans le document des composants de sauvegarde en appelant [**IVssBackupComponents :: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded). Si un fichier géré par un composant ou un jeu de composants ne parvient pas à sauvegarder, l’ensemble du composant est considéré comme ayant échoué. Les informations exactes relatives au fichier qui n’a pas pu être sauvegardé doivent toujours être journalisées.

Les développeurs peuvent trouver utile de stocker un enregistrement sur le support de sauvegarde des fichiers qui sont sauvegardés, les composants et le jeu de composants dont ils étaient membres, leur spécification et leurs chemins d’origine. Il peut également être utile de stocker des informations telles que la définition de chaque composant de l’enregistreur. Cela peut rendre l’opération de récupération plus simple. Toutefois, ces détails sont laissés au développeur du demandeur.

Étant donné que les enregistreurs peuvent modifier le document des composants de sauvegarde lors de la gestion de l’événement [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) généré par l’appel du demandeur à [**IVssBackupComponents ::D Osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), le document des composants de sauvegarde ne doit pas être enregistré tant que cet appel asynchrone n’est pas terminé.

Bien qu’elle puisse avoir lieu plus tôt, elle est également un moment pratique pour enregistrer le document de métadonnées de l’enregistreur.

Il est très important que le document des composants de sauvegarde et les documents de métadonnées de l’enregistreur soient conservés à l’aide de [**IVssBackupComponents :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) et [**IVssExamineWriterMetadata :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml). Si ce n’est pas le cas, il n’est pas possible d’utiliser VSS lors de la restauration des fichiers.

Outre le stockage des métadonnées d’origine, certaines applications de sauvegarde peuvent être utiles pour enregistrer une copie de leur propre liste des fichiers (dans leur propre format optimisé), ainsi que leur auteur, composant, procédure de restauration et procédure de restauration associés, sur le support de sauvegarde en vue d’une récupération ultérieure. Une telle liste peut être utilisée pour éviter une partie de l’analyse et de la comparaison des documents de métadonnées de l’enregistreur et des documents du composant de sauvegarde lors de la restauration.

Les volumes en cours de sauvegarde peuvent contenir des données qui ne sont pas gérées par les enregistreurs VSS. Ces données peuvent et doivent être sauvegardées à partir du volume de clichés instantanés, où elles seront dans un [*État de cohérence*](vssgloss-c.md)en cas d’incident. Pour plus d’informations, consultez [sauvegardes sans participation au rédacteur](backups-without-writer-participation.md) .

 

 




