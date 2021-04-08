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
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="10c1b-103">I (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="10c1b-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="10c1b-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="10c1b-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="10c1b-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identifier l’événement**</span><span class="sxs-lookup"><span data-stu-id="10c1b-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="10c1b-106">Événement VSS indiquant qu’un enregistreur ou un demandeur doit interroger le writer actuel.</span><span class="sxs-lookup"><span data-stu-id="10c1b-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="10c1b-107">Il est utilisé pour construire les informations de métadonnées du writer actuel.</span><span class="sxs-lookup"><span data-stu-id="10c1b-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="10c1b-108">Voir aussi [*demandeur*](vssgloss-r.md), [*enregistreur*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="10c1b-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="10c1b-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusion de composant implicite**</span><span class="sxs-lookup"><span data-stu-id="10c1b-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="10c1b-110">Ne pas ajouter les informations d’un composant au document des composants de sauvegarde d’un demandeur lorsqu’il participe à une opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="10c1b-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="10c1b-111">Les composants non sélectionnables avec un ancêtre sélectionnable ne sont inclus implicitement que si leur ancêtre est inclus.</span><span class="sxs-lookup"><span data-stu-id="10c1b-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="10c1b-112">Les composants sélectionnables avec un ancêtre sélectionnable peuvent être inclus implicitement, si l’ancêtre est inclus, ou peuvent être inclus de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="10c1b-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="10c1b-113">Les composants non sélectionnables sans ancêtres sélectionnables ne sont jamais inclus implicitement dans une opération de sauvegarde ou de restauration. tous ces composants doivent être ajoutés explicitement au document des composants de sauvegarde si l’un des composants de l’enregistreur y participe.</span><span class="sxs-lookup"><span data-stu-id="10c1b-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="10c1b-114">Les composants sélectionnables sans les ancêtres sélectionnables choisis par un demandeur pour la participation à une sauvegarde ou une restauration ne peuvent pas être implicitement inclus dans l’opération, mais doivent être explicitement ajoutés au document des composants de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="10c1b-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="10c1b-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**opérations de sauvegarde incrémentielle**</span><span class="sxs-lookup"><span data-stu-id="10c1b-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="10c1b-116">Une opération de sauvegarde ou de restauration est effectuée uniquement sur les fichiers créés ou modifiés depuis la dernière sauvegarde complète, incrémentielle ou différentielle.</span><span class="sxs-lookup"><span data-stu-id="10c1b-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="10c1b-117">Voir aussi [*opérations de sauvegarde différentielle*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="10c1b-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



