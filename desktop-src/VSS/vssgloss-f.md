---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751541"
---
# <a name="f-volume-shadow-copy-service"></a><span data-ttu-id="33d26-103">F (Service VSS)</span><span class="sxs-lookup"><span data-stu-id="33d26-103">F (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="33d26-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="33d26-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="33d26-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**composant de groupe de fichiers**</span><span class="sxs-lookup"><span data-stu-id="33d26-105"><span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**file group component**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-106">Groupe de fichiers autres que ceux utilisés comme base de données et définis par un enregistreur comme ayant besoin d’être gérés comme une unité lors des opérations de sauvegarde et de restauration.</span><span class="sxs-lookup"><span data-stu-id="33d26-106">A group of files other than those used as a database and defined by a writer as needing to be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="33d26-107">Voir aussi [*composant*](vssgloss-c.md), [*composant base de données*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="33d26-107">See also [*component*](vssgloss-c.md), [*database component*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="33d26-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**jeu de fichiers**</span><span class="sxs-lookup"><span data-stu-id="33d26-108"><span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**file set**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-109">Combinaison d’un chemin d’accès, d’une spécification de fichier et d’un indicateur récursif décrivant un fichier ou un groupe de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33d26-109">The combination of a path, file specification, and recursive flag describing one of a file or group of files.</span></span> <span data-ttu-id="33d26-110">Par exemple, les fichiers sont ajoutés aux composants dans les jeux de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33d26-110">For example, files are added to components in file sets.</span></span>

<span data-ttu-id="33d26-111">Sauf indication contraire, les chemins d’accès d’un jeu de fichiers sont des chemins d’accès Windows standard et peuvent contenir des variables d’environnement (par exemple,% SystemRoot%) mais ne peut pas contenir de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="33d26-111">Unless otherwise indicated, a file set's paths are standard Windows paths and can contain environment variables (for example, %SystemRoot%) but cannot contain wildcard characters.</span></span> <span data-ttu-id="33d26-112">Il n’est pas nécessaire que le chemin d’accès se termine par une barre oblique inverse (« \\ »).</span><span class="sxs-lookup"><span data-stu-id="33d26-112">There is no requirement that the path end with a backslash ("\\").</span></span> <span data-ttu-id="33d26-113">Il s’agit des applications qui récupèrent ces informations pour les vérifier.</span><span class="sxs-lookup"><span data-stu-id="33d26-113">It is up to applications that retrieve this information to check it.</span></span>

<span data-ttu-id="33d26-114">La spécification de fichier contenue dans un jeu de fichiers indique le nom du ou des fichiers qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="33d26-114">The file specification contained in a file set indicates the name of the file or files it includes.</span></span> <span data-ttu-id="33d26-115">Cette spécification de fichier ne peut pas contenir de spécifications de répertoire (par exemple, aucune barre oblique inverse), mais peut contenir le ?</span><span class="sxs-lookup"><span data-stu-id="33d26-115">This file specification cannot contain directory specifications (for example, no backslashes) but can contain the ?</span></span> <span data-ttu-id="33d26-116">et les \* caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="33d26-116">and \* wildcard characters.</span></span>

<span data-ttu-id="33d26-117">La balise récursive est une valeur booléenne qui spécifie si le chemin d’accès du jeu de fichiers doit être traité comme un seul répertoire ou s’il indique une hiérarchie de répertoires à traverser de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="33d26-117">The recursive tag is a Boolean specifying whether the file set's path should be treated as a only a single directory or if it indicates a hierarchy of directories to be traversed recursively.</span></span> <span data-ttu-id="33d26-118">La valeur booléenne est **true** si le chemin d’accès est traité comme une hiérarchie de répertoires à parcourir de manière récursive, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="33d26-118">The Boolean is **true** if the path is treated as a hierarchy of directories to be traversed recursively, or **false** if not.</span></span>

<span data-ttu-id="33d26-119">Les informations relatives à un jeu de fichiers sont retournées via des instances de l’interface **IVssWMFiledesc** . elles peuvent contenir des chemins d’accès alternatifs, des mappages d’emplacement de remplacement et des paramètres de prise en charge de schéma au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="33d26-119">Information about a file set is returned through instances of the **IVssWMFiledesc** interface, and can contain additional information includes alternate paths, alternate location mappings, and file-level schema support settings.</span></span>

<span data-ttu-id="33d26-120">Voir aussi [*chemin alternatif*](vssgloss-a.md), [*mappage d’emplacement secondaire*](vssgloss-a.md), [*composant*](vssgloss-c.md), *spécification de fichier*.</span><span class="sxs-lookup"><span data-stu-id="33d26-120">See also [*alternate path*](vssgloss-a.md), [*alternate location mapping*](vssgloss-a.md), [*component*](vssgloss-c.md), *file specification*.</span></span>

</dd> <dt>

<span data-ttu-id="33d26-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**spécification de fichier**</span><span class="sxs-lookup"><span data-stu-id="33d26-121"><span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**file specification**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-122">Utilisé pour faire correspondre des fichiers dans un répertoire et pour définir un jeu de fichiers.</span><span class="sxs-lookup"><span data-stu-id="33d26-122">Used to match files within a directory and to define a file set.</span></span> <span data-ttu-id="33d26-123">Elle ne peut pas contenir de spécifications de répertoire (par exemple, aucune barre oblique inverse), mais elle peut contenir le ?</span><span class="sxs-lookup"><span data-stu-id="33d26-123">It cannot contain directory specifications (for example, no backslashes) but it can contain the ?</span></span> <span data-ttu-id="33d26-124">et les \* caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="33d26-124">and \* wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="33d26-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Service de réplication de fichiers**</span><span class="sxs-lookup"><span data-stu-id="33d26-125"><span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**File Replication Service**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-126">Utilisé pour répliquer des fichiers système dans un répertoire de volume système (SysVol) redondant pour prendre en charge la survie du système de fichiers, en particulier pour les systèmes de fichiers distribués.</span><span class="sxs-lookup"><span data-stu-id="33d26-126">Used to replicate system files in a redundant system volume (SysVol) directory to support file system survivability, particularly for distributed file systems.</span></span>

</dd> <dt>

<span data-ttu-id="33d26-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**antigel**</span><span class="sxs-lookup"><span data-stu-id="33d26-127"><span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**freeze**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-128">Un laps de temps pendant le processus de création de clichés instantanés lorsque tous les enregistreurs ont vidé leurs écritures sur les volumes et ne lancent pas d’écritures supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="33d26-128">A period of time during the shadow copy creation process when all writers have flushed their writes to the volumes and are not initiating additional writes.</span></span>

</dd> <dt>

<span data-ttu-id="33d26-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Figer l’événement**</span><span class="sxs-lookup"><span data-stu-id="33d26-129"><span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze event**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-130">Événement VSS indiquant qu’un blocage de cliché instantané est en cours.</span><span class="sxs-lookup"><span data-stu-id="33d26-130">A VSS event indicating that a shadow copy freeze is in progress.</span></span> <span data-ttu-id="33d26-131">Voir aussi *figer*, [*cliché instantané*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="33d26-131">See also *freeze*, [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="33d26-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**applications de niveau frontal**</span><span class="sxs-lookup"><span data-stu-id="33d26-132"><span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**front-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="33d26-133">Indique le point auquel un writer est notifié d’un gel par VSS.</span><span class="sxs-lookup"><span data-stu-id="33d26-133">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="33d26-134">Les enregistreurs qui ont été initialisés en tant qu’applications de niveau frontal sont avertis avant l’initialisation des Writers en tant qu’applications de niveau principal ou application système.</span><span class="sxs-lookup"><span data-stu-id="33d26-134">Writers that were initialized as front-end level applications are notified prior to writers initialized either as back-end level applications or as system-level applications.</span></span> <span data-ttu-id="33d26-135">Voir aussi [*niveau application*](vssgloss-a.md), [*applications de niveau*](vssgloss-b.md)principal, [*applications système*](vssgloss-s.md), [*enregistreur*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="33d26-135">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> </dl>

 

 



