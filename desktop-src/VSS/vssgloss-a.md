---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 928341a3-ed3a-4db0-9648-1a5efaff5435
title: A (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e654c0742c824ae7ad17d91e3a2ffa65c9e6bf77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515247"
---
# <a name="a-volume-shadow-copy-service"></a><span data-ttu-id="2cc0b-103">A (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="2cc0b-103">A (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="2cc0b-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="2cc0b-104">A [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="2cc0b-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Événement d’abandon**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-105"><span id="base.vssgloss_abort_event"></span><span id="BASE.VSSGLOSS_ABORT_EVENT"></span>**Abort event**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-106">Événement VSS émis par le Service VSS indiquant qu’une opération de restauration ou de sauvegarde conforme a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-106">A VSS event issued by the Volume Shadow Copy Service indicating that a compliant backup or restore operation has been aborted.</span></span> <span data-ttu-id="2cc0b-107">Le gestionnaire d’événements est **CVssWriter :: OnAbort**.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-107">The event handler is **CVssWriter::OnAbort**.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0b-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-108"><span id="base.vssgloss_active_directory"></span><span id="BASE.VSSGLOSS_ACTIVE_DIRECTORY"></span>**Active Directory**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-109">Active Directory Service (ADSI) est un service basé sur COM qui fournit un mécanisme de localisation, d’identification et d’accès aux utilisateurs et aux ressources disponibles dans un système d’environnement informatique distribué.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-109">Active Directory Service (ADSI) is a COM-based service providing a mechanism for locating, identifying, and accessing the users and resources available in a distributed computing environment system.</span></span> <span data-ttu-id="2cc0b-110">En particulier, le service Active Directory est utilisé pour gérer les informations d’annuaire d’entreprise en vue de leur distribution par un serveur de domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-110">In particular, the Active Directory service is used to manage enterprise directory information for distribution by a Windows domain server.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0b-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**mappage d’emplacement secondaire**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-111"><span id="base.vssgloss_alternate_location_mapping"></span><span id="BASE.VSSGLOSS_ALTERNATE_LOCATION_MAPPING"></span>**alternate location mapping**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-112">Chemin d’accès, autre que le chemin d’accès d’origine d’un fichier, dans lequel le fichier peut être restauré dans certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-112">A path, other than a file's original path, to which the file may be restored under certain conditions.</span></span> <span data-ttu-id="2cc0b-113">En règle générale, les mappages d’emplacements de substitution ne sont pas définis pour un seul fichier bien défini, mais pour une paire chemin/spécification de fichier, et peuvent être récursifs.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-113">Typically, alternate location mappings are not defined for a single well-defined file, but for a path/file specification pair, and may be recursive.</span></span>

<span data-ttu-id="2cc0b-114">Un autre mappage d’emplacement est utilisé uniquement au cours d’une opération de restauration et ne doit pas être confondu avec un autre chemin d’accès, qui est utilisé uniquement pendant une opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-114">An alternate location mapping is used only during a restore operation and should not be confused with an alternate path, which is used only during a backup operation.</span></span> <span data-ttu-id="2cc0b-115">Consultez également *chemin alternatif*.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-115">See also *alternate path*.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0b-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**autre chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-116"><span id="base.vssgloss_alternate_path"></span><span id="BASE.VSSGLOSS_ALTERNATE_PATH"></span>**alternate path**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-117">Pendant les opérations de sauvegarde, une paire chemin/spécification de fichier (gérée par une instance de l’interface **IVssWMFiledesc** ) est considérée comme ayant un chemin alternatif si son descripteur de fichier (tel que retourné par **IVssWMFiledesc :: GetAlternateLocation**) est non null.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-117">During backup operations, a path/file specification pair (handled by an instance of the **IVssWMFiledesc** interface) is said to have an alternate path if its file descriptor (as returned by **IVssWMFiledesc::GetAlternateLocation**) is non-NULL.</span></span> <span data-ttu-id="2cc0b-118">C’est à partir de ce chemin d’accès, au lieu du chemin d’accès spécifié par défaut, que les fichiers doivent être copiés lorsqu’un volume est sauvegardé.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-118">It is from this path, rather than the default specified path, that files are to be copied when a volume is backed up.</span></span>

<span data-ttu-id="2cc0b-119">Un autre chemin d’accès est utilisé uniquement pendant une opération de sauvegarde et ne doit pas être confondu avec un autre mappage d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-119">An alternate path is used only during a backup operation and should not be confused with an alternate location mapping.</span></span> <span data-ttu-id="2cc0b-120">Un mappage d’emplacement de remplacement est utilisé uniquement pendant les opérations de restauration.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-120">An alternate location mapping is used only during restore operations.</span></span> <span data-ttu-id="2cc0b-121">Voir aussi *mappage d’emplacements alternatifs*.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-121">See also *alternate location mapping*.</span></span>

</dd> <dt>

<span data-ttu-id="2cc0b-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**niveau de l’application**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-122"><span id="base.vssgloss_application_level"></span><span id="BASE.VSSGLOSS_APPLICATION_LEVEL"></span>**application level**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-123">Utilisé par VSS pour indiquer le point au cours de la création d’un cliché instantané qu’un enregistreur est averti d’un gel.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-123">Used by VSS to indicate the point in the course of the creation of a shadow copy that a writer is notified of a freeze.</span></span> <span data-ttu-id="2cc0b-124">Voir aussi [*applications de niveau*](vssgloss-b.md)principal, [*figer*](vssgloss-f.md), [*applications frontales*](vssgloss-f.md), clichés [*instantanés*](vssgloss-s.md), [*applications au niveau système*](vssgloss-s.md), [*enregistreur*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="2cc0b-124">See also [*back-end level applications*](vssgloss-b.md), [*freeze*](vssgloss-f.md), [*front-end level applications*](vssgloss-f.md), [*shadow copy*](vssgloss-s.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cc0b-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**cliché instantané récupéré automatiquement**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-125"><span id="base.vssgloss_auto_recoved_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RECOVED_SHADOW_COPY"></span>**auto-recovered shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-126">Cliché instantané qui a été traité par un enregistreur pour être dans un état totalement cohérent pour les actions de sauvegarde ou d’exploration de données (par exemple, pour restaurer toutes les transactions qui n’ont pas encore été effectuées au point où le cliché instantané a été créé). Cela peut être initié par un enregistreur en spécifiant un indicateur approprié à partir de l’énumération des **\_ \_ indicateurs du composant VSS** dans le membre **dwComponentFlags** de la structure **VSS \_ COMPONENTINFO** ou par un demandeur en ajoutant l’indicateur de **\_ récupération VSS VOLSNAP \_ attr \_ Rollback \_ Recovery** au contexte du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-126">A shadow copy that has had additional processing by a writer to be in a completely consistent state for backup or data mining actions (for example, rolling back all transactions that did not yet complete at the point that the shadow copy was created.) This can be initiated by a writer by specifying an appropriate flag from the **VSS\_COMPONENT\_FLAGS** enumeration in the **dwComponentFlags** member of the **VSS\_COMPONENTINFO** structure or by a requester by adding the **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** flag to the context for the shadow copy.</span></span> <span data-ttu-id="2cc0b-127">La récupération automatique permet d’utiliser les données de clichés instantanés sur un volume en lecture seule, pour l’exploration de données, des restaurations partielles (par exemple, des éléments sélectionnés dans une base de données) ou d’autres fins.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-127">Auto-recovery allows the shadow copied data to be used on a read-only volume, for data mining, partial restores (for example selected items in a database), or other purposes.</span></span>

<span data-ttu-id="2cc0b-128">Voir aussi cliché [*instantané transportable*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="2cc0b-128">See also [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cc0b-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**cliché instantané de la mise en sortie automatique**</span><span class="sxs-lookup"><span data-stu-id="2cc0b-129"><span id="base.vssgloss_auto_release_shadow_copy"></span><span id="BASE.VSSGLOSS_AUTO_RELEASE_SHADOW_COPY"></span>**auto-release shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="2cc0b-130">Cliché instantané qui sera supprimé à la fin d’une opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-130">A shadow copy that will be deleted upon the termination of a backup operation.</span></span> <span data-ttu-id="2cc0b-131">Par programmation, cela signifie que le cliché instantané sera supprimé lors de la libération de l’interface **IVssBackupComponents** .</span><span class="sxs-lookup"><span data-stu-id="2cc0b-131">Programmatically, this means the shadow copy will be deleted when the **IVssBackupComponents** interface is released.</span></span> <span data-ttu-id="2cc0b-132">Un cliché instantané de mise en sortie automatique ne peut pas être persistant.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-132">An auto-release shadow copy cannot be persistent.</span></span>

<span data-ttu-id="2cc0b-133">Par défaut, tous les clichés instantanés sont en sortie automatique.</span><span class="sxs-lookup"><span data-stu-id="2cc0b-133">By default, all shadow copies are auto-release.</span></span> <span data-ttu-id="2cc0b-134">Voir aussi cliché [*instantané persistant*](vssgloss-p.md), cliché [*instantané transportable*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="2cc0b-134">See also [*persistent shadow copy*](vssgloss-p.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> </dl>

 

 



