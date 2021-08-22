---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f20bbe9f858066d7fca09a3f263aa618c79c4174664b9a4e0994c900fb81c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998049"
---
# <a name="b-volume-shadow-copy-service"></a>B (Service VSS)

[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**applications de niveau principal**
</dt> <dd>

Indique le point auquel un writer est notifié d’un gel par VSS. Les enregistreurs qui sont initialisés en tant qu’applications de niveau principal sont avertis après que les Writers ont été initialisés en tant qu’applications de niveau frontal et antérieurs à ceux qui sont initialisés en tant qu’applications au niveau du système. Voir aussi [*niveau application*](vssgloss-a.md), [*applications de niveau frontal*](vssgloss-f.md), [*applications système*](vssgloss-s.md), [*enregistreur*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Événement BackupComplete**
</dt> <dd>

Événement VSS indiquant qu’une sauvegarde VSS est terminée. Cet événement doit être suivi d’un événement BackupShutdown en fonctionnement normal. Voir aussi *événement BackupShutdown*.

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Document sur les composants de sauvegarde**
</dt> <dd>

Document XML créé par un demandeur (à l’aide de l’interface **IVssBackupComponents** ) au cours de la configuration d’une opération de restauration ou de sauvegarde. Le document des composants de la sauvegarde contient une liste des composants explicitement inclus, provenant d’un ou de plusieurs enregistreurs, qui participent à une opération de sauvegarde ou de restauration. Il ne contient pas d’informations sur les composants inclus implicitement. En revanche, un document des métadonnées de l’enregistreur contient seulement des composants d’enregistreur qui peuvent participer à une sauvegarde.

Un document de composants de sauvegarde peut être enregistré sur le disque. Voir aussi [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**jeu de sauvegarde**
</dt> <dd>

Fichiers à sauvegarder. Il inclut les fichiers sélectionnés par inclusion dans un composant, ceux indiqués par les instructions include au niveau de l’enregistreur, moins les fichiers qui ont été explicitement inclus.

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Événement BackupShutdown**
</dt> <dd>

Événement VSS indiquant qu’une application de sauvegarde conforme s’est arrêtée. Normalement, il est précédé d’un événement BackupComplete. Toutefois, si une sauvegarde se termine de manière inattendue, cet événement peut être généré sans événement BackupComplete précédent. Voir aussi *événement BackupComplete*.

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**tampon de sauvegarde**
</dt> <dd>

Chaîne contenant les informations relatives au moment où une sauvegarde a eu lieu. VSS n’impose aucune restriction sur le format de cette chaîne, à ceci près qu’il est intelligible pour toutes les instances d’écriture d’une classe donnée. Il peut contenir des informations de date et d’heure, des numéros de séquence logique ou toute autre information qui permettra à un rédacteur de la même classe de déterminer à quel moment la dernière sauvegarde a eu lieu.

</dd> </dl>

 

 



