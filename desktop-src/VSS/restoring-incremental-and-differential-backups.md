---
description: La restauration d’une sauvegarde incrémentielle ou différentielle sous VSS n’est pas très différente de celle d’une autre opération de restauration VSS.
ms.assetid: 67143f6f-0bb8-4740-9289-8bbfeb7caadf
title: Restauration des sauvegardes incrémentielles et différentielles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 639919ea24f12fbc036116bd89b1630321cbae54
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414588"
---
# <a name="restoring-incremental-and-differential-backups"></a>Restauration des sauvegardes incrémentielles et différentielles

La restauration d’une sauvegarde incrémentielle ou différentielle sous VSS n’est pas très différente de celle d’une autre opération de restauration VSS.

Un enregistreur peut modifier les cibles de restauration ou demander le ciblage dirigé, et un demandeur doit gérer d’autres mappages d’emplacements et de nouvelles cibles, comme avec toute autre restauration. Toutefois, il existe deux problèmes importants à prendre en compte lors de la gestion de la restauration d’une sauvegarde incrémentielle ou différentielle : des restaurations supplémentaires et des tampons de sauvegarde.

## <a name="additional-restores"></a>Restaurations supplémentaires

Le premier problème est celui des restaurations supplémentaires. Un opérateur de sauvegarde peut avoir besoin d’exécuter plusieurs opérations de restauration à l’aide d’un support de sauvegarde complet et incrémentiel suivant ou différentiel en tant que source.

Certains Writers, généralement dans le cadre de leur gestion d’un événement [*postRestore*](vssgloss-p.md) à l’aide de [**CVssWriter :: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), utilisent des fichiers restaurés pour effectuer des mises à jour de données actuellement sur le disque. Pour certains de ces Writers, il est inefficace, ou dangereux, de mettre à jour de façon répétée les données sur disque à partir des fichiers restaurés.

Par conséquent, il est important que les applications de sauvegarde indiquent quand un jeu de composants ou de composants peut nécessiter des restaurations ultérieures en appelant [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

Un writer appelle [**IVssComponent :: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) pour déterminer si l’opérateur de sauvegarde a planifié plus de restaurations du composant ou du jeu de composants.

Si le demandeur n’a pas appelé [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores), [**IVssComponent :: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) retourne la valeur false, et le writer peut effectuer tout traitement de postconnexion à la restauration.

Si [**IVssBackupComponents :: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) a été appelé, [**IVssComponent :: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) retourne la **valeur true** et qu’un enregistreur doit décider comment gérer les opérations après la restauration, par exemple, le writer peut choisir de ne pas mettre à jour ses données sur disque.

## <a name="backup-stamps"></a>Tampons de sauvegarde

Dans le cadre de l’opération de sauvegarde complète précédente, un enregistreur peut avoir stocké un tampon de sauvegarde dans le document des composants de sauvegarde du demandeur.

Le tampon de sauvegarde est stocké sous forme de chaîne, et son format et ses informations ne sont pas intelligibles pour le demandeur. Par conséquent, le demandeur ne peut pas utiliser directement les informations de tampon de sauvegarde.

Au lieu de cela, sa tâche consiste à mettre ces informations à la disposition du writer, en appelant la méthode [**IVssBackupComponents :: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) avant la génération d’un événement [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) pour une sauvegarde incrémentielle.

Le demandeur effectue cette fonction composant par composant. Un demandeur examine les informations de tampon de sauvegarde du composant ou du jeu de composants stockés à l’aide de [**IVssComponent :: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp).

Si les informations de tampon de sauvegarde sont adaptées au type de restauration que le demandeur est en mesure d’effectuer, il est disponible en tant qu’horodatage de la dernière sauvegarde d’un composant avec la méthode [**IVssBackupComponents :: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) .

Un enregistreur récupère les informations de tampon de sauvegarde à l’aide de [**IVssComponent :: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Un enregistreur de cette classe a généré le tampon de sauvegarde initial, de sorte que l’enregistreur est en mesure de décoder ce tampon et d’utiliser les informations. En fonction de cela, lors de la gestion d’un événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , un enregistreur peut choisir de prendre des mesures telles que la modification des cibles de restauration ou la demande de ciblage dirigé.

 

 



