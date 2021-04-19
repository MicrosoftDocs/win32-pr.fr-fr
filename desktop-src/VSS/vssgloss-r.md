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
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="a234a-103">R (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="a234a-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="a234a-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a234a-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a234a-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**demandeur**</span><span class="sxs-lookup"><span data-stu-id="a234a-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="a234a-106">Au minimum, tout processus qui interagit avec VSS pour créer et gérer des clichés instantanés et des jeux de clichés instantanés d’un ou de plusieurs volumes.</span><span class="sxs-lookup"><span data-stu-id="a234a-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="a234a-107">En règle générale, un demandeur gère les clichés instantanés pour prendre en charge d’autres fonctionnalités, telles que les opérations de sauvegarde et de restauration et la mise en miroir de disques.</span><span class="sxs-lookup"><span data-stu-id="a234a-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="a234a-108">Voir aussi cliché [*instantané*](vssgloss-s.md), jeu de clichés [*instantanés*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="a234a-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="a234a-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Méthode Restore**</span><span class="sxs-lookup"><span data-stu-id="a234a-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="a234a-110">Spécification de la méthode de processus de restauration.</span><span class="sxs-lookup"><span data-stu-id="a234a-110">A specification of the restore process method.</span></span> <span data-ttu-id="a234a-111">Il contrôle ces problèmes, par exemple si les fichiers sont remplacés lors de la restauration.</span><span class="sxs-lookup"><span data-stu-id="a234a-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="a234a-112">Si un paramètre de méthode de restauration est en conflit avec ceux de la cible de restauration, la cible de restauration est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="a234a-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="a234a-113">Voir aussi *cible de restauration*.</span><span class="sxs-lookup"><span data-stu-id="a234a-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="a234a-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restaurer la cible**</span><span class="sxs-lookup"><span data-stu-id="a234a-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="a234a-115">Sous VSS, une cible de restauration est une spécification de la façon dont un demandeur doit restaurer un fichier, par exemple, s’il doit remplacer les fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="a234a-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



