---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751540"
---
# <a name="i-volume-shadow-copy-service"></a>I (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identifier l’événement**
</dt> <dd>

Événement VSS indiquant qu’un enregistreur ou un demandeur doit interroger le writer actuel. Il est utilisé pour construire les informations de métadonnées du writer actuel. Voir aussi [*demandeur*](vssgloss-r.md), [*enregistreur*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusion de composant implicite**
</dt> <dd>

Ne pas ajouter les informations d’un composant au document des composants de sauvegarde d’un demandeur lorsqu’il participe à une opération de sauvegarde ou de restauration.

Les composants non sélectionnables avec un ancêtre sélectionnable ne sont inclus implicitement que si leur ancêtre est inclus.

Les composants sélectionnables avec un ancêtre sélectionnable peuvent être inclus implicitement, si l’ancêtre est inclus, ou peuvent être inclus de manière explicite.

Les composants non sélectionnables sans ancêtres sélectionnables ne sont jamais inclus implicitement dans une opération de sauvegarde ou de restauration. tous ces composants doivent être ajoutés explicitement au document des composants de sauvegarde si l’un des composants de l’enregistreur y participe.

Les composants sélectionnables sans les ancêtres sélectionnables choisis par un demandeur pour la participation à une sauvegarde ou une restauration ne peuvent pas être implicitement inclus dans l’opération, mais doivent être explicitement ajoutés au document des composants de sauvegarde.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**opérations de sauvegarde incrémentielle**
</dt> <dd>

Une opération de sauvegarde ou de restauration est effectuée uniquement sur les fichiers créés ou modifiés depuis la dernière sauvegarde complète, incrémentielle ou différentielle. Voir aussi [*opérations de sauvegarde différentielle*](vssgloss-d.md).

</dd> </dl>

 

 



