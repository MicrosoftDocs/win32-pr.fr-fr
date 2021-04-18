---
description: 'La version de Windows Server 2003 de VSS ne prend plus en charge les éléments suivants :'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Fonctionnalités supprimées de Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542927"
---
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="4c847-103">Fonctionnalités supprimées de Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c847-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="4c847-104">La version de Windows Server 2003 de VSS ne prend plus en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="4c847-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="4c847-105">Les enregistreurs ne peuvent pas spécifier de nouvelles destinations de restauration de fichiers ([*nouveaux emplacements cibles*](vssgloss-n.md)) lors des opérations de restauration.</span><span class="sxs-lookup"><span data-stu-id="4c847-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="4c847-106">Le remontage d’un cliché instantané exposé comme volume inscriptible n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4c847-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="4c847-107">La méthode **IVssBackupComponents :: RemountReadWrite** n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="4c847-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="4c847-108">Les enregistreurs ne peuvent pas spécifier de fichiers inclus explicitement (à l’aide de [**IVssCreateWriterMetadata :: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span><span class="sxs-lookup"><span data-stu-id="4c847-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="4c847-109">Les fichiers peuvent être ajoutés à un composant uniquement dans le cadre d’un jeu de fichiers à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span><span class="sxs-lookup"><span data-stu-id="4c847-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="4c847-110">Les fichiers peuvent toujours être exclus explicitement d’un composant à l’aide de [**IVssCreateWriterMetadata :: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span><span class="sxs-lookup"><span data-stu-id="4c847-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



