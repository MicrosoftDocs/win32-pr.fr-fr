---
description: Les opérations de sauvegarde et de restauration copient généralement les fichiers à partir d’un emplacement donné, par défaut sur le disque, sur le support de sauvegarde, puis effectuent une restauration à partir de ce média vers le même emplacement par défaut sur le disque.
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: Emplacements de restauration et de sauvegarde non par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519644"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="96bf2-103">Emplacements de restauration et de sauvegarde non par défaut</span><span class="sxs-lookup"><span data-stu-id="96bf2-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="96bf2-104">Les opérations de sauvegarde et de restauration copient généralement les fichiers à partir d’un emplacement donné, par défaut sur le disque, sur le support de sauvegarde, puis effectuent une restauration à partir de ce média vers le même emplacement par défaut sur le disque.</span><span class="sxs-lookup"><span data-stu-id="96bf2-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="96bf2-105">Il existe de nombreuses raisons, en particulier lorsque vous traitez des processus en cours d’exécution, et non pas pour suivre ce modèle simple.</span><span class="sxs-lookup"><span data-stu-id="96bf2-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="96bf2-106">VSS prend en charge l’utilisation de sources non standard pour la sauvegarde et d’autres destinations pour la restauration, et comprend des mécanismes permettant d’utiliser des sous-ensembles de fichiers et de remapper des fichiers.</span><span class="sxs-lookup"><span data-stu-id="96bf2-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="96bf2-107">Utilisation de chemins alternatifs pendant la sauvegarde</span><span class="sxs-lookup"><span data-stu-id="96bf2-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="96bf2-108">Utilisation d’autres emplacements pendant la restauration</span><span class="sxs-lookup"><span data-stu-id="96bf2-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="96bf2-109">Utilisation de nouvelles cibles pendant la restauration</span><span class="sxs-lookup"><span data-stu-id="96bf2-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="96bf2-110">Utilisation de fichiers partiels</span><span class="sxs-lookup"><span data-stu-id="96bf2-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="96bf2-111">Utilisation des cibles dirigées</span><span class="sxs-lookup"><span data-stu-id="96bf2-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



