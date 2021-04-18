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
# <a name="functionality-removed-from-windows-server-2003"></a>Fonctionnalités supprimées de Windows Server 2003

La version de Windows Server 2003 de VSS ne prend plus en charge les éléments suivants :

-   Les enregistreurs ne peuvent pas spécifier de nouvelles destinations de restauration de fichiers ([*nouveaux emplacements cibles*](vssgloss-n.md)) lors des opérations de restauration.
-   Le remontage d’un cliché instantané exposé comme volume inscriptible n’est plus pris en charge. La méthode **IVssBackupComponents :: RemountReadWrite** n’est plus disponible.
-   Les enregistreurs ne peuvent pas spécifier de fichiers inclus explicitement (à l’aide de [**IVssCreateWriterMetadata :: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). Les fichiers peuvent être ajoutés à un composant uniquement dans le cadre d’un jeu de fichiers à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).

    Les fichiers peuvent toujours être exclus explicitement d’un composant à l’aide de [**IVssCreateWriterMetadata :: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).

 

 



