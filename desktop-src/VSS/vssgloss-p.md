---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbcf3f9d4938e407b82c58482cabab08156c3b9fabac6c1770ec20d0a40394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121609"
---
# <a name="p-volume-shadow-copy-service"></a>P (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**prise en charge partielle des fichiers**
</dt> <dd>

Capacité à implémenter des opérations de sauvegarde en modifiant les sous-sections des fichiers impliqués, plutôt que d’utiliser l’ensemble des fichiers. Voir aussi [*ciblage dirigé*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**cliché instantané persistant**
</dt> <dd>

Cliché instantané qui n’est pas supprimé automatiquement lorsque le demandeur libère un objet [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou lorsque l’ordinateur est redémarré. Voir aussi cliché [*instantané avec mise en sortie automatique*](vssgloss-a.md), cliché [*instantané*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Duplex**
</dt> <dd>

Type spécial de volume de clichés instantanés qui représente entièrement et complètement un volume de clichés instantanés sans avoir besoin de l’un des volumes originaux. Il s’agit également d’un miroir scindé, mais cette documentation utilise le terme Plex.

</dd> <dt>

<span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Événement PostRestore**
</dt> <dd>

Événement VSS indiquant qu’une restauration VSS est terminée.

</dd> <dt>

<span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Événement PostSnapshot**
</dt> <dd>

Événement VSS indiquant qu’un cliché instantané a été effectué. Voir aussi cliché [*instantané*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Événement PrepareForBackup**
</dt> <dd>

Événement VSS indiquant qu’une opération de sauvegarde est sur le point d’être effectuée.

</dd> <dt>

<span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Événement PrepareForSnapshot**
</dt> <dd>

Événement VSS indiquant que les rédacteurs doivent prendre des mesures pour préparer une opération de cliché instantané à venir. Voir aussi cliché [*instantané*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Événement de prérestauration**
</dt> <dd>

Événement VSS indiquant qu’une opération de restauration est sur le point d’être effectuée.

</dd> <dt>

<span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**moteur**
</dt> <dd>

Objet de système d’exploitation qui intercepte et gère les demandes d’e/s afin de créer et de représenter des clichés instantanés de volume dans le système de fichiers. Voir aussi [*fournisseur de matériel*](vssgloss-h.md), [*fournisseur de logiciels*](vssgloss-s.md).

</dd> </dl>

 

 



