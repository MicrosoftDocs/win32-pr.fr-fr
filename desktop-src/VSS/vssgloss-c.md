---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751556"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="b532d-103">C (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="b532d-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="b532d-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="b532d-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="b532d-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="b532d-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-106">Entité approuvée pour émettre des certificats qui déclarent que le destinataire individuel, l’ordinateur ou l’organisation qui demande le certificat répond aux conditions d’une stratégie établie.</span><span class="sxs-lookup"><span data-stu-id="b532d-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="b532d-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**cliché instantané accessible par le client**</span><span class="sxs-lookup"><span data-stu-id="b532d-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-108">Cliché instantané créé par le fournisseur système pour prendre en charge clichés instantanés pour dossiers partagés et d’autres mécanismes de restauration, qui permettent aux clients de voir les anciennes versions des fichiers et d’annuler des erreurs sans nécessiter de restauration complète.</span><span class="sxs-lookup"><span data-stu-id="b532d-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="b532d-109">Un cliché instantané accessible par le client est créé à l’aide de la valeur accessible par le **\_ \_ client \_ CTX VSS** de l’énumération du [**\_ \_ \_ contexte de capture instantanée VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) .</span><span class="sxs-lookup"><span data-stu-id="b532d-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="b532d-110">En outre, la \_ \_ \_ valeur accessible par le client VSS VOLSNAP attr \_ de l’énumération des [**\_ \_ attributs d' \_ instantané \_ de volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) est définie automatiquement pour les clichés instantanés accessibles par le client.</span><span class="sxs-lookup"><span data-stu-id="b532d-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="b532d-111">Voir aussi [*clichés instantanés pour dossiers partagés*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b532d-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b532d-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**-**</span><span class="sxs-lookup"><span data-stu-id="b532d-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-113">Groupe de fichiers, défini par un enregistreur, qui doit être traité comme une unité lors des opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="b532d-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="b532d-114">Voir aussi [*composant de base de données*](vssgloss-d.md), [*composant de groupe de fichiers*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="b532d-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="b532d-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dépendance de composant**</span><span class="sxs-lookup"><span data-stu-id="b532d-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-116">Une situation dans laquelle un composant (et le jeu de composants qu’il définit) géré par un enregistreur ne peut pas être sauvegardée ou restaurée indépendamment des composants gérés par d’autres rédacteurs.</span><span class="sxs-lookup"><span data-stu-id="b532d-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="b532d-117">Une dépendance n’indique pas un ordre de préférence entre le composant avec les dépendances documentées et les composants dont il dépend : une dépendance indique simplement que le composant et les composants dont il dépend doivent toujours être sauvegardés ou restaurés ensemble.</span><span class="sxs-lookup"><span data-stu-id="b532d-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="b532d-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**mode composant**</span><span class="sxs-lookup"><span data-stu-id="b532d-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-119">Mode dans lequel une opération de sauvegarde ou de restauration utilise les informations de composant d’un enregistreur.</span><span class="sxs-lookup"><span data-stu-id="b532d-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="b532d-120">Voir aussi [*composant sélectionnable*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b532d-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b532d-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**ensemble de composants**</span><span class="sxs-lookup"><span data-stu-id="b532d-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-122">Groupe de composants avec au moins un composant sélectionnable (pour la sauvegarde ou la restauration) et un certain nombre de composants non sélectionnables organisés dans une hiérarchie par leurs chemins logiques.</span><span class="sxs-lookup"><span data-stu-id="b532d-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="b532d-123">La participation implicite à une opération de sauvegarde ou de restauration dépend de l’inclusion explicite du composant sélectionnable de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="b532d-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="b532d-124">Seules les informations sur les composants de ce composant sélectionnable sont incluses dans le document sur les composants de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="b532d-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="b532d-125">Un jeu de composants peut inclure des sous-composants sélectionnables et non sélectionnables.</span><span class="sxs-lookup"><span data-stu-id="b532d-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="b532d-126">Voir aussi [*chemin logique*](vssgloss-l.md), [*composant sélectionnable*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="b532d-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="b532d-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**cliché instantané de copie en écriture**</span><span class="sxs-lookup"><span data-stu-id="b532d-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-128">Cliché instantané créé en enregistrant uniquement les différences par rapport au volume d’origine.</span><span class="sxs-lookup"><span data-stu-id="b532d-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="b532d-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**État de cohérence des incidents**</span><span class="sxs-lookup"><span data-stu-id="b532d-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="b532d-130">État des disques équivalant à ce qui serait trouvé à la suite d’une défaillance catastrophique qui arrête brusquement le système.</span><span class="sxs-lookup"><span data-stu-id="b532d-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="b532d-131">Une restauration à partir d’un tel jeu de clichés instantanés équivaut à un redémarrage après un arrêt brutal.</span><span class="sxs-lookup"><span data-stu-id="b532d-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="b532d-132">Il s’agit de l’État par défaut des données qui ont été copiées par des clichés instantanés sans la prise en charge des enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="b532d-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



