---
description: 'la version 2003 du serveur Windows de VSS ne prend plus en charge les éléments suivants :'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: fonctionnalités supprimées du serveur Windows 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7cd2cbfce24717bdd0bf0c36db1c5d8ff7faddebd5b7795cff6640b74df3c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006359"
---
# <a name="functionality-removed-from-windows-server-2003"></a>fonctionnalités supprimées du serveur Windows 2003

la version 2003 du serveur Windows de VSS ne prend plus en charge les éléments suivants :

-   Les enregistreurs ne peuvent pas spécifier de nouvelles destinations de restauration de fichiers ([*nouveaux emplacements cibles*](vssgloss-n.md)) lors des opérations de restauration.
-   Le remontage d’un cliché instantané exposé comme volume inscriptible n’est plus pris en charge. La méthode **IVssBackupComponents :: RemountReadWrite** n’est plus disponible.
-   Les enregistreurs ne peuvent pas spécifier de fichiers inclus explicitement (à l’aide de [**IVssCreateWriterMetadata :: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). Les fichiers peuvent être ajoutés à un composant uniquement dans le cadre d’un jeu de fichiers à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).

    Les fichiers peuvent toujours être exclus explicitement d’un composant à l’aide de [**IVssCreateWriterMetadata :: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).

 

 



