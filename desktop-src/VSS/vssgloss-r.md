---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514182"
---
# <a name="r-volume-shadow-copy-service"></a>R (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**demandeur**
</dt> <dd>

Au minimum, tout processus qui interagit avec VSS pour créer et gérer des clichés instantanés et des jeux de clichés instantanés d’un ou de plusieurs volumes.

En règle générale, un demandeur gère les clichés instantanés pour prendre en charge d’autres fonctionnalités, telles que les opérations de sauvegarde et de restauration et la mise en miroir de disques. Voir aussi cliché [*instantané*](vssgloss-s.md), jeu de clichés [*instantanés*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Méthode Restore**
</dt> <dd>

Spécification de la méthode de processus de restauration. Il contrôle ces problèmes, par exemple si les fichiers sont remplacés lors de la restauration. Si un paramètre de méthode de restauration est en conflit avec ceux de la cible de restauration, la cible de restauration est prioritaire. Voir aussi *cible de restauration*.

</dd> <dt>

<span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restaurer la cible**
</dt> <dd>

Sous VSS, une cible de restauration est une spécification de la façon dont un demandeur doit restaurer un fichier, par exemple, s’il doit remplacer les fichiers existants.

</dd> </dl>

 

 



