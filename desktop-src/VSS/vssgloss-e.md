---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305a02633e8ed2aca1e372f250d6d91a8560ef1cb7a9f565e64aea6924397ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905129"
---
# <a name="e-volume-shadow-copy-service"></a>E (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) e [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusion explicite de composant**
</dt> <dd>

Ajout des informations d’un composant au document des composants de sauvegarde d’un demandeur lorsqu’il participe à une opération de sauvegarde ou de restauration. Les demandeurs utilisent [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour inclure explicitement un composant dans une opération de sauvegarde, et [**IVssBackupComponents :: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) ou [**IVssBackupComponents :: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) pour inclure explicitement un composant dans une opération de restauration.

Si un composant d’un enregistreur est sauvegardé ou restauré, tous les composants non sélectionnables sans ancêtres sélectionnables doivent être inclus explicitement dans une opération de sauvegarde ou de restauration.

Les composants sélectionnables sans les ancêtres sélectionnables choisis par un demandeur pour la participation à une sauvegarde ou une restauration doivent être inclus explicitement dans l’opération.

Les composants non sélectionnables avec un ancêtre sélectionnable ne sont jamais explicitement inclus.

Les composants sélectionnables avec un ancêtre sélectionnable peuvent être inclus de manière explicite, ou peuvent être inclus implicitement si l’ancêtre est inclus explicitement.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**clichés instantanés exposés**
</dt> <dd>

Cliché instantané de volume monté sur un système et disponible pour les processus autres que celui qui le gère. Un volume de clichés instantanés monté sous une lettre de lecteur ou un emplacement de répertoire est appelé « localement exposé ». Un volume de clichés instantanés accessible via un partage (à l’exception des clichés instantanés accessibles aux clients) est appelé « exposé à distance ». Tous les clichés instantanés exposés sont également des clichés instantanés en surface. Voir aussi cliché [*instantané accessible*](vssgloss-c.md)par le client, cliché [*instantané*](vssgloss-s.md).

</dd> </dl>

 

 



