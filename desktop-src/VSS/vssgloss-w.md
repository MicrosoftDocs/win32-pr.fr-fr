---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526266"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="7ab08-103">W (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="7ab08-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="7ab08-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="7ab08-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7ab08-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Protection des fichiers Windows**</span><span class="sxs-lookup"><span data-stu-id="7ab08-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="7ab08-106">Service système qui protège les fichiers de système d’exploitation spéciaux.</span><span class="sxs-lookup"><span data-stu-id="7ab08-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="7ab08-107">Si l’un de ces fichiers est supprimé ou remplacé, la protection des fichiers Windows remplace le fichier par le cache d’origine.</span><span class="sxs-lookup"><span data-stu-id="7ab08-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="7ab08-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**écrit**</span><span class="sxs-lookup"><span data-stu-id="7ab08-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="7ab08-109">Application qui coordonne ses opérations d’e/s avec cliché instantané VSS et les opérations associées aux clichés instantanés (telles que les sauvegardes et restaurations) afin que les données contenues sur le volume cliché instantané soient dans un état cohérent.</span><span class="sxs-lookup"><span data-stu-id="7ab08-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="7ab08-110">Pour prendre en charge cette coordination, un enregistreur doit implémenter une instance d’une classe dérivée de la classe de base abstraite **CVssWriter** pour communiquer avec l’infrastructure VSS.</span><span class="sxs-lookup"><span data-stu-id="7ab08-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="7ab08-111">Voir aussi cliché [*instantané*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="7ab08-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ab08-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**classe Writer**</span><span class="sxs-lookup"><span data-stu-id="7ab08-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="7ab08-113">Identificateur global unique (GUID) fourni par un enregistreur pendant l’initialisation pour indiquer qu’il appartient à un type donné d’enregistreurs.</span><span class="sxs-lookup"><span data-stu-id="7ab08-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="7ab08-114">Par exemple, plusieurs implémentations d’un writer peuvent partager le même ID de classe de writer.</span><span class="sxs-lookup"><span data-stu-id="7ab08-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="7ab08-115">Les writers de la même classe peuvent être distingués par leurs instances de writer.</span><span class="sxs-lookup"><span data-stu-id="7ab08-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="7ab08-116">Il revient à un développeur d’applications de spécifier des classes d’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="7ab08-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="7ab08-117">Voir aussi *instance* de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="7ab08-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="7ab08-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**instance d’enregistreur**</span><span class="sxs-lookup"><span data-stu-id="7ab08-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="7ab08-119">Identificateur global unique (GUID) fourni par VSS pour chaque processus d’écriture exécuté sur un système.</span><span class="sxs-lookup"><span data-stu-id="7ab08-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="7ab08-120">Une valeur unique pour l’instance du writer est générée à chaque démarrage de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="7ab08-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="7ab08-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Document de métadonnées de l’enregistreur**</span><span class="sxs-lookup"><span data-stu-id="7ab08-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="7ab08-122">Document XML créé par un enregistreur (à l’aide de l’interface **IVssCreateWriterMetadata** ) contenant des informations sur l’État et les composants du writer.</span><span class="sxs-lookup"><span data-stu-id="7ab08-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="7ab08-123">Un demandeur peut interroger des documents de métadonnées de l’enregistreur (à l’aide de l’interface **IVssExamineWriterMetadata** ) lors d’une opération de restauration ou de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7ab08-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="7ab08-124">Un document de métadonnées de l’enregistreur contient la liste de tous les composants d’un enregistreur, chacun d’entre eux pouvant participer à une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="7ab08-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="7ab08-125">Cela diffère du document sur les composants de sauvegarde du demandeur, qui contient uniquement les composants explicitement inclus pour une opération de sauvegarde ou de restauration.</span><span class="sxs-lookup"><span data-stu-id="7ab08-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="7ab08-126">Une fois construit, le document de métadonnées de l’enregistreur doit être affiché en tant qu’objet en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7ab08-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="7ab08-127">Il peut être enregistré sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7ab08-127">It can be saved to disk.</span></span> <span data-ttu-id="7ab08-128">Voir aussi [*document*](vssgloss-b.md)sur les composants de sauvegarde, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="7ab08-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



